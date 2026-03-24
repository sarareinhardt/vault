Lin. f.
![[Pasted image 20260115191946.png]]


![[Pasted image 20260116180925.png]]
what presecisca help


![[Pasted image 20260118205355.png]]

Verjetnost vs. ostale naloge
Vprašanje: 1. zakaj se delamo, da so kocke različne in 2. zakaj pri B ne množim še s 3
![[Pasted image 20260317163839.png]]1. To je verjetno najbolj pogosto vprašanje pri verjetnosti! Odgovor je morda presenetljiv, a zelo pomemben: Kocke moramo vedno obravnavati, kot da so ločljive (različne), tudi če jih vržemo hkrati.

Zakaj? Poglejva na preprostem primeru z dvema kockama. Če bi kocke bile nerazločljive, bi bil izid {1,2}{1,2} (pade ena in dva) enako verjeten kot {1,1}{1,1}. Pa v resnici ni!

V naravi se izid {1,2}{1,2} zgodi dvakrat pogosteje (lahko pade 1−21−2 ali 2−12−1), medtem ko se {1,1}{1,1} zgodi samo na en način. Če bi uporabili kombinacije (kjer vrstni red ni pomemben), bi vsem tem dogodkom pripisali isto verjetnost, kar bi nas pripeljalo do napačnega rezultata.

Tukaj sta glavna razloga, zakaj v imenovalcu uporabljamo variacije (6⋅6⋅6=2166⋅6⋅6=216):

1. Enakoverjetnost izidov: Klasična definicija verjetnosti P(A)=mnP(A)=nm​ deluje le, če so vsi osnovni izidi nn enako verjetni. Vseh 216216 variacij (npr. 1−1−2,1−2−1,2−1−1…1−1−2,1−2−1,2−1−1…) ima isto možnost, da se zgodi. Če bi gledali kombinacije, pa izid "tri enice" ne bi bil enako verjeten kot izid "ena, dve, tri".
2. Abstraktna ločljivost: Tudi če so kocke v tvoji roki popolnoma enake, jih vesolje "loči" po tem, kje v prostoru se nahajajo ali v kakšnem vrstnem redu se ustavijo. Zato si jih vedno predstavljamo kot rdečo, modro in zeleno kocko (kot si že nekdo pravilno dopisal na tvojem listu z opombo: _"misli kot 3 kocke različnih barv"_).

Povzetek: Čeprav jih vržeš hkrati, jih v matematiki obravnavaj, kot da jih mečeš zaporedoma. To ti zagotavlja, da bo tvoj imenovalec sestavljen iz enako verjetnih dogodkov.

Na tvojem listu je naloga rešena popolnoma pravilno prav zato, ker so upoštevali vrstni red (tisti 3!3! pri vsoti 66 in tisto seštevanje možnosti pri dogodku A).




2. Ko te tri številke zmnožiš (53=12553=125), avtomatsko zajameš vse možne kombinacije števil od 1 do 5 na vseh treh kockah. Na primer, v teh 125125 možnostih so že všteti vsi vrstni redi, kot so:

- (1,2,3)(1,2,3)
- (2,1,3)(2,1,3)
- (3,2,1)(3,2,1)
- ... in tako naprej.

Zakaj torej ne množimo s 3? Ker tukaj nimaš "fiksiranega" števila, ki bi mu določal mesto (kot si to naredil pri dogodku A, kjer si rekel: "šestica je na prvem mestu, na ostalih dveh pa ne"). Pri 5⋅5⋅55⋅5⋅5 so vsa tri mesta "enakovredna" in prosta za katerokoli število od 1 do 5.


( oz ful poenostavljeno če maš 3 iste ne množiš ker že maš vse možne ker je za iste sete št ok da se pojavijo na vseh 3 mestih)


razlaga podobne stvari za drugo nalogo in zakaj tu tega ne delamo 
![[Pasted image 20260317164646.png]]
pogovor z astra AI in moja caveman brain razlaga:
![[Pasted image 20260317164631.png]]
tukaj točno zato delaš z variacijami in ne s kombinacijami
![[Pasted image 20260317170957.png]]