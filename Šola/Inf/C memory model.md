### **1. Uvod (2 minuti)**

- **vprašanje**:
    - _"Kaj se v resnici zgodi v pomnilniku, ko v jeziku C deklarirate spremenljivko? Kaj naredi računalnik z informacijami ki mu jih damo, kam jih shranjuje..."_
- **Zakaj je pomembno** razumevanje pomnilniškega modela:
    - Razumevanje pomnilniškega modela (memory model) je ključno za:
        - Učinkovito programiranje.
	        - 
        - Odpravljanje napak.
	        - npr pointer, ki kaže na del spomina po koncu izvedene funkcije, kjer te spremenljivke več ni
        - da ne pozabiš clearat spomona, ki si ga popisal z malloc (memory locate)
- **Struktura predstavitve**:
    - Razporeditev pomnilnika (memory layout).
    - Tipi spremenljivk in njihov vpliv na pomnilnik (variable types and memory impact).
    - Vrste pomnilnikov (types of memory).
    - Ključne napake (skill issues) in zaključek.
    - :3
### **2. Razporeditev pomnilnika v jeziku C (3 minute)**

- **Pomnilniški segmenti (memory segments)**:
    - **Segment kode (text/code segment)**: Shrani kodo ki se trenutno izvaja.
    - **Podatkovni segment (data segment)**: Inicializirane globalne in statične spremenljivke.
    - **Neinicializirane globalne in statične spremenljivke.
    - **Kopica (heap)**: Dinamičen, 
    - Stack (Kopica) – dolgoročen, ni avtomatičen, počasnejši
	- Heap – začasen, avtomatičen, hitrejši, določena, manjša velikost od stacka
- **Diagram**:
    - Prikaz hierarhije pomnilnika s primeri: kje so spremenljivke shranjene glede na njihovo deklaracijo.

---

### **3. Tipi spremenljivk in njihova vloga v pomnilniku (3 minute)**

- **Primitivni tipi**:
    - **Poraba pomnilnika**:
        - `int`, `char`, `float`, `double`: Pojasnite značilne velikosti v bajtih (npr. `int` običajno zaseda 4 bajte na 32-bitnem sistemu).
        - `char` = 1 bajt, `double` = 8 bajtov.
        - - **`char`**:
		    - Uporablja se za shranjevanje enega znaka (ASCII ali Unicode) ali majhnih celih števil.
		    - Zasede **1 bajt** (8 bitov).
		- **`int`**:
		    - Uporablja se za shranjevanje celih števil.
		    - Velikost je običajno **4 bajti** na večini sodobnih sistemov, vendar je na nekaterih sistemih lahko drugačna (npr. 2 bajta na starejših arhitekturah).
		- **`float`**:
		    - Shranjuje **realna števila** z decimalnimi mesti (enojna natančnost).
		    - Zasede **4 bajte** in podpira približno 7 natančnih decimalnih mest.
		- **`double`**:
		    - Shranjuje **realna števila** z večjo natančnostjo (dvojna natančnost).
		    - Zasede **8 bajtov** in podpira približno 15 decimalnih mest.
    - **Poravnava**:
        - Pravila poravnave lahko dodajo zapolnjevanje (padding). 
        - Ko določimo vrednost neki spremenljivki se ta shrani kot pointer na prvi bite te vrednosti v spominu
	        - podatkovni tipi se v spominu nahajajo na poziciji, ki je večkratnik njegove velikosti, za optimizacijo procesov (procesor ve, da se podatek lahko nahaja samo na mestu, ki je večkratnik njegove velikosti)
		        - vmes dobimo padding, ki poskrbi za pravilno poravnavo nadaljnih podatkov. Notri lahko nima nič ali pa neko naključno vrednost, ki je bila prej tam.
- **Sestavljeni tipi**:
    - **Tabele (arrays)**: Shranjene v zaporednem pomnilniku.
        - Primer: deklariramo tabelo `int arr[5];` ta porabi `5 * sizeof(int)` bajtov na skladu.
        - 
    - **Strukture (structs)**:
        - Zapolnjevanje za poravnavo in njegov vpliv.
    - **Kazalci (pointers)**:
        - Shranjujejo naslove v pomnilniku, običajno 4 bajte (32-bitni sistemi) ali 8 bajtov (64-bitni sistemi).
        - Dinamično dodeljeni kazalci uporabljajo kopico (`malloc` ali podobno).
- **Obseg in življenjska doba**:
    - **Globalne/statične spremenljivke**: Shranjene v podatkovnem ali BSS segmentu.
    - **Lokalne spremenljivke**: Shranjene na skladu.
    - **Dinamične spremenljivke**: Dodeljene na kopici z uporabo `malloc` ali podobnih funkcij.

---

### **4. Vrste pomnilnika (5 minut)**

- **Sklad**
    - Značilnosti: LIFO, upravlja ga prevajalnik, hiter.
    - Primer: Klici funkcij, lokalne spremenljivke.
    - Slabosti: Preliv sklada.
- **Kopica**
    - Značilnosti: Dinamična dodelitev, počasnejši dostop.
    - Funkcije: `malloc`, `calloc`, `free`.
    - Slabosti: Uhajanje pomnilnika, fragmentacija.
- **Statičen/globalen pomnilnik**
    - Življenjska doba: Celoten program.
    - Primeri uporabe.
- **Segment kode**
    - Samo za branje, shranjuje prevedena navodila.
    - Primer: Literalne nize.

---

### **5. Pogoste težave in nasveti za odpravljanje napak (4 minute)**

- **Pogoste napake**:
    - Ohlapni kazalci.
    - Dvojna sprostitev.
    - Prelivanje medpomnilnika.
    - Uhajanje pomnilnika.
- **Orodja za odpravljanje napak**:
    - `valgrind` za zaznavanje uhajanja pomnilnika.
    - Možnosti prevajalnika, kot je `-fsanitize=address`.

---

### **6. Napredni koncepti (2–3 minute)**

- **Poravnava in zapolnjevanje**:
    - Vpliv na hitrost dostopa do pomnilnika.
- **Težave pri sočasnosti**:
    - Tekmovanje za podatke v večnitenih programih.
    - Vloga spominskih ovir.
- **Optimizacije prevajalnika**:
    - Predpomnjenje in uporaba registrov.

---

### **7. Zaključek in vprašanja (2–3 minute)**

- **Ključne ugotovitve**:
    - Razumevanje pomnilniškega modela jezika C pomaga preprečiti napake in pisati učinkovito kodo.
    - Je temelj za sistemsko programiranje in aplikacije, kjer je zmogljivost ključna.
- **Naslednji koraki**:
    - Predlagajte vire za nadaljnje učenje: knjige, orodja ali spletne tečaje.
- **Vprašanja in odgovori**: Povabite občinstvo k vprašanjem.