
Init:
 Der Befehl git Init erstellt ein neues Git-Repository.
 Damit kann ein vorhandenes, nicht versioniertes Projekt in ein Git-Repository konvertiert oder ein neues, leeres Repository initialisiert werden.
 Die meisten anderen Git-Befehle sind außerhalb eines initialisierten Repositorys nicht verfügbar.
 Deshalb ist git init normalerweise der erste Befehl, der in einem neuen Projekt ausgeführt wird.

Add:
Mit dem Befehl git add wird eine Änderung im Workingtree zur Staging Area Hinzugefügt.
Damit wird git angewiesen, Aktualisierungen einer Datei in den nächsten Commit aufzunehmen.
Git Add hat aber keine Auswirkungen auf das Repository, Änderungen werden erst aufgezeichnet, wenn commits ausgeführt werden.

Commit:
Mit dem Befehl git commit wird eine Versionsgeschichte der aktuellen Projektänderungen erstellt. Committete Snapshots werden von Git nur auf ausdrücklichen Anweisung hin verändert, da sie als „sichere“ Versionen eines Projekts betrachtet werden. Um Änderungen, die in einem Commit gespeichert werden sollen, in das Projekt zu befördern oder zu stagen, verwendet man den Befehl git add, bevor git commit ausgeführt wird. Die beiden Git-Befehle git commit und git add sind die am weitesten verbreiteten.

Checkout:
Mit dem Befehl git checkout wird zwischen zwei Branches gewechselt, die mit git Branch erstellt wurden.
Wenn in Git ein checkout ausgeführt wird, werden die Dateien im Workingtree mit den in dem betroffenen Branch gespeicherte Versionen Aktualisiert und Git speichert alle neuen Commits in dem ausgecheckten Branch.
Es wird also im Grunde ausgewählt, zu welchem Git-Branch gewechselt wird, um an der Entwicklungslinie weiter zu arbeiten.

Head:
In Git ist ein Head ein Zeiger der auf einen bestimmten commit in der aktuellen Versionsgeschichte eines Projekts zeigt.
Es zeigt an, an welchem Punkt man sich in einem Projekt befindet.
Der Head kann auf den letzten Commit eines Branches oder auf ein Commit zeigen.
Der Head ändert sich, wenn neue Commits erstellt werden oder wenn zwischen Branches gewechselt werden, und hilft dabei, den aktuellen Zustand eines Codes zu verfolgen.

Clone:
Der Befehl git Clone dient dazu, ein vorhandenes Repository als Ziel festzulegen und einen Klon oder eine Kopie des Ziel-Repositorys zu erstellen.
Wenn ein Repository auf GitHub erstellt wird, liegt es als Remote-Repository vor. 
Das Repository kann geklont, um eine lokale Kopie auf deinem Computer zu erstellen, und die beiden Speicherorte synchronisieren.
Git Clone ermöglicht also die Zusammenarbeit an einem Projekt in dem das repository von einem anderen Nutzer geklont werden kann. 

Status (Workingtree & Staging-area):
Der Befehlt git Status gibt den Status von dem Workingtree und der Staging-area an.
So kann man sehen, welche Änderungen sich in  der Staging-area befinden, welche sich nicht in der Staging-area befinden und welche Dateien nicht von git verfolgt werden. 
Git Status zeigt keine Informationen bezüglich des committeten Projektverlauf an.

Log (Repository):
Der Befehl git log dient dazu die Commit Historie eines Projekt anzeigen zu lassen.
Es zeigt eine Liste der Commits an, die in einem Repository gemacht wurde, zusammen mit daten des commits wie Datum und commit Nachricht.

git diff:
Mit Hilfe von git diff kann man sich im Falle eines Mergekonflikts die Unterschiede beider Commits anzeigen lassen.
Hat man z.B. zwei Textdokumente und bekommt eine Fehlermeldung beim mergen, dann zeigt git diff was beim Mergen zu Problemen geführt hat.

git merge -abrot:
Mit git merge -abrot kann man schwebende Commits abrechen. Dadurch wird der Working tree zurück gesetzt auf das, was vor dem mergen darin vorhanden war.

Detached Head:
Man befindet sich im detached Head wenn man einen Commit auscheckt, der keinen Branch hat. Man checkt also z.B. C2 aus. Dann zeigt der Head auf C2 ohne einen Branch "dazwischen", würde man jetzt committen, hätte dieser Commit keine Historie. Es wäre also sehr schwer ihn wieder zu finden. Um dies zu verhindern, erstellt man erst einen neuen Branch bevor man committet.

Schwebender Commit:
Ein Schwebender Commit entsteht bei einem Merging-Konflikt. Man erkennt ihn an dem (branchName| MERGING). Es bedeutet, dass es ein Problem beim Mergen gibt und das mergen nicht vollendet werden kann.

