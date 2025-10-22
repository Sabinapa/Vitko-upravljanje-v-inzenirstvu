# VAJA 3 

## Skupinski del - Navodila – Value Stream Mapping (VSM): Analiza procesov

### Sceneraij vaje
Izdelava 3D-tiskanega prototipa
V laboratoriju za biomedicinsko inženirstvo raziskovalec pripravi 3D model individualiziranega implantata. Po končanem modeliranju mora načrt poslati vodji laboratorija v pregled in odobritev, kar običajno traja nekaj ur. Ko prejme dovoljenje, pripravi tiskalnik in material, nastavi parametre in zažene tisk. Ker je tiskalnik pogosto zaseden, mora počakati, da se zaključijo prejšnji projekti. Po tisku mora model nekaj časa hladiti, nato odstraniti podporne strukture. Kontrolor kakovosti preveri površino in dimenzije, pogosto odkrije nepravilnosti in zahteva ponoven tisk. Ko je model ustrezen, ga raziskovalec označi in zabeleži v laboratorijski dokumentaciji.

Skupinsko delo na primeru iz Vaje 1. Detaljnejši opis primera je predstavljen v datoteki v e-učilnici.

Navodila
* Ustvarite Current State Value Stream Map (lističi)
* Pripravite tabelo na osnovi predloge za VSM (e-učilnica).

Za vsak opis procesa:
1. Določite meje procesa (kje se začne in konča).
2. Razdelite opis na posamezne aktivnosti.
3. Označite, katere aktivnosti dodajajo vrednost (VA) in katere ne (NVA).
4. Ocenite čase izvajanja in čakanja.

* Predlagajte Future State Map s Kaizen izboljšavami.

## Posamezni del invidualno delo 

Po izvedeni analizi procesov in izdelavi VSM pripravite kvantitativno predstavitev rezultatov na osnovi podatkov, ki jih pripravite v točki A (lahko so izmišljeni). Vaš cilj je jasno in pregledno prikazati glavne značilnosti procesa, ugotoviti kjer nastajajo izgube (waste) ter utemeljiti učinek predlaganih izboljšav. 

A) Za svoj primer samostojno pripravite bazo podatkov v Excelu (Iteracija = ID primera (vsaka iteracija vključuje vse korake iz VSM (št. Korakov=št vrstic v bazi)), Korak, Vloga (kdo opravlja), Trajanje_h, Cakanje_h, Tip_aktivnosti (VA / NVA), Napake). Vsebuje naj vsaj 10 iteracij/ID


B)	PYTHON: Pripravite več različnih grafov, ki skupaj prikažejo najpomembnejše ugotovitve iz vaše analize. Ne izbirajte tipov grafov po navodilih – sami se odločite, kateri prikaz je najprimernejši. Pomembno je, da vsak graf odgovarja na jasno zastavljeno vprašanje.
Predlagane vsebine za posamezne grafe:
1.	Porazdelitev časa po korakih procesa
•	prikažite, kateri koraki trajajo najdlje in kjer se kopiči večina časa v procesu.
•	vključite tako čas izvajanja kot čas čakanja.
2.	Delež aktivnosti, ki dodajajo vrednost (VA) v primerjavi z NVA in NNVA
•	prikažite strukturo procesa po vrsti aktivnosti.
•	interpretirajte, kolikšen del procesa dejansko ustvarja vrednost.
3.	Analiza čakanja (waiting time)
•	prikažite skupni in povprečni čas čakanja po korakih ali vlogah.
•	interpretirajte, kje v procesu se pojavljajo največje zastoje.
4.	Napake ali ponovitve (rework)
•	prikažite, pri katerih korakih ali vlogah se pojavlja največ napak.
•	interpretirajte, ali obstaja povezava med dolžino trajanja in številom napak.
5.	Skupni čas procesa po iteracijah
•	prikažite, kako se skupni čas spreminja skozi ponovitve (npr. učinek učenja, standardizacije ali Kaizen izboljšav).
6.	Primerjava med vlogami
•	prikažite, kateri delež časa (ali čakanja) odpade na posamezno vlogo v procesu.
•	interpretirajte, ali so obremenitve uravnotežene ali ne.
7.	Skupna učinkovitost procesa
•	prikažite, kako se skupni Lead Time deli na čas z dodano vrednostjo (VA) in brez dodane vrednosti (NVA/NNVA).
•	interpretirajte potencial prihranka časa, če bi se NVA del odpravil.

Vsak graf mora biti naslovljen, imeti označene osi in legendo, ter pod njim kratek opis (2–3 stavke), ki pojasni, kaj prikazuje in kaj iz njega sklepate.

C)	Tabelarična predstavitev podatkov
Prevrite porazdelitev podatkov in pripravite opisno tabelo (izvoz v .csv) z uporabo knjižnic pandas, matplotlib in scipy.stats.

1. Preverite porazdelitev glavnih numeričnih spremenljivk
•	Spremenljivke: Trajanje_h, Cakanje_h, Napake.
•	Za vsako spremenljivko:
o	narišite histogram in boxplot,
o	uporabite Shapiro–Wilk test (scipy.stats.shapiro) in interpretirajte rezultat:
	če je p ≥ 0.05 → porazdelitev je približno normalna,
	če je p < 0.05 → ni normalna, zato uporabite mediane in kvartile.

2. Izračunajte opisno statistiko
Za vsako spremenljivko:
•	če je normalna: mean ± standard deviation
•	če ni normalna: median (Q1–Q3)
•	minimum – maksimum

3. Za nominalne spremenljivke (npr. Tip aktivnosti, Vloga) vedno prikažite število in delež [n (%)]. 
Če prikazujete podatke po iteracijah ali vlogah, ločite rezultate po skupinah in jasno označite stolpce.
Primer tabele: 
Spremenljivka	Opisna statistika	Min - Max	Enota
Trajanje_h	4.2 ± 1.1		h
Čakanje_h	6.5 (3.0–9.0)	0 - 12	h
Tip aktivnosti: VA	48 (53%)		
Tip aktivnosti: NVA	29 (32%)		
Tip aktivnosti: NNVA	13 (15%)		

4. Interpretacija
V kratkem besedilu (do ½ strani) interpretirajte:
•	katere aktivnosti ali vloge predstavljajo največji delež časa in čakanja,
•	kjer se pojavljajo največje izgube,
•	kakšna je razlika med VA in NVA časom,
•	ter katere izboljšave bi po vašem mnenju imele največji vpliv na učinkovitost procesa.


