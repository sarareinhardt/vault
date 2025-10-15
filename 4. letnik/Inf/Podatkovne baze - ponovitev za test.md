![[Podatkovne_baze.pdf]]
Vprašanja za ponavljanje poglavja podatkovne baze
1. Čemu služi informacijski sistem?
a. Navedi in predstavi elemente IS!
 - Strojna oprema 
- Omrežje
- Programska oprema
- Podatkovna baza
- Postopki in metode
- Ljudje
b. Kakšne so funkcije (naloge) IS?
-  zbiranje podatkov,
- hranjenje podatkov,
- obdelava podatkov,
- varovanje podatkov,
- posredovanje podatkov uporabnikom

c. Kako naj bi se »vedel« idealni IS?
	Idealen IS posreduje prave podatke ob pravem času pravim ljudem z minimalnimi stroški
2. Kakšne so naloge (funkcionalne) sistema za upravljanje podatkovnih baz
(SUPB npr. Access-a)?
- Z obdelavo podatkov: 
- Zbiramo podatke
- Vnašamo v podatke v sistem
- Spreminjamo posredujemo
- Varujemo pred izgubo in zlorabo 
[SUPB](https://www.wikiwand.com/sl/articles/Sistem_za_upravljanje_s_podatkovnimi_zbirkami] –– sistem za upravljanje podatkovnih baz (npr. Access) omogoča funkcionalno obdelavo
2. **Navedi ANSI zahteve za podatkovno bazo in predstavi, zakaj se podatki v**
PB ne smejo ponavljati!
- ANSI (1975) zahteve(1975) zahteve za bazo podatkov: 
	1. Podatki so v bazi povezani in urejeni po določenem vrstnem redu
	2. BP je urejena tako, da lahko podatke v njej istočasno uporablja en ali več uporabnikov
	3. Isti podatki se v bazi ne ponavljajo
	4. Baza podatkov je shranjena v računalniku
	Podatki se ne smejo ponavljati, ker če iščemo podatek ljudi z neko lastnostje bomo dobili 2x večjo število kot je res
2. **V čem je razlika med centralizirano in porazdeljeno PB?**
	- **Centralizirana podatkovna baza** – celotna baza se upravlja z enim sistemom upravljanja
	- **Porazdeljena podatkovna baza** – nameščena na več računalnikih na različnih lokacijah, medsebojno povezanih v omrežje, in je upravljana z več sistemi za upravljanje
3. **Kakšna je razlika med realnim svetom (npr. nekim podjetjem) in modelom**
**realnosti?**
4. Kakšna je razlika med globalnim in konceptualnim modelom?
5. Predstavi model ER – kakšne vrste modela je to?
a. Kaj predstavlja: entiteta, atribut, razmerje, števnost?
6. V čem je razlika med logičnim in konceptualnim modelom?
7. Kaj je entiteta in kaj entitetni tip in kaj entitetna množica?
8. Kakšen podatkovni tip je lahko atribut?
a. Zakaj je treba opredeliti podatkovni tip atributa?
9. Kako so predstavljeni posamezni elementi modela ER v relacijskem
podatkovnem modelu?
10. Kaj je primarni ključ? (Čemu služi?)
11. Kaj je tuji ključ?
12. Kako urejamo podatke v tabelah?
13. Navedi osnovne funkcije, ki jih izvajamo nad podatki s pomočjo SUPB!
14. V podatkovni bazi dijakov Gimnazije Vič je entiteta Dijak opredeljena z
atributi: matična_številka, ime_dijaka, priimek_dijaka, naslov, pošta in
letnik.
Kateri atribut je primeren za primarni ključ?
15. V podatkovni bazi Merkurja je entiteta Artikel opredeljena z atributi:
evidenčna_številka, ime_artikla, skupina_artikla, dobavitelj_artikla. Kateri
atribut je primeren za primarni ključ?
16. Izdelaj model ER za primer:
V podjetju InVinoVeritas prodajajo buteljčno vino. Podjetje ima pod svojim
okriljem več kleti (prodajaln), ki imajo vsaka svoj naziv, številko in naslov.
Podjetje odkupuje buteljke od različnih proizvajalcev, ki lahko prodajajo
različna vina. Vsaka buteljka ima svoj naziv, pridelovalca, rajon, okoliš,
državo, stopnjo alkohola in druge
2
podatke.
Hranijo podatke o nakupih in prodajah posameznih vin.
17. Izdelaj model ER za primer:
Nek kraj želi informatizirati svojo turistično ponudbo. V ta namen želijo imeti
podatkovno bazo, ki bo vsebovala podatke o turističnih prenočitvenih
zmogljivostih. Prenočišča ponujajo posamezniki in podjetja, ki imajo več sob,
ki so različno opremljena (A,B, C kategorija). Prenočišče ima lahko tudi
dodatno ponudbo, kot je savna, bazen, jahanje, sprehajalne poti itd. Za vsako
prenočevanje shranjujejo tudi podatke o gostih.
18. Izdelaj model ER za primer:
Vodnogospodarsko podjetje želi svoje poslovanje računalniško podpreti.
Želijo voditi seznam svojih vodnih virov (kje se nahaja, kolikšna je kapaciteta).
Vsak vodni vir enkrat dnevno kontrolirajo glede kakovosti. Podatke želijo
shranjevati (stopnja onesnaženosti, vsebnost trdih delcev, vsebnost nitritov,
kdo je analizo opravil itd.).
Prav tako vodijo seznam rek in stopnjo onesnaženosti. Tudi reke kontrolirajo
glede kakovosti, vendar le enkrat tedensko.
Želijo voditi tudi seznam glavnih onesnaževalcev, ki delujejo na območju
podjetja. Želijo vedeti, katere vodne vire (in tudi reke, potoke...) onesnažujejo
in s čim.
Vsako leto organizirajo razne čistilne akcije, v katerih očistijo določena
obrežja rek in potokov.
Želeli bi shranjevati seznam prostovoljcev, da bi jih lahko obveščali o akcijah.
19. Izdelaj model ER za primer:
V podjetju želijo informatizirati svojo veleprodajo sadja in zelenjave. V ta
namen želijo shranjevati podatke o svojih dobaviteljih (naslov, naziv...). Želijo
imeti pregled nad tem, kaj jim kateri dobavitelj dostavlja (kaj vse prideluje) in
po kakšni ceni. Ker se ukvarjajo s hitro pokvarljivim blagom, želijo imeti
nadzor nad pošiljkami - do kdaj je katera še uporabna.
Seveda ima podjetje tudi svoje odjemalce, ki kupujejo izdelke. Ob nakupu jim
izstavijo račun - boljše stranke imajo npr. 40-dnevni rok plačila, druge pa 30,
15, 8, ali pa morajo plačati takoj.
20. Povezava med podatkom in informacijo je v tem, da
a) podatke ustvarimo na osnovi informacije v skladu s svojim predznanjem
b) si informacijo ustvarimo na osnovi podatkov v skladu s svojim predznanjem
c) podatki vsebujejo informacijo
d) podatki so sestavljeni iz informacije in predznanja
21. V podatkovni bazi dijakov Gimnazije Vič je entiteta Dijak opredeljena z
atributi: matična_številka, ime_dijaka, priimek_dijaka, naslov, pošta in
letnik.
Kateri atribut je primeren za primarni ključ?
3
22. Kako se različne entitete med seboj razlikujejo?
a) glede na različne atribute
b) glede na vrednosti atributov
c) glede na vrednosti različnih atributov
d) glede na število ovrednotenih atributov
23. Navedi osnovne elemente relacijskega podatkovnega modela