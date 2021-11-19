# hm_jalousie
##Homematic Jalousie Script

Zeig in der Homematic die offenen, geschlossen und halb offenen Rollos/Jalousien an.
Es funktionieren die Homematic IP als auch die Homematic Rollo Aktoren.

Das Script ist als Programm auszuführen, am besten in einen Zeitintervall.
Die obersten Variablen/ Config Setting sind azupassen. Die Rollos/Jalousie Geräte
werden in einem oder mehr Gewerk/e gruppiert.

AB dem Punkt...

! -----------------------------------------------------------------------------------

! ab hier nichts verändern !

! -----------------------------------------------------------------------------------

Darf nichts mehr geändert werden.

##Konfiguration
(siehe dazu auch im Script die Kommentare)

*var LOGGING=true;*
		
>Mögliche Werte: true/false

>Schaltet das Loggin ein, sobald es auf "true" steht, wird in die Variable [LOGVar, 
>siehe weiter unten] der Text geschrieben. Dazu muss die Variable in der CCU auf 
>protokolierung aktiviert werden.

*var LOGName="Test: ";*		

>Mögliche Werte: "Irgendein Text"

>Wird for jede Meldung gesetzt um Logs zu Unterscheiden.

*var LOGVar="Debug";*			

>Mögliche Werte: "Variablen Namen" [Case sensitiv]

>Variable in der CCU, in der der Text geschrieben wird. Pprotokolierung 
>muss aktiviert werden, damit die Infos im System Protokoll zu sehen sind.


*var ClearSystemLog=false;*

>Mögliche Werte: true/false

>Sobald das Script gestartet wird, wird erst in der CCU das Logging geleert und 
>alle vohanenen Einträge gelöscht


*var jalousieUPSN="Jalousie auf";*

>Mögliche Werte: "Variablen Namen" [Case sensitiv]

>Hier werden die Rollos/Jalousie gezählt die auf sind. Mögliche Werte sind 0 bis X

*var jalousieDOWNSN="Jalousie zu";*

>Mögliche Werte: "Variablen Namen" [Case sensitiv]

>Hier werden die Rollos/Jalousie gezählt die zu sind. Mögliche Werte sind 0 bis X
 
*var jalousieHalfeSN="Jalousie halb";*

>Mögliche Werte: "Variablen Namen" [Case sensitiv]

>Hier werden die Rollos/Jalousie gezählt die auf halb (nicht zu oder auf) sind. 
>Mögliche erte sind 0 bis X

*string liste = "Jalousien Status";*

>Mögliche Werte:  [einzeln ="xxx"],[als Liste="xxx\tyyy\tzzz..."]

>Damit das Script alle Rollos/Jalousien findet muss ein Gewerk erzeugt werden in 
>den die Channels der Geräte sind (Status Kanal). Das kann ein Gewerk sein oder 
>auch mehrere Gewerke. Ein Gerät darf nur einmal vorhanden sein, ansonten wird es 
>doppelt gezählt

>HM-LC-Bl1-FM -> Channel 1

>HmIP-FROLL   -> Channel 4 oder 3
