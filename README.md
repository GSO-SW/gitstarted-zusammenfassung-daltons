Working tree

Der Working tree in git ist der Bereich wo die Version deines Projektes liegt, and der du gerade Arbeitest und welcher im Datei Explorer zu sehen ist. Man kann Dateien aus dem Workingtree der Staging area mit git add hinzufügen.

Staging area

Die Staging Area ist ein Zwischenspeicher, vor dem committen wo man seine commits vorbereiten kann. Man kann Dateien mit git add hinzufügen und mit git commit in das Repository überführen. Dabei kann man durch die Staging area auch nur bestimmte Dateien in hinzufügen und nicht alle Änderungen im Working tree erfassen.  

Repository

Im Repository werden alle Dateien und Versionen von einem Projekt gespeichert die im verlauf eines Projektes erstellt wurden. Dabei besteht die Möglichkeit den verlauf nachzuvollziehen und auf ältere Versionen zurück zu gehen.

Remote Repository

Das Remote Repository ist genau so wie ein Repository, nur das dies nicht auf dem Computer des Nutzers sondern auf einem Server liegt, und die Möglichkeit besteht, das auf dies von mehreren Personen gleichzeitig zugegriffen werden kann. Es kann außerdem als eine Art backup benutzt werden. 

Reset 
Git Reset wird verwendet um den Zustand von Working tree und Staging area zu verändern. Dabei gibt es drei Variationen Reset hard Mixed und soft.
	1. --hard
	Bei git Reset --hard wird alles im Working tree und der Staging area verworfen und es wird auf den 	ausgewählten commit zurück gegangen, dabei werden alle commits die nach dem ausgewählten gemacht worden 	gelöscht.
	2. --mixed
	Bei Git Reset --mixed werden alle Änderungen in der Staging area zurück gesetzt, Es werden jedoch keine 	änderungen am Working tree vorgenommen. Im Repository werden außerdem alle commits nach dem angegebenen 	gelöscht. Git reset --mixed ist außerdem der Standard und wird verwendet wenn nichts angegeben wird.
	3. --soft
	Bei Git Reset --soft werden alle Änderungen bei behalten in der Staging area so wie im Working tree. Es wird 	jegendlich der HEAD auf den ausgewählten commit verschoben, wodurch sich die Historie eines Branches ändern 	lässt ohne den Working tree zu beinflüssen.
