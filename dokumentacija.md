# Dokument dizajna igre

## Podaci o projektu
- Naziv igre: Focus Drive
- Autori: Lana Kohut, Daniel Katić i Luka Batarelo
- Verzija dokumenta: 1.0
- Datum: 06.02.2026.

---

## 1. Uvod

### 1.1 Svrha dokumenta
Ovaj dokument definira dizajn i funkcionalne specifikacije simulatora vožnje namijenjenog istraživanju ljudskog umora tijekom vožnje. Služi kao vodilja developerima za implementaciju igre i timu istraživača za razumijevanje na koji način se analiziraju i prikupljaju podaci.

### 1.2 Povezanost s istraživačkim projektom
Igra je ključni alat projekta DMM (Driver Monitoring Model). Ona stvara kontrolirano, repetitivno okruženje potrebno za poticanje stanja smanjene budnosti kod ispitanika. Važno je naglasiti da je AI sustav koji analizira te podatke odvojen istraživački entitet, dok igra služi isključivo kao platforma za generiranje scenarija i prikupljanje parametara kroz igru.

### 1.3 Opseg dokumenta
Dokument obuhvaća dizajn okruženja (autoceste, noć), scenarije kroz igru, općenite opise uloge i zadatka igrača, integraciju AI modula, sustav povratnih informacija tj. upozorenja te tehničke zahtjeve i okvirne specifikacije.

---

## 2. Vizija igre

### 2.1 Opis vizije
Igra je napredni simulator sigurnosti koji simulira najopasnije aspekte dugotrajne vožnje: monotoniju i smanjenu vidljivost u teškim uvjetima. Igrač se bori s "hipnozom ceste" dok integrirani AI sustav u pozadini neprestano analizira njegovo stanje. Vizija je stvoriti simbiozu između čovjeka i stroja gdje igra reagira na biološke signale umora (npr. ako igrač predugo ne trepne ili mu glava klone, igra aktivira specifične podražaje tj. upozorenja).

### 2.2 Game logline
Inteligentni simulator vožnje koji koristi AI kako bi prepoznao i reagirao na tvoj umor u najtežim uvjetima ceste.

### 2.3 Jedinstvenost igre
Igra se ne oslanja samo na pritisak tipki, već na stvarno fiziološko stanje igrača. AI sustav prepoznaje umor prije nego što igrač napravi grešku na cesti, pretvarajući "pasivni" simulator u "aktivni" sustav zaštite.

### 2.4 Look and feel
Vizualni dojam teži čim vjernijim prikazima stvarnih uvjeta (kiša, magla, noć) koji otežavaju vožnju. Atmosfera treba uglavnom biti umirujuća, ali opasno monotona te na taj način uz vizualno teške uvjete potencirati umor vozača.

---

## 3. Ciljana publika i platforme

### 3.1 Ciljana publika
Studenti, znanstveni djelatnici, osoblje u autoškolama te svi koji vole voziti.

### 3.2 Platforme
Osobno računalo - zbog procesorske snage potrebne za istovremeno izvođenje igre i AI modela za analizu slike u stvarnom vremenu.

### 3.3 Hardverski zahtjevi
Okvirni zahtjevi:
- minimalni: CPU s 6 jezgri (zbog AI paralelizacije), 16GB RAM, HD Web kamera (30 FPS)

---

## 4. Opći opis igre

### 4.1 Žanr igre
Žanr igre je simulacija, odnosno, ozbiljna igra.

### 4.2 Način igranja
Vožnja kroz igru na računalu s naglaskom na budnost i izdržljivost u vožnji. AI sustav djeluje kao "suvozač" koji nadzire igrača.

### 4.3 Ciljevi igrača
Prevesti zadanu dionicu bez aktivacije AI alarma visoke razine, održavajući budnost uz dosadnu vožnju kroz teške ili dosadne uvjete na cesti.

---

## 5. Taktički aspekti igre (Gameplay)

### 5.1 Osnovna mehanika igre
Neovisno o odabranoj metodi upravljanja igrom, igra dozvoljava kontrolu kretanja naprijed, nazad, lijevo, desno te također omogućava detaljniju kontrolu vožnje:
- Kontrola kvačila/spojke
- Mijenjanje brzine
- Automatski/ručni pokazivač smjera
- Paljenje/gašenje prednjih i zadnjih svjetala
- Zoomirani pogled u retrovizore
- Kočenje
Ovo su osnove mehanike vožnje potrebne za simulaciju same vožnje u igri. 

### 5.2 Upravljanje i kontrole
Tipkovnica:
  
| Tipka | Akcija                                      |
|-------|---------------------------------------------|
| ⬆/W   | Vožnja naprijed                             |
| ⬇/S   | Kočenje/Vožnja unazad                       |
| ➡/D   | Skretanje desno                             |
| ⬅/A   | Skretanje lijevo                            |
| 1     | Prva brzina                                 |
| 2     | Druga brzina                                |
| 3     | Treća brzina                                |
| 4     | Četvrta brzina                              |
| 5     | Peta brzina                                 |
| 6     | Šesta brzina                                |
| 7/Q   | Pokazivač smjera ulijevo                    |
| 8/E   | Pokazivač smjera udesno                     |
| 9/F   | Paljenje/gašenje prednjih svijetala         |
| 0/B   | Paljenje/gašenje stražnjih svijetala        |
| M     | Zoomirani pogled u sve retrovizore          |
| Shift | Kvačilo                                     |



