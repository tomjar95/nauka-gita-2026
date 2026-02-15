# Nauka Gita – szybki start 2026

Prosty zbiór najczęściej używanych komend i wzorców pracy z Gitem.

## 1. Pierwsze kroki (raz na komputer / raz na projekt)

```bash
# konfiguracja (wystarczy raz)
git config --global user.name "Jan Kowalski"
git config --global user.email "jan.kowalski@example.com"
git config --global init.defaultBranch main

# nowe repozytorium lokalne
git init
git add .
git commit -m "pierwszy commit"

# albo klonujemy istniejące
git clone https://github.com/user/projekt.git
cd projekt
```

## 2. Gałęzie – najprostszy sensowny flow

```bash
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
```


## 3. Cofanie i ratowanie
```bash
# cofnij ostatni commit (zmiany zostają w roboczym katalogu)
git reset --soft HEAD~1

# cofnij commit i usuń zmiany z dysku
git reset --hard HEAD~1

# cofnij tylko staging (git add)
git restore --staged plik.js

# cofnij zmiany w pliku
git restore plik.js

# ostatni ratunek – co miałem w ostatnim commicie
git log -1 -p
```


## 4. Podgląd historii
```bash
git log --oneline --graph --decorate --all
git log --oneline -8               # ostatnie 8 commitów
git log --oneline --author="Jan"   # tylko Jana
```