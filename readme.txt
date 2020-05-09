CEL EDUKACYJNY:
    * projekt wielokontenerowy, widać to w docker-compose
        * przekazywanie zmiennych środowiskowych do kontenerów
        * używanie gotowych kontenerów z registry
    * html 5 push event routing (pokazany przez interakcję 2 stron html)
    * wykorzystanie nodemon
    * nginx
    * Elastic Beanstalk (EBS) wykorzysta kontenery zbudowane przez Travis (zobacz notatki o travis) załadowane do docker-hub
    * Plik sterujący dla EBS - potrzebny gdy jest wiele kontenerów - Dockerrun.aws.json
    * Użycie Amazon.RDS (relational db service) i Amazon.ElastiCache


DOKUMENTACJA:
    Dużo ZRZUTÓW ekranów dla tej aplikacji jest w Google Drive/inicjatywy/DevOpsDev/helpers - docker course notes, Travis 


PLIKI:
        .\Dockerrun.aws.json
        .\.travis.yml
        .\docker-compose.yml
    podprojekt client zawiera frontend wygenerowany przez create-react-app, edytkowano następujące pliki:
        .\client\src\OtherPage.js
        .\client\src\Fib.js - tutaj są wywołania poszczególnych routes (i apis)
        .\client\src\App.js - to jest startowy plik dla aplikacji React, 
        .\client\nginx\default.conf - konfiguracja nginx odpowiedzialnego za serwowanie stron 
        .\client\Dockerfile*       
    podprojekt server zawiera ???
        .\server\Dockerfile* - pokazuje wykorzystanie nodemon
        .\server\index.js - zawiera m.in. route handlers
    podprojekt worker
        .\worker\Dockerfile*
    folder nginx
        .\nginx\default.conf   - plik konfiguracyjny dla nginx odpowiedzialnego za routing
        .\nginx\Dockerfile*

WYWOŁANIE:
    http://192.168.99.100:4000/      port 4000 został ustawiony w docker-compose  jako port wejściowy dla servisu nginx
    
    
INTEGRATIONS:
   lokalnie w git zdalne repo w github dostało nazwę 4FiboRemote 



