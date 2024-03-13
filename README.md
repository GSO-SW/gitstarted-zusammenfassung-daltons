<u>Befehle der <b>lokalen</b> Arbeit</u>

<u><i>init:</i></u>
 Der Befehl git Init erstellt ein neues Git-Repository.
 Damit kann ein vorhandenes, nicht versioniertes Projekt in ein Git-Repository konvertiert oder ein neues, leeres Repository initialisiert werden.
 Die meisten anderen Git-Befehle sind außerhalb eines initialisierten Repositorys nicht verfügbar.
 Deshalb ist git init normalerweise der erste Befehl, der in einem neuen Projekt ausgeführt wird.

<u><i>add:</i></u>
Mit dem Befehl git add wird eine Änderung im Workingtree zur Staging Area Hinzugefügt.
Damit wird git angewiesen, Aktualisierungen einer Datei in den nächsten Commit aufzunehmen.
Git Add hat aber keine Auswirkungen auf das Repository, Änderungen werden erst aufgezeichnet, wenn commits ausgeführt werden.

<u><i>commit:</i></u>
Mit dem Befehl git commit wird eine Versionsgeschichte der aktuellen Projektänderungen erstellt. Committete Snapshots werden von Git nur auf ausdrücklichen Anweisung hin verändert, da sie als „sichere“ Versionen eines Projekts betrachtet werden. Um Änderungen, die in einem Commit gespeichert werden sollen, in das Projekt zu befördern oder zu stagen, verwendet man den Befehl git add, bevor git commit ausgeführt wird. Die beiden Git-Befehle git commit und git add sind die am weitesten verbreiteten.

<u><i>checkout:</i></u>
Mit dem Befehl git checkout wird zwischen zwei Branches gewechselt, die mit git Branch erstellt wurden.
Wenn in Git ein checkout ausgeführt wird, werden die Dateien im Workingtree mit den in dem betroffenen Branch gespeicherte Versionen Aktualisiert und Git speichert alle neuen Commits in dem ausgecheckten Branch.
Es wird also im Grunde ausgewählt, zu welchem Git-Branch gewechselt wird, um an der Entwicklungslinie weiter zu arbeiten.

<u><i>branch:</i></u>
Ein "Branch" in Git ist wie ein Zweig in einem Baum. Du kannst einen Branch erstellen, um an neuen Funktionen oder Fehlerkorrekturen zu arbeiten, 
ohne den Hauptcode zu beeinflussen. Es ermöglicht dir, Änderungen getrennt zu halten und sie später mit dem Hauptcode zu fusionieren, wenn sie fertig sind. 
So bleibt der Hauptcode stabil, während du experimentierst oder neue Funktionen entwickelst.
Wenn man den Branch ertellt hat, heißt das noch nicht, dass man auf dem Branch ist. Man muss ihm erst "auschecken".

<u><i>merge:</i></u>
"Merge" in Git ist wie das Zusammenführen von zwei Zweigen in einem Baum. Wenn du Änderungen in einem separaten Branch vorgenommen hast und diese in den Hauptbranch 
integrieren möchtest, kannst du den Merge-Befehl verwenden. Dadurch werden die Änderungen aus dem Quell-Branch in den Ziel-Branch übernommen, sodass du alle neuen 
Funktionen oder Korrekturen zusammenführen kannst, um einen konsolidierten Code zu erhalten.

<u><i>rebase:</i></u>
"Rebase" in Git ist eine Methode, um die Änderungen aus einem Branch auf einen anderen anzuwenden, indem du den Zweig an einen neuen Ausgangspunkt verschiebst. 
Es ist wie das Umstellen von Büchern in einem Regal, um eine klare und lineare Geschichte zu erhalten. Dadurch kannst du deine Änderungen auf dem aktuellsten 
Stand halten und einen sauberen Verlauf deiner Commits beibehalten.

<u><i>git cherry pick:</i></u>
Mit Hilfe git cherry pick kann man eine Änderung eines bestimmten Commits "pflücken". Man überträgt nicht die gesamte Historie sondern nur die Änderung.

<u><i>revert:</i></u>
Der Befehl git revert ermöglicht es dir, einzelne Commits in einem Git-Repository rückgängig zu machen, ohne den gesamten Verlauf zu ändern. Du kannst ihn verwenden, 
indem du die Kennung des Commits angibst, den du rückgängig machen möchtest. Git erstellt dann automatisch einen neuen Commit, der die Änderungen dieses 
Commits widerspiegelt. Das ist nützlich, wenn du bestimmte Fehler beheben oder unerwünschte Änderungen entfernen möchtest, während der bisherige Verlauf 
des Repositorys erhalten bleibt.

