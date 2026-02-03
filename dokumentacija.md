# Dokument dizajna igre

## Podaci o projektu
- Naziv igre:
- Projekt:
- Fakultet:
- Kolegij:
- Mentor:
- Autori:
- Verzija dokumenta:
- Datum:

---

## Povijest verzija dokumenta
| Verzija | Datum | Autor | Opis promjene |
|-------|-------|-------|---------------|
| 0.1   |       |       | Početna verzija dokumenta |

---

## 1. Uvod

### 1.1 Svrha dokumenta
Opisati svrhu ovog dokumenta dizajna igre, njegovu ulogu u razvoju projekta te kome je namijenjen.

### 1.2 Povezanost s istraživačkim projektom
Opis kako se igra koristi kao simulacijsko okruženje unutar šireg istraživačkog projekta.
Naglasiti da AI sustav nije dio ovog rada.

### 1.3 Opseg dokumenta
Što dokument pokriva, a što je izvan njegovog opsega.

---

## 2. Vizija igre

### 2.1 Opis vizije
Sažet, ali jasan opis ideje igre (cca 300–500 riječi).

### 2.2 Game logline
Jedna rečenica koja opisuje igru.

### 2.3 Jedinstvenost igre
Po čemu se ova igra razlikuje od postojećih simulacija vožnje.

### 2.4 Look and feel
Vizualni i atmosferski dojam igre.

---

## 3. Ciljana publika i platforme

### 3.1 Ciljana publika
Opis korisnika (npr. studenti, vozači, akademska zajednica).

### 3.2 Platforme
- PC (primarna platforma)
- Ostale moguće platforme (opcionalno)

### 3.3 Hardverski zahtjevi
- Minimalni
- Preporučeni

---

## 4. Opći opis igre

### 4.1 Žanr igre
Opis žanra i podžanra.

### 4.2 Način igranja
Single-player, real-time simulacija.

### 4.3 Ciljevi igrača
Što igrač pokušava postići tijekom igranja.

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
Opis svrhe korištenja web kamere.

### 7.2 Podaci koje igra prikuplja
Popis svih podataka koje igra šalje vanjskom sustavu.

### 7.3 Granice sustava
Naglasiti da igra ne analizira podatke, već ih samo prikuplja.

---

## 8. Sustav upozorenja

Sustav upozorenja ima cilj pravovremeno obavještavati korisnika o smanjenoj razini koncentracije ili pojavi umora tijekom igranja.

Njegova je uloga povećati sigurnost i svijest korisnika, bez narušavanja korisničkog iskustva.

Upozorenja su dizajnirana tako da budu jasno uočljiva, ali nenametljiva, te prilagodljiva različitim situacijama.

Sustav podržava više vrsta upozorenja kako bi se osigurala učinkovita komunikacija s korisnikom.

### 8.1 Vrste upozorenja

#### 8.1.1 Vizualna upozorenja

Vizualna upozorenja prikazuju se na ekranu u obliku jasno prepoznatljivih grafičkih elemenata i promjena u korisničkom sučelju. Njihova je svrha diskretno, ali učinkovito skrenuti pažnju korisniku bez korištenja zvuka. Ova vrsta upozorenja posebno je korisna u situacijama gdje zvuk nije poželjan ili treba biti ograničen, ali se može koristiti i u kombinaciji s drugim vrstama upozorenja.

Primjeri vizualnih upozorenja u igri uključuju:
- promjenu boje rubova ekrana (npr. postupno crvenilo ili zatamnjenje)
- pojavu ikone upozorenja na HUD-u (npr. simbol oka ili umora)
- kratku tekstualnu poruku ili obavijest na ekranu
- blago zamućenje slike ili smanjenje kontrasta kako bi se simulirao pad koncentracije
- treperenje ili pulsiranje određenih elemenata korisničkog sučelja

#### 8.1.2 Zvučna upozorenja

Zvučna upozorenja koriste kratke zvučne signale ili tonove kako bi brzo privukla pažnju korisnika. Ova vrsta upozorenja osobito je korisna u situacijama kada vizualni elementi mogu proći nezapaženo, primjerice kada je korisnik fokusiran na središnji dio ekrana ili ne primjećuje promjene u sučelju.

Zvučna upozorenja u igri mogu uključivati:
- kratki upozoravajući zvučni signal
- ton sličan alarmu ili obavijesti u vozilu
- suptilan, ali ponavljajući zvuk koji signalizira smanjenje koncentracije

Zvučni signali dizajnirani su tako da ne budu agresivni, već informativni, te da ne narušavaju ukupni doživljaj igre.

#### 8.1.3 Kombinirana upozorenja

Kombinirana upozorenja predstavljaju istovremenu primjenu vizualnih i zvučnih elemenata te osiguravaju najvišu razinu uočljivosti. Koriste se u kritičnim situacijama kada je potrebno odmah upozoriti korisnika i potaknuti ga na što bržu reakciju.

U kombiniranim upozorenjima, vizualni elementi (npr. promjena boje ekrana ili HUD upozorenje) sinkronizirani su sa zvučnim signalom, čime se povećava vjerojatnost da će korisnik primijetiti upozorenje i pravovremeno reagirati.

