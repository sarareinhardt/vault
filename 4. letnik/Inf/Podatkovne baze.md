![[Podatkovne_baze.pdf]]

##### Modeliranje realnosti
- Predmeti, osebe in dogodki v realnosti so Predmeti, osebe in dogodki v realnosti so entitete - npr. učenci, itd 
- Entiteta ima svoje lastnosti (Entiteta ima svoje lastnosti (atribute) in) in pomen  
	 Človek nekatere entitete zaznava, sprejema vtise in iz njih oblikuje koncepcije
	 Koncepcije povezuje in dopolnjuje ter v glavi oblikuje model realnosti
	 Model realnosti sestavljajo le tisti deli, ki nas v določenem primeru zanimajo –– okrnjena realnost
	 **Entitete** s skupnimi lastnostmi lahko združimo v **entitetno množico**(= skupina entitet, za katere imamo skupne podatke, npr. ena entitetna množica so dijaki, ena profesorji, ...) oz.množico oz. entitetnientitetni tip in join jo poimenujemo z entitetnim imenom

##### Informacijski sistem
- Ali neko podjetje, ustanova, … , lahko deluje ne da bi na nek načinda bi na nek način zbirali podatke zbirali podatke o svojemsvojem delovanju (Zakaj jih potrebuje?)(Zakaj jih potrebuje?) 
- Katere podatke Katere podatke potrebuje za svoje delovanje neko podjetje, šola, šolska kuhinja, …neko podjetje, šola, šolska kuhinja, 
- Kaj se dogaja v npr. privatni zobozdravstveni ordinaciji?
- informacijski sistem je sistem, v katerem se **generirajo, arhivirajo in pretakajo podatki.podatki.** 
- ISIS ne more obstajati sam zažene more obstajati sam zase, ampak le kot, ampak le kot del ali podsistem nekega drugega sistemadel ali podsistem nekega drugega sistema (organizacije), k s posredovanjem podatkov(organizacije), k s posredovanjem podatkov pomaga ljudem v organizaciji, da svoje delopomaga ljudem v organizaciji, da svoje delo opravijoopravijo lažjelažje,, hitrejehitreje,, boljebolje inin ceneje
![[Pasted image 20250916083757.png]]
##### elementi informacijskega sistema
- Strojna oprema 
- Omrežje
- Programska oprema
- Podatkovna baza
- Postopki in metode
- Ljudje

##### Naloge IS
- zbiranje podatkov,
- hranjenje podatkov,
- obdelava podatkov,
- varovanje podatkov,
- posredovanje podatkov uporabnikom
Idealen IS posreduje prave podatke ob pravem času pravim ljudem z minimalnimi stroški
![[Pasted image 20250916084158.png]]
*Podatkovna baza*
Je model v računalniku, ki:  
- Vsebuje lastnosti ki jih proučujemo 
- Vsebuje povezave, ki nas zanimajo (kdo koga uči, kdo je na kerem predmetu, itd)
- Njegovo delovanje ustreza razmeram **v realnosti**

##### Opredelitev baze podatkov
- ANSI (1975) zahteve(1975) zahteve za bazo podatkov: 
1. Podatki so v bazi povezani in urejeni po določenem vrstnem redu
2. BP je urejena tako, da lahko podatke v njej istočasno uporablja en ali več uporabnikov
3. Isti podatki se v bazi ne ponavljajo
4. Baza podatkov je shranjena v računalniku

