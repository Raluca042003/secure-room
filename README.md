SecureRoom – Sistem de securitate cu STM32
Descriere

SecureRoom este un proiect de securitate pentru o încăpere, realizat cu un microcontroler STM32.

Accesul se face prin introducerea unui cod PIN de la o tastatură. Pentru un cod corect se aprinde un LED verde, iar pentru unul greșit un LED roșu.

Sistemul folosește un senzor PIR pentru detectarea mișcării. Dacă este detectată mișcare atunci când alarma este activată, se transmite o notificare wireless către o stație de monitorizare.

Componente hardware
STM32 Nucleo-F446RE
Tastatură matricială 4x4
Senzor de mișcare PIR
LED verde și LED roșu
Buzzer sau motor vibrator
Module wireless nRF24L01
Tehnologii utilizate
Limbajul C
STM32CubeIDE
FreeRTOS
Comunicație wireless
Organizarea aplicației

Aplicația va conține două task-uri independente:

Task de control local: verifică PIN-ul, citește senzorul și controlează alarma.
Task de comunicație: transmite evenimentele către stația de monitorizare.

Sincronizarea dintre task-uri se va realiza printr-o coadă de mesaje FreeRTOS.

Obiective
Controlul accesului prin PIN.
Detectarea mișcării și semnalizarea alarmei.
Transmiterea alertelor la distanță.
Utilizarea unui sistem de operare de timp real.
Măsurarea și analiza timpilor de răspuns.
Autor

Proiect realizat în cadrul disciplinei de sisteme cu microcontrolere și timp real.
