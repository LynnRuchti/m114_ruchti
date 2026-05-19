# A1 - Themen aus der Digitaltechnik

<img width="536" height="466" alt="image" src="https://github.com/user-attachments/assets/ebc9141a-bf26-4fb1-bcc7-d0217b858ff6" /><br>

### Lernziele:
- Wie werden binäre Zustände im der Computerarchitektur dargestellt?
- Wie werden grosse und kleine Zahlen mit Präfixen dargestellt?
- Wie werden Daten in den Speichergrössen Byte, Word, DWord und QWord abgelegt und interpretiert?
- Warum gibt es einen Überlauf?
- Wie werden binäre Werte verrechnet?
- Darstellung der und Umwandlung in die drei versch. Zahlensystemen: Bin, Dez und Hex.
- Optional: Datenübertragung auf Leitungen


## Digitale Daten
**Bit (eng. Binary Digit=Binärziffer, z.B. 100b) = Masseinheit Datenmänge digital gespeicherten/übertragenen Daten, Datenübertragungsraten werden meistens in b gerechnet(100kb/s), 2b => 2^2 Bitkombinationen = 4 Zustände von 0/1 Kombinationen** <br>
! kleiner als 1 Bit ist nicht möglich<br>

PC kennt nur 0/1, Spannung aus/ein, bei Datentrans. auf Leitungen negativ/positiv Strom (kein Strom wenn unterbrochen)<br>
| Binär |  Information(en) | Spannung (alte) Logik | Spannung moderne CPU | Strom auf der Leitung: <br> Base-T  bis 1G | Base-T 10G |
|:---:|---|---|:---:|:---:|:---:|
| **1** |  Logisch WAHR <br> (true)|  5V (TTL) <br> 3.3V (CMOS) | 0.7V - 1.5V |  +800mA  | +100mA |
| **0** |  Logisch FALSCH <br> (false) | 0V  | 0V |-800mA | -100mA |
| **(Unterbruch)** | - | - | - | 0mA | 0mA |

**Me:** <br>
- Bit/b= eine Masseinheit digitaler Daten, Dat.trans. meistens in b,
- Comtuters verstehen nur 0/1(Tabelle), also HEX


**Byte (1B=8b, 1B=2HEX-Ziffern(011'0100 = B4) = adressiert via Adressbus, 1B hat 256 Bitkombinationen(0-255), Speichergrössen werden meistens in B gerechnet(1TB)** <br>
Dat.bus. (bei 8-Bit-CPU -> 8b breit, 64-Bit-CPU -> 64b breit), jedes Byte bleibt immer adressierbar<br>
(Bsp. 8b breit => kann 256 x 1 Byte adressieren)<br>
<img width="431" height="267" alt="image" src="https://github.com/user-attachments/assets/e6667140-23c5-48be-ae05-208f29981810" /><br>

**Me:** <br>
- Byte/B= 1B=8b, meistens für Speicher(100GB), 1B hat 256 Bitkombinationen<br>

**SI-Präfixe(Système international d’unités) (10er-Systen) = Massvorsätze (k in km, m in mg)** <br>
- 10^24 → [Y] → Yotta → 1024 → 1'000'000'000'000'000'000'000'000 → Quadrillion
- 10^21 → [Z] → Zetta → 1021 → 1'000'000'000'000'000'000'000 → Trilliarde
- 10^18 → [E] → Exa  → 1'000'000'000'000'000'000 → Trillion
- 10^15 → [P] → Peta  → 1'000'000'000'000'000 → Billiarde
- 10^12 → [T] → Tera  → 1'000'000'000'000 → Billion
- 10^9 → [G] → Giga  → 1'000'000'000 → Milliarde
- 10^6 → [M] → Mega  → 1'000'000 → Million
- 10^3 → [k] → kilo → 1'000 → Tausend
- 10^0 → [-]  → 1 → Eins
- 10^-3 → [m] → milli  → 0.001 → Tausendstel
- 10^-6 → [µ] → mikro  → 0.000'001 → Millionstel
- 10^-9 → [n] → nano  → 0.000'000'001 → Milliardstel
- 10^-12 → [p] → piko  → 0.000'000'000'001 → Billionstel
- 10^-15 → [f] → femto  → 0.000'000'000'000'001 → Billiardstel
- 10^-18 → [a] → atto  → 0.000'000'000'000'000'001 → Trillionstel

**Me:** <br>
- SI-Präfixe(z.B. Mega MB, Tera TG, kilo kg), immer 1000x besser/mehr als das vorherige, wird für Masseinheiten benutzt(auch im Alltag für Liter, Gramm, Meter, ec.)<br>


**IEC-Präfixe(International Electrotechnical Commission) (Zweier-System) = verwendet für Kapazitätsangaben bei Speichermedien -> Grund: Datenspeicher mit binärer Adressierung ergeben sich Speicherkapazitäten von 2n Byte, d.h. Zweierpotenzen.** <br>
- 2^80 → [Yi] → Yobi → 1'208'925'819'614'629'174'706'176
- 2^70 → [Zi] → Zebi → 1'180'591'620'717'411'303'424
- 2^60 → [Ei] → Exbi → 1'152'921'504'606'846'976
- 2^50 → [Pi] → Pebi → 1'125'899'906'842'624
- 2^40 → [Ti] → Tebi → 1'099'511'627'776
- 2^30 → [Gi] → Gibi → 1'073'741'824
- 2^20 → [Mi] → Mebi → 1'048'576
- 2^10 → [Ki] → Kibi → 1'024
(Bsp. 1 MiB ist 1 Mebibyte oder 1'048'576 Byte (= 8'589'934'592 Bit)<br>

TTL(Transistor-Transistor-Logic)=0/1<->0V/5V<br>
Transistor=elektronisches Bauteil, das Leitungen dazwischen hat, erzeugt 0/1<br>

### Aufgabe 1
1) 2*10^-3 mm, 0,002 mm
2) 234*10^9 µl -> 234*10^9*10^-6 l -> 234'000 l
3) 3.3 ZB -> 3.3*10^21-9 GB => 3.3*10^21-9/25 -AI-> 132*10^9 Blue-Ray-Discs
4) PDF-Datei Vers. 1.7 (%PDF-1.7), es hat einige PDF-Strukturelemente
  - Dateigrösse: 220 KB (225,776 bytes)
  - Grösse auf Datenträger: 224 KB (229,376 bytes)


