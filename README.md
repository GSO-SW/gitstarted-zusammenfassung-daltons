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