##### AOP (aspect oriented programming) sistem za obdelavo podatkov
- Z obdelavo podatkov: 
- Zbiramo podatke
- Vnašamo v podatke v sistem
- Spreminjamo posredujemo
- Varujemo pred izgubo in zlorabo 
[SUPB](https://www.wikiwand.com/sl/articles/Sistem_za_upravljanje_s_podatkovnimi_zbirkami] –– sistem za upravljanje podatkovnih baz (npr. Access) omogoča funkcionalno obdelavo

##### Obdelava podatkov
**Naloge funkcionalne obdelave podatkov so:**
- Zagotoviti pravilnost in ažurnost podatkov
- Sočasno nuditi podatke vsem uporabnikom brez ogrožanja celovitosti baze podatkov
- Posredovati podatke takrat, ko jih uporabniki potrebujejo
- Omogočiti vsem uporabnikom dostopnost do tistih podatkov, ki jih potrebujejo pri svojem delu
- Posredovati podatke o tem, kaj se je zgodilo (zgodovina) in o tem, kaj se lahko zgodi (napovedi)

 **Podatkovna baza je z vidika upravljanja organizirana kot:**
- **Centralizirana podatkovna baza** – celotna baza se upravlja z enim sistemom upravljanja
- **Porazdeljena podatkovna baza** – nameščena na več računalnikih na različnih lokacijah, medsebojno povezanih v omrežje, in je upravljana z več sistemi za upravljanje


*Random intermission*
Vrste spletnih strani:
- [statične][https://nsa-splet.si/splet/uvod/splet-uvod-04-vrsteStr.php#staticne]
![[Pasted image 20250916092938.png|400]]
- [aktivne spletne strani] [https://nsa-splet.si/splet/uvod/splet-uvod-04-vrsteStr.php#aktivne]
![[Pasted image 20250916092912.png|400]]
- [Dinamične spletne strani][https://nsa-splet.si/splet/uvod/splet-uvod-04-vrsteStr.php#dinamicne]
![[Pasted image 20250916092840.png|400]]

**Podatkovni model**  
Podatkovni model je strukturiran mehanizem za opis realnosti s podatki.  
Model vsebuje množico pravil, ki določajo:

- **Organizacijo podatkov** – strukturo
    
- **Operacije nad podatki**
 ![[Pasted image 20250918082037.png|400]]

##### Podatkovna analiza – Izdelava PB “od spodaj”**  
1.  Zbiranje in analiza dokumentov in ostalih podatkov: pregled vseh »nastopajočih« atributov  
2. Oblikovanje logičnega modela

##### Analiza realnega procesa**  
1. Analiza realnega procesa → globalni model  
2. Določitev »enot« (entitet), ki nastopajo v tem procesu → konceptualni model  
3. Zapis logičnega modela (glede na SUPB)  
4. Izdelava fizične podatkovne baze → fizični model - podatkovna baza naarejena na compu
![[Pasted image 20250918082458.png|400]]

##### **Konceptualni model**  
Določimo:
1. entitete
2. njihove atribute
3. razmerja (povezave) med njimi
4. števnost razmerja
Model: **E–R diagram** (Entity–Relationship = model Entiteta–Razmerje)
	**E–R model**
- Obstaja več verzij te diagram­ske tehnike
- **Prednosti:**
    - Enostavnost
    - Možnost pretvorbe v različne podatkovne modele
    - Neodvisnost od konkretnih komercialnih izvedb baz podatkov in njihovih SUPB
##### **Števnost razmerja**
- Števnost (kardinalnost) pove, koliko primerkov ene entitete nastopa v povezavi z enim primerkom druge entitete.
- Pri binarnih povezavah (v povezavi sta udeležena dva tipa entitet) poznamo 3 osnovna razmerja števnosti:
    - **1 : 1 (ena proti ena)** - vsak razred ima 1 razrednika, vsak razrednik ima 1 razred
    - **1 : N (ena proti več)** – pravzaprav ena proti ena ali več, vsak dijak je v 1 oddelku, v 1 oddelku je več dijakov
    - **N : M (več proti več)** – pravzaprav ena ali več proti ena ali več - vsak dijak ima več krožkov, v vsakem krožku je več dijakov

pogledat za nazaj kdaj je kdo bil na kerem SD 
pogledat a majo dost ur

##### Konceptualni model
**Izdelaj model E–R branja knjige**
- Imamo:
    - 2 entiteti: **oseba**, **knjiga**
    - Eno razmerje: **bere**
    - Pri entiteti _oseba_ atributa: **spol, starost**
    - Pri entiteti _knjiga_ atributa: **avtor, naslov**
- **Izdelaj model E–R izbiranja maturitetnih predmetov**
- Imamo:
    - 2 entiteti: **dijak**, **predmet**
    - Eno razmerje: **izbiranje**
    - Pri entiteti _dijak_ atributi: **ime, priimek, razred**
    - Pri entiteti _predmet_ atributi: **ime, št. ur**
    - **Števnost:** vsak dijak lahko izbere le en predmet, isti predmet pa lahko izbere več dijakov
![[Pasted image 20250918091318.png]]
tle je so še primeri v pptju (slide 30+)


##### Logični podatkovni model
**Izhodišče je razviti konceptualni model**
- V njem zajamemo vse entitete in razmerja med njimi.
- Vsako entiteto podrobno opišemo z njenimi atributi, tako da je vsaka entiteta v modelu enolično določena.
![[Pasted image 20250918091612.png|400]]

mi rabimo znat Relacijski model

##### Objektni podatkovni model
**Objektni podatkovni model**
- Pri objektno orientiranem pristopu je BP sestavljena iz množice objektov, kjer vsak objekt predstavlja neko entiteto iz realnega sveta.
- Eden od ciljev objektnega pristopa pri modeliranju podatkov je obdržati ustrezno zvezo med realnimi objekti in njihovo predstavitvijo v bazi.
- Pri klasičnih modelih je ta zveza zabrisana.
##### Relacijski podatkovni model
**Relacijski podatkovni model – lastnosti**
- Formalno je definiran in osnovan na matematičnih strukturah – relacijah.
- Ne vsebuje elementov fizičnega shranjevanja podatkov, s čimer je zagotovljena podatkovna neodvisnost.
- Relacije so predstavljive s tabelami, ki so človeku dobro razumljive.
- Vsaka entitetna množica je predstavljena z eno ali več matematičnimi relacijami = **tabelami**.
relacije v mat so +, -, =, * , ...
- Stolpci v tabeli (relaciji) predstavljajo **atribute entitetne množice**.
- Vrstice predstavljajo **primerke entitetne množice** (zapis / record).
- Povezave med relacijami **niso vnaprej določene in vgrajene v strukturo** (kot pri hierarhični ali mrežni strukturi).
- Vzpostavijo se v skladu s trenutnimi informacijskimi potrebami.
![[Pasted image 20250918092650.png|400]]
**Terminologija relacijskega modela**
- **Relacijska shema** je naslovna vrstica tabele.
- Vsak atribut ima svojo **domeno** – zalogo vrednosti.
- Primer: atribut _starost_ pri entiteti _Najstnik_ lahko zavzame vrednosti med 11 in 19.
- Atribut _spol_ lahko zavzame vrednosti _m_ ali _ž_.
- **Ključ** – primarni ključ (lahko pa tudi sekundarni ali tuji ključ).
 ![[Pasted image 20250918092818.png|400]]
- spet primeri za to v pptju slide 43
- tanka povezava - 

microsoft baze thing?
	quick sort?

kaj je indeksiranje rabs vedn, kaj dosezem z indeksiranjem
(telefonske številke)


To je nek thing v unmu accessu  ki basically nardi da se izpiše ko runnaš sam to kar se začne na opra- 
![[Pasted image 20250930084036.png]]

access vspostavi referenčno integriteto, kaskadno posodabljanje polj v relaciji, kaskadno brisanje polj v relaciji


splet. uč. naloge za pripravo na test 21. bo zihr