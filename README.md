# TVC-Breakout
<img src="imgs/exp-front.jpg" width="500" alt="Expansion breakout">
## Magyar
Ez a repo olyan ny�klapok EagleCAD terveit tartalmazza, melyek a Videoton TVC sz�m�t�g�p programmodul �s fels� b�v�t�-helyeinek kivezet�seit teszik k�nnyen (k�nnyebben) el�rhet�v� hardverfejleszt�k sz�m�ra.
- _cart_ k�nyvt�r tartalmazza a programmodul forr�s file-jait, gerber file-t �s a kapcsol�si rajzot pdf-ben is.
- _exp_ k�nyvt�r tartalmazza a fels� b�v�t� forr�s file-jait, gerber file-t �s a kapcsol�si rajzot pdf-ben is. Az r2-es v�ltozat az r1-hez k�pest annyival tud t�bbet, hogy arra ker�lt egy 27C512 -es ROM foglalat is, kapcsolhat� A13-A15 vonalakkal. Az ellen�ll�sok 3# -ra lettek tervezve, hogy egyszer�bben lehessen bele LED -et tenni.
- _imgs_ k�nyvt�r a m�r elk�sz�lt ny�klapokr�l tartalmaz f�nyk�peket
- _lib_ k�nvyt�r a sz�ks�ges alkatr�sz-k�nyvt�rakat tartalmazza
- OPCION�LIS: Az exp lap r2 -es v�ltozata tartalmazhat egy 64kB -os EEPROM -ot. Ha ebb�l csak a legfels� 8kB van haszn�latban, akkor nem kell semmi m�st csin�lni a lapon. Amennyiben lapoz�s sz�ks�ges, az EEPROM az A13-A15 jeleit a lap k�v�lr�l kell megkapja (neked kell legener�lnod �s az EX_A13, EX_A14, EX_A15 illetve az /EX_CE helyeken visszahozni a jobb als� t�skesoron). Ilyenkor az A13, A14, A15 �s /CE jumperek alj�t v�gni kell �s be�ll�tani, hogy honnan �rkezzen a c�mjel + /CE jel. A /CE jel alapb�l a TVC /EXPn jele. 
- OPCION�LIS: a jeleket vagy a k�belek beforraszt�s�val, vagy egy t�skesor beilleszt�s�vel �s szalagk�bellel lehet elvezetni.
-- Az exp lapon 3db 2x20 -as t�skesornak van hely amikhez 40 eres szalagk�belek kellenek. Ha megn�zed, az egyik t�skesor kiv�logatott jeleket tartalmaz. Tanulm�nyozd, mert lehet, h neked el�g csak azokat a jeleket elhozni a lapr�l. Az als� k�t headersor az �sszes TVC kivezet�st tartalmazza.
-- A cart lapon 1db 2x17 -es t�skesornak van hely, amihez 34 eres szalagk�bel kell.
- OPCION�LIS: Mindk�t lap tartalmaz helyeket �.n. polifuse-nak, azaz �ngy�gy�t� biztos�t�knak a +5V -os �s a +12V (csak exp) �gon. Jel�l�s�k F1 (�s F2 az exp lapon). Nem musz�j berakni, viszont v�delmet jelent a TVCnek. Ha berakod, akkor ne felejtsd el elv�gni alul a ny�kon az �tvezet�st (ha m�r elv�gtad, akkor be KELL rakni a biztos�t�kot)!
- OPCION�LIS: Mindk�t lap tartalmaz LED-nek �s ellen�ll�snak helyet, melyek visszajelz�sk�nt tudnak szolg�lni a +5V �s a +12V (csak exp lapon) �gaknak.
-- Az exp lapon 3mm -es LEDek �s 5k1 �s 12k �rt�k� ellen�ll�sok kellenek
-- A cart lapon 5mm -es LED �s egy 5k1 �rt�k� ellen�ll�s kell
-- Az �rt�kek nem k�bev�sett sz�mok, ha azt akarod, hogy jobban vil�g�tson a LEDed, akkor rakj be kisebb ellen�ll�st - de csak �sszel (tudd, hogy mit csin�lsz)!
- FONTOS: a fels� b�v�t� r1 �s r2-es v�ltozata is le lett gy�rtva, m�k�dnek. A programmodulb�l gy�rtott r1 -es v�ltozatban a GND nem volt bek�tve. Ez lett jav�tva az r2-ben, viszont abb�l m�g nem gy�rtattam, de m�s v�ltoztat�s nem lett a ny�klapon, m�k�dnie kell. Az r1-es - hib�s - v�lozatot nem is t�lt�ttem fel, minek.


## English
This repository contains breakout board PCB plans for the Videoton TVC computer in EagleCAD. There are two type of TVC sockets I plan to provide help in this repo : 
- cartridge socket: This is the programmodule connector on the left side of the computer (cartridges uses this socket).
- expansion socket: There are 4 sockets on the top of the computer for IO board expansions (floppy and serial expansion cards use these connectors)

These PCBs is aiming to help new card builders to get easily all the signals from each of the connector. 
- _cart_ directory contains source files for the cartridge ('programmodul')
- _exp_ directory contains source files for the expansion ports.
- _imgs_ contains images about manufactured PCBs
- _lib_ directory contains the necessary library files
- OPTIONAL: both of the PCBs contain places for polifuse (marked as F1 and F2). If you place those you have to cut the wire on the back side of the PCB
- OPTIONAL: both of the PCBs contain places for LED and resistor. Those are just a visual signal to the hw developer if the TVC PSU provides the power (overheated TVC PSU needs some time to 'recover'). The resistor values are 5k1 for the 5V and 12k for the 12V, but those can be lowered if you want brighter LEDs (know what you are doing there!!). The LEDs are 3mm on the exp PCB and 5MM on the cart PCB.
- Both revisions of the exp PCB was manufactured and they works properly. The cart PCB r1 contained an error (GND pin was not connected on the header) so I fixed that but it wasn't manufactured yet. No other change was made, r1 otherwise works. 

# License: GNU GPL v3
[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)    




