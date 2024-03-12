git diff:
Mit Hilfe von git diff kann man sich im Falle eines Mergekonflikts die Unterschiede beider Commits anzeigen lassen.
Hat man z.B. zwei Textdokumente und bekommt eine Fehlermeldung beim mergen, dann zeigt git diff was beim Mergen zu Problemen geführt hat.

git merge -abrot:
Mit git merge -abrot kann man schwebende Commits abrechen. Dadurch wird der Working tree zurück gesetzt auf das, was vor dem mergen darin vorhanden war.
