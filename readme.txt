CEL EDUKACYJNY:
    * projekt wielokontenerowy, widać to w docker-compose
        * przekazywanie zmiennych środowiskowych do kontenerów
        * używanie gotowych kontenerów z registry
    * html 5 push event routing (pokazany przez interakcję 2 stron html)
    * wykorzystanie nodemon
    * nginx


DOKUMENTACJA:
    Dużo ZRZUTÓW ekranów dla tej aplikacji jest w Google Drive/inicjatywy/DevOpsDev/helpers


PLIKI:
    podprojekt client zawiera frontend wygenerowany przez create-react-app, edytkowano następujące pliki:
        .\client\src\OtherPage.js
        .\client\src\Fib.js - tutaj są wywołania poszczególnych routes (i apis)
        .\client\src\App.js - to jest startowy plik dla aplikacji React, 
    podprojekt server zawiera ???
        .\server\Dockerfile.dev - pokazuje wykorzystanie nodemon
        .\server\index.js - zawiera m.in. route handlers
    podprojekt worker
        .\worker\Dockerfile.dev
    folder nginx
        .\nginx\default.conf   - plik konfiguracyjny dla nginx
        .\nginx\Dockerfile.dev

WYWOŁANIE:
    przez port 3050 - port ten został ustawiony w docker-compose  jako port wejściowy dla servisu nginx


