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
Neovisno o odabranoj metodi upravljanja igrom, igra dozvoljava kontrolu kretanja naprijed, nazad, lijevo, desno te također omogućava detaljniju kontrolu vožnje:
- Kontrola kvačila/spojke
- Mijenjanje brzine
- Automatski/ručni pokazivač smjera
- Paljenje/gašenje prednjih i zadnjih svjetala
- Zoomirani pogled u retrovizore
- Kočenje
Ovo su osnove mehanike vožnje potrebne za simulaciju same vožnje u igri. 

### 5.2 Upravljanje i kontrole
- Tipkovnica:
|Tipka|Akcija|
|⬆/W|Vožnja naprijed|
|⬇/S|Kočenje/Vožnja unazad|
|➡/D|Skretanje desno|
|⬅/A|Skretanje lijevo|
|1|Prva brzina|
|2|Druga brzina|
|3|Treća brzina|
|4|Četvrta brzina|
|5|Peta brzina|
|6|Šesta brzina|
|7/Q|Pokazivač smjera ulijevo|
|8/E|Pokazivač smjera udesno|
|9/F|Paljenje/gašenje prednjih svijetala|
|0/B|Paljenje/gašenje stražnjih svijetala|
|M|Zoomirani pogled u sve retrovizore|
|Shift|Kvačilo|


- Kontroler:
|Tipka|Akcija|
|L2|Vožnja naprijed/unazad/kočenje|
|L1|Skretanje desno/lijevo|
|RT|Mijenjanje brzine prema gore (ubrzavanje)|
|LT|Mijenjanje brzine prema dolje (usporavanje)|
|⬅|Pokazivač smjera ulijevo|
|➡|Pokazivač smjera udesno|
|⬆|Paljenje/gašenje prednjih svijetala|
|⬇|Paljenje/gašenje stražnjih svijetala|
|+|Zoomirani pogled u sve retrovizore|
|X/🔺|Kvačilo|

- Volan i pedale (opcionalno)
|Tipka|Akcija|
|Pedala lijevo|Kvačilo|
|Pedala sredina|Kočenje|
|Pedala desno|Gas|
|Y/🔺|Vožnja naprijed|
|A/X|Vožnja unazad|
|Okretanje volana desno/lijevo|Skretanje desno/lijevo|
|RB|Mijenjanje brzine prema gore (ubrzavanje)|
|LB|Mijenjanje brzine prema dolje (usporavanje)|
|⬅|Pokazivač smjera ulijevo|
|➡|Pokazivač smjera udesno|
|⬆|Paljenje/gašenje prednjih svijetala|
|⬇|Paljenje/gašenje stražnjih svijetala|
|+|Zoomirani pogled u sve retrovizore|

### 5.3 Sustav umora
Umor se simulira pomoću:
- 

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
