# Lokální katalog MVČR
Metadata lokálního katalogu otevřených dat MVČR v JSON-LD.

## Přidání datové sady
Přidat datovou sadu lze vyplněním [formuláře v NKOD](https://data.gov.cz/formulář/registrace-datové-sady), kde v třetím kroku se ozubeným kolečkem nastaví stažení záznamu pro LKOD, doplní IRI datové sady s prefixem `https://data.mvcr.gov.cz/zdroj/datové-sady/` a zbytkem dle struktury repozitáře, např. `https://data.mvcr.gov.cz/zdroj/datové-sady/czechpoint/2007` a vyplní IRI poskytovatele, tj. `https://rpp-opendata.egon.gov.cz/odrpp/zdroj/orgán-veřejné-moci/00007064`.
Stažený registrační soubor se pak uloží na vhodné místo tohoto repozitáře.

Tato akce spustí automatický aktualizační proces v [LinkedPipes ETL](https://github.com/linkedpipes/etl), který aktualizuje katalog ve [SPARQL Endpointu](https://data.mvcr.gov.cz/sparql) a v instanci [LinkedPipes DCAT-AP Viewer](https://github.com/linkedpipes/dcat-ap-viewer) běžící na https://data.mvcr.gov.cz.
Data odpovídají Otevřené formální normě [Rozhraní katalogů otevřených dat](https://data.gov.cz/otevřené-formální-normy/rozhraní-katalogů-otevřených-dat/2019-04-04/) a ze SPARQL Endpointu jsou data harvestována do [Národního katalogu otevřených dat (NKOD)](https://data.gov.cz/datové-sady).
