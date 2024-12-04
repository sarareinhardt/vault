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
    - **Kopica (heap)**: Dinamično dodeljen pomnilnik za spremenljivke, ki so dodeljene s funkcijami, kot sta `malloc` ali `calloc`.
    - **Sklad (stack)**: Pomnilnik za lokalne spremenljivke in klice funkcij. dinamičen, avtomatičen, 
- **Diagram**:
    - Prikaz hierarhije pomnilnika s primeri: kje so spremenljivke shranjene glede na njihovo deklaracijo.