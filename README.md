<img width="561" height="461" alt="Diagramă fără titlu drawio(1)" src="https://github.com/user-attachments/assets/e47e000b-8b37-4ab7-bda9-2fa0908ac521" />
# ProiectTSC
3. Descrierea Funcționalității Hardware
Module și Interfețe

    Microcontroller: nRF52840 gestionează procesarea centrală.

    Display E-Paper: Comunică prin interfața SPI. S-a ales acest tip de ecran datorită consumului de energie zero în stare statică.

    Senzor IMU: Conectat prin I2C, utilizat pentru detectarea mișcării și orientării.

    Sistem de alimentare: Include un circuit de încărcare pentru bateria Li-Po și convertoare DC/DC pentru a asigura pragurile de tensiune de 3.3V necesare componentelor digitale.

    Interfață Utilizator: Trei butoane mecanice pentru navigare și un motor de vibrații pentru notificări haptice.



5. Design Log și Decizii Tehnice

    PCB Stackup: Placa are o grosime de 1mm
    Plan de masă: S-au implementat planuri de masă pe ambele straturi (Top și Bottom) legate prin Via Stitching pentru a minimiza zgomotul electromagnetic, în special în zona circuitului radio.

    Antenă: Zona de sub antenă a fost decupată complet de planul de masă pe toate straturile pentru a asigura performanța optimă a semnalului BLE.

    Erori DRC acceptate: S-au ignorat erorile de tip "Dimension" la butoane și mufa USB-C deoarece acestea sunt necesare pentru alinierea mecanică cu carcasa, conform specificațiilor.

    Componente: Toate rezistențele și condensatoarele de decuplare (100nF) au fost plasate în capsulă 0201 cât mai aproape de pinii IC-urilor.
