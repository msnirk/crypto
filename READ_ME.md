##Project backlog:
- integracja z 3 gieldami
  - mozliwosc pobierania kursu waluty ze zdefiniowanej gieldy w danym momencie
  - interwal czasu dla odpytan
  - zakres czasu z ktorego chcemy zobaczyc kurs
  - waluty:
    - Crypto:
      - BTC
      -  ETH
    - Fiat:
      - USD
      - EURO
      - PLN
      - złoto
      - srebro
    - https://bitbay.net/pl/api-prywatne
    - https://binance-docs.github.io/apidocs/spot/en/
    - https://bittrex.github.io/api/v3
    - https://coinmarketcap.com/api/
      - dev TODO: 5 sda days - 15 sda days
        - rozpoznanie API
        - zbudowac importer per giełda
        - entity: 
        - dto
        - repository
        - serwis
        - serwis webowy (thymeleaf)
        - serwis resstowy (angulara)
        - UI Angular

- wykresy   1 sda days - 3 sda days
  - czas-cena
  - rozny kolor w zaleznosci od tego czy jest tendencja spadkowa czy wzrostowa 
  - zbudowany slupek od minimalnej do maksymalnej ceny w zaleznosci od interwalu czasowego
  - dev TODO:
    - wybór biblioteki
    - sortowanie
    - filtrowanie
    - kontroler
    - UI Angular
  

- transakcje 2 sda days - 4 sda days
  - mozliwosc przeprowadzenia transakcji
  - historia
    - informacja o naszych transakcjach
  - dev TODO:
    - kontroler
    - UI Angular
    - integracja z portfelem 
 
### REFINEMENTS
- wyswietlanie TOP/sortowanie
- maksymalna i minnimalna cena w miesiacu
- przeliczanie walut
- wiadomości ze świata  😀
    - market research
- wyswietlanie paska z wartościami np. WIG 20
- alerty
- portfel
- filtry
- zleć kupno lub sprzedaż gdy wartość jest wybrana
- panel administracji konta
- może logowanie uzytkownika
- zmiana hasla
- opcja premium


#### MVC (Model, View, Controller)
V - view
C - controller
M - model (data + operations)

View - dto
Controller - returns dto
Service - operations
Repository - data (entities)

#### Responsibilities

Controller
- returns views/data
- handle queries

Service 
- business logic

Repository
- data management

#### Restfull (CRUD on Http)
- resource has URI
- Read - GET
- Create - POST
- Delete - DELETE
- Update - PUT (replace), PATCH (partial update)

#### Http Response codes
- 1xx - processing in progress
- 2xx - ok
- 3xx - redirecting
- 4xx - user error
- 5xx - server error