## Binäre Datenspeicher und ihre Grenzen
**Anzahl Bit-Kombinationen ermitteln:** 2^x (x=anzahl Bit)<br>
Anzahl Bit: Aufgerundet von (LOG y / LOG 2) (y=anzahl bKombinationen)<br>

| Speicher- grösse | Anzahl Bit | Anzahl Kombinationen | Wertebereich **Unsigned** | Wertebereich **Signed** <br> MSB* &rarr; ±|
|---|:---:|---|---|---|
| BYTE | 8 | 2<sup>8</sup> = 256 | 0 bis <br> 255 (= 2<sup>8</sup>-1) | -128 bis +127 |
| WORD | 16 | 2<sup>16</sup> = 65536 | 0 bis 65535 | -32'768 bis +32'767 |
| DWORD | 32 | 2<sup>32</sup>  | 0 bis 4’294’967’296 | -2'147'483'648 bis +2'147'483'647 |
| QWORD | 64 | 2<sup>64</sup> | 0 bis 2<sup>64</sup>-1 ≈ 1,70141·10<sup>38</sup> | -9'223'372'036'854'775'808 bis +9'223'372'036'854'775'807 |

MSB (Most Significant Bit): versendung von links nach rechts<br>
LSB (Least Significant BIt): Versendung von rechts nach links<br>
<img width="710" height="1383" alt="image" src="https://github.com/user-attachments/assets/4ce54481-481d-46c0-83c9-5b455f4f20aa" /><br>
(signed)<br>

<img width="428" height="438" alt="image" src="https://github.com/user-attachments/assets/97553bce-d3e4-483e-9252-d81f77c2f169" /><br>
(MSB=1 ist Vorzeichen "-", MSB=0 ist "+")<br>
(Datenüberfluss error: Unsig. >255, Sig. <-128 & >127

### Aufgabe 2
1) 2^32 bKombinationen 1 DWORD
2) min sig. WORD bin: 1000 0000 0000 0000 (hier vordestes bit vorzeichen/msb=1->"-"), dec: -32'768
3) max unsig. WORD bin: 1111 1111 1111 1111, dec: 65'535
4) 2^9 -> 512 bKombos
5) 2^20 -> 1'048'576 bKombos
6) 9 bStellen
7) 100-(-100) = 200 -> 200*10+1 = 2001 bKombos -> Aufrunden(LOG 2001/Log 2) = 11 Bit
8) WORD: <-32'768, >32,767, DWORD: <-2'147'483'648, >2,147,483,647
