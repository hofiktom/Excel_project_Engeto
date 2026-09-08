# 📊 Analýza vzdělanostní struktury obyvatel v krajích ČR

## 📌 Popis projektu
Tento projekt se zaměřuje na zpracování a vizualizaci dat Českého statistického úřadu (ČSÚ) týkajících se úrovně dosaženého vzdělání v jednotlivých krajích České republiky. Cílem analýzy je poskytnout podklady pro Asociaci hejtmanů ohledně strukturálních rozdílů v regionech a identifikovat oblasti vyžadující zvýšenou podporu.

## 💾 Datové zdroje
Analýza vychází z oficiálních otevřených dat ČSÚ (Sčítání lidu, domů a bytů 2021):
* **Hlavní datová sada:** [Sčítání 2021 - Obyvatelstvo podle vzdělání](https://data.gov.cz/) (CSV distribuce)
* **Číselník:** [Vazba mezi číselníky ČSÚ: KRAJ_NUTS - CISOB](https://data.gov.cz/) pro přesné párování územních kódů s názvy krajů

## 🛠️ Použité nástroje a metody
* **Data Enrichment (`XLOOKUP`)**: Propojení kódů území z hlavní datové sady s číselníkem krajů pro dohledání oficiálních názvů krajů a čištění dat před samotnou agregací.
* **Microsoft Excel**: Kontingenční tabulky, dynamické výpočty, relativní podíly (% z řádku).
* **Datová vizualizace**: Skládané a kombinované grafy, úprava vizuálu (odstranění tlačítek polí, formátování os).
* **Metodika**: Agregace dat, hodnocení v absolutních vs. relativních ukazatelích, srovnání s celorepublikovým průměrem (benchmarking).

---

## 🔑 Klíčová zjištění (Executive Summary)

### 1. Základní a neukončené vzdělání (Absolutní počty)
* **Nejvyšší absolutní koncentrace:** Středočeský (148 tis.), Moravskoslezský (143 tis.) a Jihomoravský kraj (126 tis.).
* **Kategorie Bez vzdělání:** Nejvyšší absolutní počet lidí bez vzdělání má Ústecký kraj (7 794 obyvatel).
* *Poznámka:* Absolutní čísla jsou silně korelována s celkovou lidnatostí jednotlivých krajů.

### 2. Vysokoškolské vzdělání (Absolutní i relativní pohled)
* **Dominance metropole:** Hlavní město Praha vede v obou metrikách — žije zde **371 351 vysokoškoláků**, což představuje **33,70 %** populace kraje (každý 3. obyvatel).
* **Univerzitní centra:** Druhý nejvyšší podíl i počet vykazuje Jihomoravský kraj (**20,71 %** / 207 890 VŠ), což odpovídá silné akademické základně v Brně.
* **Srovnání s průměrem ČR:** Celorepublikový průměr činí **17,58 %**. Nad tímto průměrem se nachází výhradně Praha a Jihomoravský kraj.
* **Nejnižší podíl:** Karlovarský (**9,64 %**) a Ústecký kraj (**10,39 %**).

### 3. Celkové srovnání vzdělanostní struktury s průměrem ČR
* **Páteř vzdělání v ČR:** Středoškolské vzdělání tvoří přes **61 %** populace ČR (30,99 % bez maturity vs. 30,90 % s maturitou).
* **Regionální disparity:** Karlovarský a Ústecký kraj vykazují nadprůměrný podíl obyvatel se základním vzděláním (~16,7 % oproti 12,54 % průměru ČR) a zároveň nejvyšší podíl neodpovězených dat (Kategorie *Nezjištěno* > 8 %).

---

## 📁 Soubory v repozitáři
* `tomas_hofman_sldb2021_vzdelani.xlsx` – Kompletní datový model s načtenými daty ČSÚ, vzorci `XLOOKUP`, kontingenčními tabulkami a grafy.
