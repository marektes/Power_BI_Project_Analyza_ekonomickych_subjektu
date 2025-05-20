Jedná se o projekt, který jsem vytvořil v rámci kurzu „Datová akademie“ společnosti ENGETO.

1. Datový soubor Registr ekonomických subjektů (RES)byl získán z Národního katalogu otevřených dat. URL: https://data.gov.cz/datov%C3%A1-sada?iri=https%3A%2F%2Fdata.gov.cz%2Fzdroj%2Fdatov%C3%A9-sady%2F00025593%2F7bad26fdd8554ce715b81b5b416d75f0

2. Tabulka RES obsahuje záznamy všech ekonomických subjektů v ČR (stav k 31.3.2025). Jednotlivé záznamy (řádky) se skládají mimo jiné z identifikátoru IČO, názvu subjektu, adresy, právní formy, oboru podnikání, počtu pracovníku apod.
Bylo zapotřebí obstarat také pomocné tabulky (číselníky), které jsou k dispozici v dokumentaci RES.

3. Datové sady byly staženy ve formátu CSV a nahrány do Power BI. V Power Query bylo nutné data vhodně transformovat, což u hlavní tabulky RES spočívalo v odebrání nepotřebných sloupců, odstranění již zaniklých subjektů, změna datového                typu některých sloupců a přidání nového sloupce oboru podnikání za pomoci jazyka M (Power Query Formula Language). Obor podnikání byl totiž označen pouze písmenem (např. P), ale pro následné analýzy byl potřeba celý název (např.
Zpracovatelský průmysl). Toto kódování jednotlivých oborů jsem nalezl v pomocném číselníku. Další sloupce jsem musel přidat i v číselníku „Počet zaměstnanců“, protože mi nevyhovoval příliš vysoký počet kategorií, které jsem zagregoval do menšího počtu.

4. Po transformaci dat jsem vytvořil datový model, kde jesm hlavní tabulku RES vhodně propojil s jednotlivými pomocnými tabulkami. Pro zamýšlené analýzy bylo nutné vytvořit také několik „měr“ za pomoci jazyka DAX. Pro vyšší efektivitu práce jsem si v této části pomohl nástroji „AI“.

5. Následně jsem měl vše připraveno pro vytváření jednotlivých vizuálů. Nechybí vizuál karta (nová), tabulka (s vlastními sloupci generovanými na základě připravených měr), výsečový a sloupcový graf a mapa s podmíněným vizuálním formátováním. K interaktivnímu filtrování jednotlivých krajů jsem využil průřez.

6. Vizuální podobu dashboardu jsem sjednotil do stejného formátu (stejné písmo, barvy, umístění vizuálů, ohraničení apod.). Do horní části jsem přidal interaktivní šipky pro navigaci po stranách.

7. Podle mého názoru je výsledný dashboard přehledný, uživatelsky přívětivý a zobrazuje zajímavé údaje ohledně podnikání v ČR se zaměřením na srovnání mezi jednotlivými kraji. Celkově jsem tímto projektem strávil odhadem 20 hodin.