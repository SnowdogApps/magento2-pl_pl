Polski pakiet językowy dla Magento 2
==========
Repozytorium zawiera gotowy komponent z językiem polskim dla Magento 2.

Tłumaczenia są automatycznie synchronizowane ze zmianami dokonanymi w serwisie Crowdin co 15 minut.

## Instalacja

### Przez composera
* jeżeli chcemy trzymać się tylko oficjalnych wydań pakietu (do użycia w działającym sklepie)
```
$ composer config repositories.magento2-pl vcs https://github.com/SnowdogApps/magento2-pl_pl.git
$ composer require snowdog/language-pl_pl
```
* jeżeli zależy nam na wszystkich aktualnych zmianach (dla tłumaczy)
```
$ composer config repositories.magento2-pl vcs https://github.com/SnowdogApps/magento2-pl_pl.git
$ composer require snowdog/language-pl_pl dev-develop
```

Na koniec instalujemy treści statyczne z pobranym przed chwilą pakietem i czyścimy pamięci podręczne sklepu:
```
$ php bin/magento setup:static-content:deploy pl_PL
$ php bin/magento cache:flush
```

### Manualna
Pobieramy zawartość repozytorium i umieszczamy jego zawartość w lokalizacji `app/i18n/snowdog/pl_pl/`.
Ostatecznie powinniśmy otrzymać następującą strukturę:
```
app/i18n/
└── snowdog
    └── pl_pl
        ├── composer.json
        ├── language.xml
        ├── pl_PL.csv
        ├── README.md
        └── registration.php
```

Na koniec instalujemy treści statyczne z pobranym przed chwilą pakietem i czyścimy pamięci podręczne sklepu:
```
$ php bin/magento setup:static-content:deploy pl_PL
$ php bin/magento cache:flush
```
