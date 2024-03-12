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