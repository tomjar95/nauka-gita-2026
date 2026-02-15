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