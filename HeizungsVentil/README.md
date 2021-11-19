# hm_ventiel
##Homematic Ventiel Script

..... 

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