<u><i>reset:</i></u>
Git Reset wird verwendet um den Zustand von Working tree und Staging area zu verändern. Dabei gibt es drei Variationen Reset hard Mixed und soft.<br>
1. --hard Bei git Reset --hard wird alles im Working tree und der Staging area verworfen und es wird auf den ausgewählten commit zurück gegangen, dabei werden alle commits die nach dem ausgewählten gemacht worden gelöscht.<br>
2. --mixed Bei Git Reset --mixed werden alle Änderungen in der Staging area zurück gesetzt, Es werden jedoch keine änderungen am Working tree vorgenommen. Im Repository werden außerdem alle commits nach dem angegebenen gelöscht. Git reset --mixed ist außerdem der Standard und wird verwendet wenn nichts angegeben wird.<br>
3. --soft Bei Git Reset --soft werden alle Änderungen bei behalten in der Staging area so wie im Working tree. Es wird jegendlich der HEAD auf den ausgewählten commit verschoben, wodurch sich die Historie eines Branches ändern lässt ohne den Working tree zu beinflüssen.

<u><i>status (Workingtree & Staging-area):</i></u>
Der Befehlt git Status gibt den Status von dem Workingtree und der Staging-area an.
So kann man sehen, welche Änderungen sich in  der Staging-area befinden, welche sich nicht in der Staging-area befinden und welche Dateien nicht von git verfolgt werden. 
Git Status zeigt keine Informationen bezüglich des committeten Projektverlauf an.

<u><i>log (Repository):</i></u>
Der Befehl git log dient dazu die Commit Historie eines Projekt anzeigen zu lassen.
Es zeigt eine Liste der Commits an, die in einem Repository gemacht wurde, zusammen mit daten des commits wie Datum und commit Nachricht.

<u><i>diff:</i></u>
Mit Hilfe von git diff kann man sich im Falle eines Mergekonflikts die Unterschiede beider Commits anzeigen lassen.
Hat man z.B. zwei Textdokumente und bekommt eine Fehlermeldung beim mergen, dann zeigt git diff was beim Mergen zu Problemen geführt hat.

<u><i>merge -abrot:</i></u>
Mit git merge -abrot kann man schwebende Commits abrechen. Dadurch wird der Working tree zurück gesetzt auf das, was vor dem mergen darin vorhanden war.

<u>Befehle der <b>entfernten</b> Arbeit</u>

<u><i>clone:</i></u>
Der Befehl git Clone dient dazu, ein vorhandenes Repository als Ziel festzulegen und einen Klon oder eine Kopie des Ziel-Repositorys zu erstellen.
Wenn ein Repository auf GitHub erstellt wird, liegt es als Remote-Repository vor. 
Das Repository kann geklont, um eine lokale Kopie auf deinem Computer zu erstellen, und die beiden Speicherorte synchronisieren.
Git Clone ermöglicht also die Zusammenarbeit an einem Projekt in dem das repository von einem anderen Nutzer geklont werden kann. 

<u><i>push:</i></u>
"Push" in Git bedeutet, deine lokalen Änderungen auf eine Plattform wie GitHub hochzuladen, damit andere darauf zugreifen können. Das ist wichtig, 
damit alle im Team die aktuellen Updates sehen und daran arbeiten können.

<u><i>fetch:</i></u>
 "Fetch" ist ein Git-Befehl, mit dem du die neuesten Änderungen von einem entfernten Repository herunterladen kannst, ohne sie auf deinem lokalen Branch zu fusionieren. 
Es ist wie ein Blick auf die Aktualisierungen, die auf dem Server gespeichert sind, ohne deine eigenen Änderungen zu beeinflussen.

<u><i>pull:</i></u>
"Pull" in Git ist ein Befehl, der deine lokalen Änderungen mit den neuesten Änderungen aus einem entfernten Repository aktualisiert. 
Es ist wie das Aktualisieren deiner Arbeitskopie, um sicherzustellen, dass du die aktuellste Version deines Codes hast.