Kontroler:

| Tipka | Akcija                                      |
|-------|---------------------------------------------|
| L2    | Vožnja naprijed/unazad/kočenje              |
| L1    | Skretanje desno/lijevo                      |
| RT    | Mijenjanje brzine prema gore (ubrzavanje)   |
| LT    | Mijenjanje brzine prema dolje (usporavanje) |
| ⬅     | Pokazivač smjera ulijevo                    |
| ➡     | Pokazivač smjera udesno                     |
| ⬆     | Paljenje/gašenje prednjih svijetala          |
| ⬇     | Paljenje/gašenje stražnjih svijetala         |
| +     | Zoomirani pogled u sve retrovizore          |
| X/🔺  | Kvačilo                                     |


Volan i pedale (opcionalno)

| Tipka                  | Akcija                                      |
|------------------------|---------------------------------------------|
| Pedala lijevo          | Kvačilo                                     |
| Pedala sredina         | Kočenje                                     |
| Pedala desno           | Gas                                         |
| Y/🔺                   | Vožnja naprijed                             |
| A/X                    | Vožnja unazad                               |
| Okretanje volana desno/lijevo | Skretanje desno/lijevo          |
| RB                     | Mijenjanje brzine prema gore (ubrzavanje)   |
| LB                     | Mijenjanje brzine prema dolje (usporavanje) |
| ⬅                      | Pokazivač smjera ulijevo                    |
| ➡                      | Pokazivač smjera udesno                     |
| ⬆                      | Paljenje/gašenje prednjih svijetala          |
| ⬇                      | Paljenje/gašenje stražnjih svijetala         |
| +                      | Zoomirani pogled u sve retrovizore          |


### 5.3 Sustav umora
Umor se simulira pomoću:
- Prilikom svakog distrakcijskog događaja, igrač dobiva opciju da u kratkom roku odgovori na pitanje gdje želi usmjeriti svoju pažnju.
- Ako ne odgovori na pitanje na vrijeme, automatski se računa kao da je kliknuo da želi usmjeriti pažnju na distrakcijski događaj te se povećava mjerač umora.

### 5.4 Distrakcijski događaji
- reklame uz autocestu (neanimirane i animirane) - lako oduzimaju pažnju
- zvonjava vozačevog mobitela u autu
- kamion sa glasnom reklamom koji prolazi pored nas ili u suprotnom smjeru
- žongleri na pješačkom
- GPS krivo postavljen, daje krive upute
- protest/parada u gradu
- prolivena kava po autu i vozaču
- puno obavijesti u kratkom vremenu na mobitelu (mobitel vibrira, blješti ili zvoni)
- tjelesne distrakcije: svrbež na nekom dijelu tijela, bolovi, ukočenost vrata/ramena/leđa

### 5.5 Pravila igre
- Nije dopušteno ilegalno kretanje sa automobilom (kretanje travom, preko ograde uz cestu, po dvorištima, po kolniku), igra daje upozorenje te vraća igrača na točku prije ilegalnog skretanja
- Dopušteno je praćenje pravila prometa u stvarnom svijetu te vožnja u igri u skladu s time
- Kampanje: Igrač u svakoj kampanji ima zadatak doći od točke A do točke B bez okidanja upozorenja za umor (ili može imati dopuštena 3 upozorenja (nisko, srednje, visoko) prije nego što ga igra vrati na početak kampanje)
- Sandbox: Igrač vozi gdje god želi, ali sa istim ograničenjem umora kao i u kampanji. Razlika ovdje bi bila što igrač nakon 3 upozorenja može birati gdje će se pojaviti (spawn point)

---

## 6. Scenariji igranja

### 6.1 Scenarij: monotona vožnja
Duga vožnja autocestom (20-30 minuta real-time) sa malo vizualnih promjena uz cestu.

### 6.2 Scenarij: noćna vožnja
Vožnja slabije osvjetljenim gradom ili mjestom sa više slabije vidljivih skretanja, kružnih tokova, pješačkih prijelaza.

### 6.3 Scenarij: gradska vožnja
Vožnja sa više mogućih distrakcijskih događaja uključenih (npr žongleri, protest, prolivena kava,...)

---

## 7. Sustav praćenja korisnika

### 7.1 Uloga kamere
Kamera ne služi samo snimanju već i kao izvor podataka za AI sustav. Ona u realnom vremenu snima te se svakih npr. 50 milisekundi snimi slika za AI model koji izračunava postotak zatvorenosti očiju i frekvenciju treptanja.

### 7.2 Podaci koje igra prikuplja
Biometrija: AI detektira mikrosan tj. gledanje u prazno, zijevanje i nagib glave
Telemetrija: Odstupanje od trake (Lane Departure) sinkronizirano s detekcijom pogleda

