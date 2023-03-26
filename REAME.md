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
- 