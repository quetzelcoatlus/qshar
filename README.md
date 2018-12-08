# qshar
Skrypt archiwizujący pliki, który generuje wykonywalny skrypt wypakowujący.

## Instalacja
Aby zainstalować qshara wystarczy wykonać następujące polecenia w terminalu:
```
curl https://raw.githubusercontent.com/quetzelcoatlus/qshar/master/install.sh | sudo sh
```
albo
```
wget -qO- https://raw.githubusercontent.com/quetzelcoatlus/qshar/master/install.sh | sudo sh
```

## Użycie
$ man qshar
```
qshar(1)                             qshar                            qshar(1)

NAZWA
       qshar  -  Skrypt archiwizujący pliki, który generuje wykonywalny skrypt
       wypakowujący.

SKŁADNIA
       qshar NAZWA_ARCHIWUM LISTA_PLIKOW

OPIS
       qshar jest własną  implementacją  programu  do  archiwizacji  plikow  w
       skrypt powłoki systemowej, inspirowany programem shar z sharutils.

       Wynikiem  archiwizacji  jest skrypt wykonywalny, który może zostać uru‐
       chomiony przez /bin/sh celem wypakowania.

       Skrypt obsługuje archiwizację plików i  katalogów.  Dla  każdego  pliku
       zamienia  on  wszystkie jego bajty na ósemkowy format obsługiwany przez
       printf oraz zapisuje jego atrybuty i sumę  kontrolną  wylicznoną  przez
       md5sum  (która  może  zostać pominięta, jeżeli wypakowujący nie posiada
       tego programu).

       qshar wymaga posiadania co najmniej jednego z następujących  programów:
       hexdump lub od celem zakodowania plików wejściowych.

       Ideą  programu  jest,  żeby  wynikowy  skrypt był jak najprostszy i jak
       najmniej zależny od zewnętrznych programów. Na chwilę obecną wymaga: if
       while mkdir chmod printf oraz (opcjonalnie) md5sum

ARGUMENTY
       Obecnie  qshar  nie  przyjmuje żadnych argumentów, ale z czasem może to
       ulec zmianie.

PRZYKŁADY
       1. Spakowanie jednego pliku main.c do archiwum o nazwie archiwum

              qshar archiwum main.c

       2. Spakowanie katalogu dir do archiwum ar

              qshar ar dir

       3. Spakowanie wszystkich plikow (i katalogow)  w  obecnym  katalogu  do
       archiwum

              qshar archiwum *

ZOBACZ TAKŻE
       shar(1)

AUTOR
       quetzelcoatlus (https://github.com/quetzelcoatlus)

Wersja 1.6                    06 Grudnia, AD 2018                     qshar(1)
```
