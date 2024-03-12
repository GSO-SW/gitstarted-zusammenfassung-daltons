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