Versionsverwaltungssysteme:
Versionsverwaltungssysteme helfen im Verlauf von Projekten den Überblick zu behalten, indem sie die Historie des Projektes anzeigen können. Damit auch was der neuste stand ist.
	1. Lokale Versionsverwaltungssysteme sind Systeme, die nur auf dem eigenen Rechner sind. Nachteil davon ist, dass wenn der eigene Rechner ausfällt ist alles weg.
	2. Zentrale Versionsverwaltungssysteme haben einen zentralen Server auf dem das Repository liegt. Mehrere Clients können auf den letzten Zustand zugreifen, das ermöglicht Zusammenarbeit. Allerdings gibt es immer noch das Problem, fällt der Server aus ist die gesamte Historie weg.
	3. Bei Dezentrale Versionsverwaltungssysteme wird das gesamte Repository auf den lokalen Rechner   kopiert. Das heißt ist der Server oder einer der Rechner beschädigt, so kann das Repository einfach wieder gecloned werden. Es geht also nicht einfach verlohren nur weil etwas kaputt geht. 

--set-upstream:
Mit dem Anhang --set-upstream erstellt man, beim ersten pushen von einem lokalen Branch, einen Branch auf dem Remote Repository der dem Lokalen Branch entspricht.

git cherry pick:
Mit Hilfe git cherry pick kann man eine Änderung eines bestimmten Commits "pflücken". Man überträgt nicht die gesamte Historie sondern nur die Änderung.

branch
Ein "Branch" in Git ist wie ein Zweig in einem Baum. Du kannst einen Branch erstellen, um an neuen Funktionen oder Fehlerkorrekturen zu arbeiten, 
ohne den Hauptcode zu beeinflussen. Es ermöglicht dir, Änderungen getrennt zu halten und sie später mit dem Hauptcode zu fusionieren, wenn sie fertig sind. 
So bleibt der Hauptcode stabil, während du experimentierst oder neue Funktionen entwickelst.
Wenn man den Branch ertellt hat, heißt das noch nicht, dass man auf dem Branch ist. Man muss ihm erst "auschecken".

merge
"Merge" in Git ist wie das Zusammenführen von zwei Zweigen in einem Baum. Wenn du Änderungen in einem separaten Branch vorgenommen hast und diese in den Hauptbranch 
integrieren möchtest, kannst du den Merge-Befehl verwenden. Dadurch werden die Änderungen aus dem Quell-Branch in den Ziel-Branch übernommen, sodass du alle neuen 
Funktionen oder Korrekturen zusammenführen kannst, um einen konsolidierten Code zu erhalten.

rebase
"Rebase" in Git ist eine Methode, um die Änderungen aus einem Branch auf einen anderen anzuwenden, indem du den Zweig an einen neuen Ausgangspunkt verschiebst. 
Es ist wie das Umstellen von Büchern in einem Regal, um eine klare und lineare Geschichte zu erhalten. Dadurch kannst du deine Änderungen auf dem aktuellsten 
Stand halten und einen sauberen Verlauf deiner Commits beibehalten.

revert
Der Befehl git revert ermöglicht es dir, einzelne Commits in einem Git-Repository rückgängig zu machen, ohne den gesamten Verlauf zu ändern. Du kannst ihn verwenden, 
indem du die Kennung des Commits angibst, den du rückgängig machen möchtest. Git erstellt dann automatisch einen neuen Commit, der die Änderungen dieses 
Commits widerspiegelt. Das ist nützlich, wenn du bestimmte Fehler beheben oder unerwünschte Änderungen entfernen möchtest, während der bisherige Verlauf 
des Repositorys erhalten bleibt.

push
"Push" in Git bedeutet, deine lokalen Änderungen auf eine Plattform wie GitHub hochzuladen, damit andere darauf zugreifen können. Das ist wichtig, 
damit alle im Team die aktuellen Updates sehen und daran arbeiten können.

fetch
 "Fetch" ist ein Git-Befehl, mit dem du die neuesten Änderungen von einem entfernten Repository herunterladen kannst, ohne sie auf deinem lokalen Branch zu fusionieren. 
Es ist wie ein Blick auf die Aktualisierungen, die auf dem Server gespeichert sind, ohne deine eigenen Änderungen zu beeinflussen.

pull
"Pull" in Git ist ein Befehl, der deine lokalen Änderungen mit den neuesten Änderungen aus einem entfernten Repository aktualisiert. 
Es ist wie das Aktualisieren deiner Arbeitskopie, um sicherzustellen, dass du die aktuellste Version deines Codes hast.

.gitignore Datei	
Die .gitignore-Datei sagt Git, welche Dateien und Ordner ignoriert werden sollen, damit sie nicht verfolgt oder ins Repository aufgenommen werden. 
Das ist praktisch für temporäre Dateien, Logdateien oder sensible Informationen. Man erstellt eine Datei namens ".gitignore" im Repository und listet 
darin Dateien oder Muster auf, die ignoriert werden sollen. Das hält den Versionsverlauf sauber und verhindert, dass unerwünschte Dateien im Repository landen.


