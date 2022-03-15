# Vaja14-UART-Putty-NUCLEO

Vprašanja:

Privzeto je UART2 vmesnik povezan na USB priključek razvojne ploščice. Katere dva mostička bi morali odspajkati in kateri dve povezavi pospajkati, da bi lahko uporabili pina Tx/D1in Rx/D0? __SB62__ in __SB63__, __SB13__ in __SB14__ (video od 0:45 naprej).

V področju Connectivity aktivirajte protokol USART2 kot asinhroni. Katera dva pina sta se pobarvala zeleno oz. se aktivirala? ____PA2____ in ____PA3_____.

V polju Configuration izbranega serijskega vmesnika pustimo privzeto hitrost(Baud Rate), ki zna       ____115200____Bits/s.

Za to funkcijozapišite ukaz za vklop/izklopzelene LED (pomagajte si z metodo toggle, glej vaja0a).____HAL_GPIO_TogglePin(GPIOA, GPIO_PIN_5);____.

Dodajte še ukaz za zakasnitev s funkcijo Delay iz knjižnice HAL, in sicer 2 sekunde (glej vaja0a):____HAL_Delay(1000);_____.

Program sva dopolnila tako, da sva dodala HAL_Delay(100); v USER CODE BEGIN 3, ki nama je omogočilo
izpis imen z vsakim pritiskom na tipko USER.


Komentar:
Naloga nama je na začetku sva imela težave pri nalaganju na stm board. To težavo sva odpravila z posodobitvijo programa. Pri 
programu PuTTY sva imela težavo pri izbiri COM priključka, ker nisva imela dostopa do upravitelja naprav. Na koncu, sva v program samo dodala še delay, da se nama je ob pritisku na tipko USER na programu PuTTY izpisalo najino ime.
