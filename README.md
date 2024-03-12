branch
Ein "Branch" in Git ist wie ein Zweig in einem Baum. Du kannst einen Branch erstellen, um an neuen Funktionen oder Fehlerkorrekturen zu arbeiten, 
ohne den Hauptcode zu beeinflussen. Es ermöglicht dir, Änderungen getrennt zu halten und sie später mit dem Hauptcode zu fusionieren, wenn sie fertig sind. 
So bleibt der Hauptcode stabil, während du experimentierst oder neue Funktionen entwickelst.

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