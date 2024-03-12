git diff:
Mit Hilfe von git diff kann man sich im Falle eines Mergekonflikts die Unterschiede beider Commits anzeigen lassen.
Hat man z.B. zwei Textdokumente und bekommt eine Fehlermeldung beim mergen, dann zeigt git diff was beim Mergen zu Problemen geführt hat.

git merge -abrot:
Mit git merge -abrot kann man schwebende Commits abrechen. Dadurch wird der Working tree zurück gesetzt auf das, was vor dem mergen darin vorhanden war.

Detached Head:
Man befindet sich im detached Head wenn man einen Commit auscheckt, der keinen Branch hat. Man checkt also z.B. C2 aus. Dann zeigt der Head auf C2 ohne einen Branch "dazwischen", würde man jetzt committen, hätte dieser Commit keine Historie. Es wäre also sehr schwer ihn wieder zu finden. Um dies zu verhindern, erstellt man erst einen neuen Branch bevor man committet.
