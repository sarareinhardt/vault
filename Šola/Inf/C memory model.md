### **1. Uvod (2 minuti)**

- **vprašanje**:
    - _"Kaj se v resnici zgodi v pomnilniku, ko v jeziku C deklarirate spremenljivko? Kaj naredi računalnik z informacijami ki mu jih damo, kam jih shranjuje..."_
    - :3
### **2. Razporeditev pomnilnika v jeziku C (3 minute)**

- **Pomnilniški segmenti (memory segments)**:
    - **Segment kode (text/code segment)**: Shrani kodo ki se trenutno izvaja - navodila programa prevedena v strojno kodo
    - **Podatkovni segment (data segment BSS)**: Inicializirane globalne in statične spremenljivke.
    - **Neinicializirane globalne in statične spremenljivke.
    - **Kopica (heap)**: Dinamičen, 
    - Heap – začasen, avtomatičen, hitrejši, določena, manjša velikost od stacka
    - Stack (Kopica) – dolgoročen, ni avtomatičen, počasnejši


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
        - Ko določimo vrednost neki spremenljivki se ta shrani kot pointer na prvi bite te vrednosti v spominu
	        - podatkovni tipi se v spominu nahajajo na poziciji, ki je večkratnik njegove velikosti, za optimizacijo procesov (procesor ve, da se podatek lahko nahaja samo na mestu, ki je večkratnik njegove velikosti)
		        - vmes dobimo padding, ki poskrbi za pravilno poravnavo nadaljnih podatkov. Notri lahko nima nič ali pa neko naključno vrednost, ki je bila prej tam.
- **Sestavljeni tipi**:
    - **Tabele (arrays)**: Shranjene v zaporednem pomnilniku.
        - Primer: deklariramo tabelo `int arr[5];` ta porabi `5 * sizeof(int)` bajtov na skladu.
        - 
    - **Strukture (structs)**:
        - Več zaporedno shranjenih različnih (lahko sicer tudi enakih) podatkovnih tipov shranjenih znotraj ene strukture/objekta
    - **Kazalci (pointers)**:
        - Shranjujejo naslove v pomnilniku, običajno 4 bajte (32-bitni sistemi) ali 8 bajtov (64-bitni sistemi).
        - Dinamično dodeljeni kazalci uporabljajo kopico (`malloc` ali podobno).
- **Obseg in življenjska doba**:
    - **Globalne/statične spremenljivke**: Shranjene v podatkovnem ali BSS segmentu.
    - **Lokalne spremenljivke**: Shranjene na skladu (stack).
    - **Dinamične spremenljivke**: Dodeljene na kopici (heap) 
	    - spremenljivke, ki jim tekom programa dodelimo vrednost, na začetku samo določimo prostor, ki ga bo porabila
			- int * ptr = malloc(sizeof(int)); 
			- * ptr = 10; 
			- free(ptr);

---

### **4. Pogoste težave in nasveti za odpravljanje napak (4 minute)**

- **Pogoste napake**:
    - Ohlapni kazalci (dangeling pointers)
	    - Kazalec, ki kaže na prostor ki je bil že sproščen s free()
    - Dvojna sprostitev (double free)
	    - 2x sprostiš prostor s free()
    - Prelivanje medpomnilnika(Buffer overflow)
	    - poskusiš pisati izven meje dodeljenega pomnilnika (napišeš več podatkov kot si dodelil prostora)
	    - Buffer (ali medpomnilnik) je začasni pomnilniški prostor, ki se uporablja za shranjevanje podatkov med prenosom iz enega mesta v drugo.
    - Uhajanje pomnilnika (Memory leak)
	    - Dinamično dodeljeni pomnilnik se ne sprosti z `free`, kar povzroči, da ostane dodeljen, vendar nedostopen.
	    - torej mi (npr znotraj neke funkcije) zapišemo nekaj v heap - dinamični polnilnik, po izvedbi funkcije pa ne sprostimo tega prostora s free. Podatki so še vedno tam shranjeni pointerja za dostop do njih pa nimamo več.
	    - **Valgrind**  - orodje za zaznavanje uhajanja pomnilnika 

---

### **5. Zaključek in vprašanja (2–3 minute)**

-
    - Razumevanje pomnilniškega modela jezika C pomaga preprečiti napake in pisati učinkovitejšo kodo.
    - Je temelj za sistemsko programiranje in aplikacije, kjer je zmogljivost ključna.