### 8.2 Razine upozorenja

Sustav upozorenja podijeljen je u više razina, ovisno o stupnju smanjenja koncentracije ili razini umora detektirane tijekom igranja. Razine upozorenja omogućuju postupno i prilagodljivo reagiranje sustava, čime se izbjegava naglo ili nepotrebno ometanje korisnika, dok se u kritičnim situacijama osigurava brza i jasna reakcija.

#### 8.2.1 Niska razina upozorenja

Niska razina upozorenja aktivira se pri blagom padu koncentracije. Cilj ove razine je diskretno upozoriti korisnika bez značajnijeg prekidanja tijeka igre.

U ovoj razini koriste se prvenstveno suptilna vizualna upozorenja, poput blage promjene boje korisničkog sučelja, pojave male ikone upozorenja na HUD-u ili kratke nenametljive poruke. Zvučna upozorenja u ovoj fazi uglavnom se ne koriste ili su vrlo blaga, ovisno o postavkama igre.

#### 8.2.2 Srednja razina upozorenja

Srednja razina upozorenja aktivira se kada sustav detektira kontinuirani ili izraženiji pad koncentracije. Ova razina ima za cilj jasno skrenuti pažnju korisniku i potaknuti ga na svjesniju reakciju.

U ovoj fazi koriste se izraženija vizualna upozorenja, poput pulsiranja rubova ekrana, vidljivijih HUD indikatora ili kratkih tekstualnih obavijesti. Po potrebi se uvode i zvučni signali umjerenog intenziteta, čime se povećava uočljivost upozorenja bez narušavanja doživljaja igre.

#### 8.2.3 Visoka (kritična) razina upozorenja

Visoka razina upozorenja aktivira se u situacijama kada je detektirana značajna razina umora ili ozbiljan pad koncentracije koji može negativno utjecati na uspješnost ili sigurnost korisnika.

Ova razina koristi kombinirana upozorenja koja uključuju izražene vizualne efekte (npr. promjena boje cijelog ekrana, jasne poruke upozorenja ili intenzivni HUD elementi) zajedno sa zvučnim signalima visoke uočljivosti. Cilj ove razine je odmah privući pažnju korisnika i potaknuti ga na brzu reakciju, poput pauziranja igre ili promjene načina igranja.


### 8.3 Reakcija sustava na upozorenja

Reakcija sustava na upozorenja ovisi o aktivnoj razini upozorenja te je dizajnirana tako da postupno utječe na tijek igre, bez naglog prekida korisničkog iskustva. Sustav reagira dinamički, prilagođavajući se stanju korisnika i kontekstu igre.

Kod niske razine upozorenja, sustav ne mijenja mehanike igre, već korisniku pruža isključivo informativni signal. Igra se nastavlja neometano, a upozorenje služi kao blagi podsjetnik na smanjenje koncentracije.

Kod srednje razine upozorenja, sustav može dodatno naglasiti upozorenje te potaknuti korisnika na svjesniju reakciju. U ovoj fazi moguće je privremeno pojačavanje vizualnih ili zvučnih indikatora, kao i prikaz savjeta ili kratke poruke koja korisnika upozorava na potrebu za povećanom pažnjom ili kratkim odmorom.

Kod visoke (kritične) razine upozorenja, sustav može aktivno intervenirati u tijek igre. To može uključivati ali i ne mora automatsko pauziranje igre, jasno istaknutu poruku upozorenja ili preporuku za prekid igre. Cilj ove reakcije nije kažnjavanje korisnika, već zaštita korisničkog iskustva i simulacija realnih posljedica smanjene koncentracije.

Nakon reakcije sustava, korisniku se omogućuje nastavak igranja, prilagodba postavki upozorenja ili prekid igre, ovisno o vlastitoj procjeni i preporukama sustava.

### 8.4 Prilagodba sustava upozorenja korisniku

Sustav upozorenja omogućuje prilagodbu prema preferencijama korisnika kako bi se osiguralo optimalno korisničko iskustvo bez nepotrebnog ometanja. Cilj prilagodbe je omogućiti korisniku kontrolu nad načinom i intenzitetom upozorenja, uz zadržavanje osnovne funkcionalnosti sustava.

Korisnik može prilagoditi vrstu upozorenja koje želi primati, uključujući mogućnost uključivanja ili isključivanja vizualnih i zvučnih upozorenja. Također je moguće prilagoditi intenzitet zvučnih signala, učestalost pojavljivanja upozorenja te razinu njihove izraženosti unutar korisničkog sučelja.

Sustav omogućuje i prilagodbu osjetljivosti upozorenja, čime korisnik može utjecati na pragove pri kojima se pojedine razine upozorenja aktiviraju. Na taj način sustav se može prilagoditi različitim stilovima igranja i individualnim razlikama među korisnicima.

Sve prilagodbe dostupne su kroz izbornik postavki igre te se primjenjuju u stvarnom vremenu, bez potrebe za ponovnim pokretanjem igre. Time se osigurava fleksibilnost sustava uz zadržavanje jasnoće i konzistentnosti upozorenja tijekom igranja.

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