<u><i>--set-upstream:</i></u>
Mit dem Anhang --set-upstream erstellt man, beim ersten pushen von einem lokalen Branch, einen Branch auf dem Remote Repository der dem Lokalen Branch entspricht.

<u><b>Fachbegriffe</b></u>

<u><i>Versionsverwaltungssysteme:</i></u>
Versionsverwaltungssysteme helfen im Verlauf von Projekten den Überblick zu behalten, indem sie die Historie des Projektes anzeigen können. Damit auch was der neuste stand ist.<br>
	1. Lokale Versionsverwaltungssysteme sind Systeme, die nur auf dem eigenen Rechner sind. Nachteil davon ist, dass wenn der eigene Rechner ausfällt ist alles weg.<br>
	2. Zentrale Versionsverwaltungssysteme haben einen zentralen Server auf dem das Repository liegt. Mehrere Clients können auf den letzten Zustand zugreifen, das ermöglicht Zusammenarbeit. Allerdings gibt es immer noch das Problem, fällt der Server aus ist die gesamte Historie weg.<br>
	3. Bei Dezentrale Versionsverwaltungssysteme wird das gesamte Repository auf den lokalen Rechner   kopiert. Das heißt ist der Server oder einer der Rechner beschädigt, so kann das Repository einfach wieder gecloned werden. Es geht also nicht einfach verlohren nur weil etwas kaputt geht. 

<i><u>Working tree:</i></u>
Der Working tree in git ist der Bereich wo die Version deines Projektes liegt, and der du gerade Arbeitest und welcher im Datei Explorer zu sehen ist. Man kann Dateien aus dem Workingtree der Staging area mit git add hinzufügen.

<i><u>Staging area:</i></u>
Die Staging Area ist ein Zwischenspeicher, vor dem committen wo man seine commits vorbereiten kann. Man kann Dateien mit git add hinzufügen und mit git commit in das Repository überführen. Dabei kann man durch die Staging area auch nur bestimmte Dateien in hinzufügen und nicht alle Änderungen im Working tree erfassen.

<i><u>Repository:</i></u>
Im Repository werden alle Dateien und Versionen von einem Projekt gespeichert die im verlauf eines Projektes erstellt wurden. Dabei besteht die Möglichkeit den verlauf nachzuvollziehen und auf ältere Versionen zurück zu gehen.
Remote Repository
Das Remote Repository ist genau so wie ein Repository, nur das dies nicht auf dem Computer des Nutzers sondern auf einem Server liegt, und die Möglichkeit besteht, das auf dies von mehreren Personen gleichzeitig zugegriffen werden kann. Es kann außerdem als eine Art backup benutzt werden.

<u><i>Head:</i></u>
In Git ist ein Head ein Zeiger der auf einen bestimmten commit in der aktuellen Versionsgeschichte eines Projekts zeigt.
Es zeigt an, an welchem Punkt man sich in einem Projekt befindet.
Der Head kann auf den letzten Commit eines Branches oder auf ein Commit zeigen.
Der Head ändert sich, wenn neue Commits erstellt werden oder wenn zwischen Branches gewechselt werden, und hilft dabei, den aktuellen Zustand eines Codes zu verfolgen.

<u><i>Detached Head:</i></u>
Man befindet sich im detached Head wenn man einen Commit auscheckt, der keinen Branch hat. Man checkt also z.B. C2 aus. Dann zeigt der Head auf C2 ohne einen Branch "dazwischen", würde man jetzt committen, hätte dieser Commit keine Historie. Es wäre also sehr schwer ihn wieder zu finden. Um dies zu verhindern, erstellt man erst einen neuen Branch bevor man committet.

<u><i>Schwebender Commit:</i></u>
Ein Schwebender Commit entsteht bei einem Merging-Konflikt. Man erkennt ihn an dem (branchName| MERGING). Es bedeutet, dass es ein Problem beim Mergen gibt und das mergen nicht vollendet werden kann.

<u><i>.gitignore Datei:</i></u>
Die .gitignore-Datei sagt Git, welche Dateien und Ordner ignoriert werden sollen, damit sie nicht verfolgt oder ins Repository aufgenommen werden. 
Das ist praktisch für temporäre Dateien, Logdateien oder sensible Informationen. Man erstellt eine Datei namens ".gitignore" im Repository und listet 
darin Dateien oder Muster auf, die ignoriert werden sollen. Das hält den Versionsverlauf sauber und verhindert, dass unerwünschte Dateien im Repository landen.
