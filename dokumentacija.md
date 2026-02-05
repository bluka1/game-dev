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
Opis temeljne mehanike vožnje.

### 5.2 Upravljanje i kontrole
- Tipkovnica
- Kontroler
- Volan i pedale (opcionalno)

### 5.3 Sustav umora
Opis kako se umor simulira unutar igre.

### 5.4 Distrakcijski događaji
Detaljan opis svih vrsta događaja koji testiraju pažnju.

### 5.5 Pravila igre
Što je dopušteno, što nije, kada dolazi do greške.

---

## 6. Scenariji igranja

### 6.1 Scenarij: monotona vožnja
Opis tijeka scenarija.

### 6.2 Scenarij: noćna vožnja
Opis tijeka scenarija.

### 6.3 Scenarij: gradska vožnja
Opis tijeka scenarija.

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
Opis glavnih ekrana.

### 9.2 HUD elementi
Opis elemenata na zaslonu tijekom vožnje.

### 9.3 Wireframe prikazi
Mjesto za skice i ilustracije.

---

## 10. Dijagrami

### 10.1 Dijagram toka igre
Opis toka igre (uz ilustraciju).

### 10.2 Arhitektura sustava
Blok-dijagram sustava igre i vanjskog AI sustava.

---

## 11. Svijet igre

### 11.1 Okruženja
- Grad
- Autocesta
- Noćni uvjeti

### 11.2 Vremenski uvjeti
Opis vremenskih promjena.

---

## 12. Popis medija

### 12.1 Grafički elementi
### 12.2 Audio elementi
### 12.3 Animacije

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
