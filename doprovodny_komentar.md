# PBI_Projekt
- Projekt se zaměřuje na politické násilí během války na Ukrajině. Zkoumaným obdobím je začátek ruské invaze 24.2. 2022 a konec sběru dat je ke dni 19.2.2025.
- Zadavateli mohou být vládní agentury, veřejný sektor, humanitární organizace nebo informační kanály, které mohou získané podklady využít například k analýze:
    - počtu obětí konfliktu,
    - druhů politického násilí, nebo
    - rostoucí efektivity různých typů dronů na bojišti.
- Tyto informace mohou sloužit jako podklad pro informovaná rozhodnutí, například při cílení humanitární pomoci, plánování akvizičních strategií či kvantitativním doložení skutečnosti, že masové nasazení rojů ruských dronů Shahed může signalizovat nárůst kapacit jejich výroby. To následně může vést k relokaci finančních prostředků směrem k identifikaci či monitoringu těchto výrobních zařízení.
- Takto získané poznatky jsou užitečné nejen pro novináře, ale také pro aktéry přímo zapojené do konfliktu.

## Obsah repozitáře
- .pbi složka Projekt_Engeto.SemanticModel
      - složka .pbi
      - složka definition
      - soubor .platform
      - soubor definition.pbism
      - soubor diagramLayout.json
- .pbix soubor Projekt_Engeto
- doprovodny_komentar.md

## Datové zdroje pro projekt
1. Ukrajina: kurátorované ACLED data z projektu [Ukraine Conflict Monitor](https://acleddata.com/monitor/ukraine-conflict-monitor)
2. Rusko: kurátorované ACLED data z datasetu [Europe and Central Asia](https://acleddata.com/region/europe-and-central-asia)
3. Údaje o dronových a raketových útocích na Ukrajině: dataset [Massive Missile Attacks on Ukraine](https://www.kaggle.com/datasets/piterfm/massive-missile-attacks-on-ukraine)
od Petra Ivaniuka na Kaggle

## Výroba datasetu pro projekt
- Dataset vznikl prvotním vyfiltrováním zkoumaného období v datasetu Ukraine Conflict Monitor. Z datasetu Europe and Central Asia bylo od ostatních zemí vyfiltrováno
pouze Rusko, kde byly údaje také omezeny na zkoumané období. Tyto dvě tabulky pak byly spojeny pomocí Append v Power Query. Datová příprava a filtrace byla před nahráním do PowerBI provedena v Excelu. 

## Stanovené cíle pro projekt:
- Cílem je vytvoření takových podkladů, které mohou sloužit pro zodpovězení například následujících okruhů otázek a jejich vizuální doprovod:
   - Jak se v průběhu času měnil počet a druh útoků, a to ve srovnání útoků vedených na území Ukrajiny a útoků směřujících na území Ruska?
   - Jaké druhy útoků se v průběhu války objevovaly, kdy dosahovaly nejvyšší intenzity podle počtu obětí a na jakých místech byly nejčastěji vedeny?
   - Které čtvrtletí války bylo v porovnání s ostatními nejintenzivnější z hlediska průměrného počtu útoků?
   - V kterém roce války došlo k největšímu počtu obětí, a jak se tento rok lišil ve srovnání s ostatními obdobími konfliktu?
   - Jak se v průběhu času měnil trend efektivity dronů a hlavic, a to na základě počtu vypuštěných dronů a hlavic a počtu jich zničených?
   - Které modely dronů a jaké druhy hlavic nejvýrazněji souvisejí s tímto trendem?

## Poznámky na konec
- Jelikož ACLED změnil a zpoplatnil přístup k datům, časové rozmezí dat projektu je neintuitivní. Jedná se totiž o data sesbíraná dříve pro účely diplomové práce autora.
- Výše zmíněné s sebou nese jedno omezení, a to, že se mezi sebou mohou srovnávat pouze celá čtvrtletí, nekompletními jsou totiž Q1 2022 (začátek války na konci února 2022) a Q1 2025 (konec sběru dat k 19.2.2025).
- Jelikož je dataset Massive Missile Attacks on Ukraine manuálně doplňován nezávislým jednotlivcem, započal zde sběr dat dne 28.9.2022. Chybí tedy údaje z prvotních měsíců války.

## Komentář k požadavkům na projekt
- V projektu byly vytvořeny následující metriky a kalkulované sloupce:
   - Metriky:
       - Celkový počet útoků
       - Dronové a raketové útoky
       - Počet útoků na Ukrajině
       - Počet útoků v Rusku
       - Průměrný počet útoků za čtvrtletí
       - Attack Effectiveness %
   - Sloupec "Čtvrtletí" v Appended_tables_UKR_RUS