### 7.3 Granice sustava
Kad AI prepozna kritičnu razinu umora, igra aktivira:
- vizualna upozorenja
- glasovna upozorenja

---

## 8. Sustav upozorenja

### 8.1 Vrste upozorenja
- Vizualna
- Zvučna
- Kombinirana

### 8.2 Način aktivacije upozorenja
Kako i kada se upozorenja prikazuju.

---

## 9. Korisničko sučelje (UI)

### 9.1 Pregled sučelja
Glavni ekran uključuje pozadinu, naziv igre te meni:
- Nova igra (New Game) -> Kampanja (Campaign)/Slobodno igranje (Free Play/Sandbox)
- Učitaj igru (Load Game)->Odaberi slot za učitavanje igre (Choose a slot to start playing the game)
- Postavke (Settings)->Grafika (Graphics), Audio, Kontrole (Controls), Jezik (Language)
- Izlaz (Exit)

### 9.2 HUD elementi
Na zaslonu je vidljivo prednje staklo auta sa brisačima, volan, brzinomjer, ventilatori, radio, ladica na suvozačevoj strani.
Mjenjač se pojavljuje preko radia pritiskom gumba za kvačilo+brzinu te se prikazuje ruka na mjenjaču koja povećava ili smanjuje brzinu.
Pritiskom gumba za retrovizore se prikazuju zoomirani retrovizori blizu ili na mjestima gdje se inače nalaze.
U donjem desnom kutu je vidljiv mjerač umora koji mjeri vozačev umor te se u odnosu na njega prikazuju ili ne prikazuju upozorenja.



### 9.3 Wireframe prikazi

![Zoomirana ogledala](./slike/ogledala_ilustracija.png)



---

## 10. Dijagrami

### 10.1 Dijagram toka igre
Opis toka igre (uz ilustraciju).

### 10.2 Arhitektura sustava
Blok-dijagram sustava igre i vanjskog AI sustava.

---

## 11. Svijet igre

### 11.1 Okruženja
- 4 različita grada raspoređena po težinama
- Prvi grad ima najlakšu težinu, što znači da ima najmanje događaja koji uzrokuju umor
- Drugi grad ima srednju težinu te se povećava broj događaja koji uzrokuju umor, isto se ponavlja za treći i četvrti grad
- Svaki grad uključuje: promjene iz dana u noć, različite vremenske uvjete, autocestu
- Prvi grad uključuje: noćnu vožnju, smanjeno osvjetljenje u nekim predjelima grada ili okolice grada, kišu (slabu i srednja), srednji vjetar, sunčano vrijeme, oblačno vrijeme, kiša s grmljavinom
- Drugi, treći i/ili četvrti grad uključuju: kompleksnije vremenske uvjete (snijeg, magla, poledica, jaki vjetar, jaka kiša (od koje mogu nastati poplave)), više događaja koji mogu uzrokovati umor, duže noćne vožnje i duže vožnje autocestom

### 11.2 Vremenski uvjeti
Vrijeme bi se mijenjalo u skladu sa godišnjim dobom i umjerenim klimatskim pojasom. 
Igrač bi unutar jednog dana najčešće imao više vremenskih uvjeta, ovisno gdje i koliko daleko vozi. Vrijeme bi se prilagođavalo lokaciji, godišnjem dobu te dobu dana (vizualno bi oblačno vrijeme izgledalo drugačije po noći nego po danu).


---

## 12. Popis medija

### 12.1 Grafički elementi
- Prednja unutrašnjost automobila (iz perspektive vozača)
- 4 različita grada i njihovih okolica sa svim elementima prometa (lokalne ceste, državne ceste, autoceste, drugi automobili, pješaci, prometni znakovi, semafori, pješački prijelazi, škole, autoceste, kružni tokovi,...)
- Različite zgrade (stambene, poslovne, društvene)
- vegetacija uz cestu, parkovi
- tematski parkovi (za pse, skateboard)
- Reklame uz autocestu i uz gradske ceste
- Ruke vozača na volanu
### 12.2 Audio elementi
- zvukovi prometa, pješaka kako razgovaraju (na semaforu) ili puštaju glasnu muziku
- zvuk semafora za pješake
- zvuk igračevog automobila
- zvuk kamiona koji puštaju glasne reklame
### 12.3 Animacije
- Pop-in/pop out animacija prilikom aktiviranja gumba za zoomirana ogledala
- Fade-in animacija za upozorenja
- Eksplozija zvijezdica za uspješno završen grad u svakoj kampanji

---

## 13. Tehničke specifikacije

### 13.1 Razvojno okruženje
Unity, C#.

### 13.2 Tehnička ograničenja
Performanse, kamera, rezolucije.

### 13.3 Integracija s vanjskim sustavima
Konceptualni opis komunikacije s AI sustavom.

---

## 14. Rizici i ograničenja

- Tehnički rizici
- Hardverska ograničenja
- Organizacijski rizici

---

## 15. Zaključak

Sažetak dizajna i smjer daljnjeg razvoja.
