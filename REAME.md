- SARG - definicja - powtórzyć

## Rekomnedowany podział plików po dyskach (nie partycjach)

- C - SQL bin
- D - tempdb
- E - dane
- D - logi

## System plików

- NTFS
- ReFS

## AV 

- wykluczaym katalogi z danymi SQL ze skanowania

## Konta dla usług (bez kupowania licencji)

- konta managment można założyć tylko przez powershell-a
- konta nie powinny mieć uprawnień

### Rekomendacje:

Zakładamy nowe konta
Do instalacji:

                domena      serwer
- SQLSRV_Intall DomainUser  LocalAdmin
- SQLSRV_Engine DomainUser  brak
- SQLSRV_Agent  DomainUser  brak
- ...           DomainUser  brak

## Szyfrowanie komunikacji

## Budowa SQL server

- Sieć
- DB_Endine
- AS
- SQLOS


## Bazy

### Bazy konfiguracyjne
- mamy 6 baz konfiguracyjnych (4 do 5 które widzimy, 6 jest dla nas "niedostępna")
  - bez bazy master nie uruchomimy servera
  - bez bazy model nie uruchomimy servera
  - tempdb - niszczona po każdym restarcie serwera
  - msdb - zależna od SQL Agenta
  - pojawia i się i zniga baza distribution (jeśli włączymy replikację baz)
  - mssystemresources - wewnętrzna baza sql servera - nie ma do niej prostego dostępu 

## Charakterystyka bazy

- stosunek odczyt/zapis 
- LDF - jest plikiem z zapisem sekwencyjnym
- MDF - tu zapis jest losowy
- rekomendacja - rozdzielić MDF i LDF różne dyski (zapis losowy/sekwencyjny)