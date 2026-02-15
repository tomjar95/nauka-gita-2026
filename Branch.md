# zobacz gdzie jesteś i jakie gałęzie istnieją
git branch

# nowa gałąź i od razu na nią przeskakujemy
git switch -c feat/koszyk
# albo stare dobre
# git checkout -b fix/bug-127

# praca → commit(y) → push gałęzi
git push -u origin feat/koszyk

# powrót na main i aktualizacja
git switch main
git pull

# scalenie (po pull request / code review)
git merge feat/koszyk
git push

# sprzątanie
git branch -d feat/koszyk