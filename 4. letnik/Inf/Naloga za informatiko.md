# Knjige in avtorji

Za izdelavo sem uporabljala DB Bowser for SQLite
Najprej sem naredila vse tabele, ki jih bo vključevala moja podatkovna baza.
![[Pasted image 20251020214325.png]]
Prvo tabelo sem poimenovala **authors**. Vanjo sem dala entiteto *id*, katerega podatkovni tip bo integer, *name* (ime knjige) katerega podatkovni tip bo text in *size* (predstavlja število izdanih knjig) katere podatkovni tip bo integer. Pri *id* sem še označila, da gre za primarni ključ (PK - primary key) in AI (= auto- increment), kar omogoča samodejno generiranje edinstvene številke, ko se v tabelo vstavi nov zapis.

Nato sem naredila podobno stvar še za tabelo **books** . Dodala sem na sliki vidne entitete, ter označila *id* (za tabelo **books**) s PK in AI na enak način kot zgoraj. Edina razlika je bila, da sem še autor_id in označila kot tuji ključ, ter povedala, da je iz tabele **authors**.
![[Pasted image 20251020214725.png]]


Po tem sem naslednje podatke vključila v tabele

*S tem delom vstavim imena in št. izdanih knjig avtorjev v tabelo avtorji*
INSERT INTO authors (name, size) VALUES
('J.K. Rowling', 7),
('George R.R. Martin', 5),
('J.R.R. Tolkien', 4);

*S tem delom vstavim iimena, datum izdaje in id avtorja (tuji ključ) v tabelo knjige*
INSERT INTO books (name, release_date, author_id) VALUES
('Harry Potter and the Philosopher''s Stone', 1997, 1),
('Harry Potter and the Chamber of Secrets', 1998, 1),
('A Game of Thrones', 1996, 2),
('A Clash of Kings', 1998, 2),
('The Hobbit', 1937, 3),
('The Lord of the Rings: The Fellowship of the Ring', 1954, 3),
('The Lord of the Rings: The Two Towers', 1954, 3),
('The Lord of the Rings: The Return of the King', 1955, 3);

Pri vstavljanju podatkov v tabele ni potrebno ročno podajati vrednosti za stolpec **id**, saj je ta nastavljen kot  autoincrement. Program tako samodejno določi in dodeli enolično vrednost za vsak nov vnos.

Na zadnje sem Podatkovno bazo stestirala s temi ukazi:

SELECT books.name AS book_title, books.release_date, authors.name AS author_name
	Ukaz **SELECT** določa, katere stolpce želimo prikazati. Stolpec `books.name` predstavlja ime knjige iz tabele _books_, izraz `AS book_title` pa mu določi prijaznejše ime v izpisu (torej _book_title_). Stolpec `books.release_date` prikazuje leto izida knjige, medtem ko `authors.name` predstavlja ime avtorja iz tabele _authors_ in je v izpisu prikazan kot _author_name_.
FROM books
	iz tabele books
JOIN authors ON books.author_id = authors.id;
S tem delom ukaza povežemo tabeli **book** in **authors**, pri čemer se povezava izvede tako, da se stolpec *author_id*iz tabele **books**_ ujema z id iz tabele **authors**, kar SQLite-u omogoča, da ve, kateri avtor pripada posamezni knjigi.
Dobimo to:
![[Pasted image 20251020220908.png]]