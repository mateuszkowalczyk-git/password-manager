# Secure Password Manager 

Lokalny menedżer haseł napisany w języku Python. Projekt prezentuje praktyczne zastosowanie podstaw kryptografii, bezpiecznego generowania liczb losowych oraz zarządzania poufnymi danymi w aplikacjach konsolowych.

##  Główne funkcjonalności

* **Kryptograficznie bezpieczny generator haseł:** Wykorzystuje wbudowany moduł `secrets` (CSPRNG) zamiast standardowego, przewidywalnego modułu `random`, co gwarantuje wysoki poziom bezpieczeństwa generowanych ciągów.
* **Szyfrowanie danych (AES):** Zapisane hasła są szyfrowane symetrycznie przy użyciu algorytmu AES w trybie CBC (za pomocą modułu Fernet z biblioteki `cryptography`).
* **Lokalne zarządzanie kluczami:** Automatyczne generowanie i wczytywanie głównego klucza szyfrującego (`secret.key`).
* **Trwały magazyn danych:** Przechowywanie zaszyfrowanych wpisów w lokalnym pliku `baza.json` z wykorzystaniem bezpiecznej obsługi plików w Pythonie (menedżery kontekstu `with open`).

##  Wymagania i technologie

* Python 3.x
* Biblioteka `cryptography`
* Wbudowane moduły Pythona: `secrets`, `json`, `os`

##  Instalacja i uruchomienie

1. Sklonuj repozytorium lub pobierz pliki projektu na swój dysk.
2. Zainstaluj wymaganą bibliotekę kryptograficzną:
   
```bash
   pip install cryptography
