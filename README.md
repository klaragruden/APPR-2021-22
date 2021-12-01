# Analiza podatkov s programom R - 2021/22

Repozitorij za projekt pri predmetu APPR v študijskem letu 2021/22. 

## Analiza rodnosti

V projektni nalogi bom analizirala podatke za obdobje od leta 2000 do leta 2020.

V prvem delu se bom osredotočila na Slovenijo. Analizirala bom število živorojenih otrok na starost in izobrazbo matere ter število rojenih po regijah.
V drugem delu pa bom po svetu opazovala povezavo med robnostjo in številom splavov z BDP-jem države.  


1.tabela: število rojenih po dnevih

* Leto (integer)
* Mesec (integer)
* Dan (integer)
* Število rojenih (integer)
vir: https://pxweb.stat.si/SiStatData/pxweb/sl/Data/Data/05J1031S.px/ (CSV)



2.tabela: živorojeni po starosti in izobrazbi matere
 

* Leto (integer)
* Starost matere (integer)
* Izobrazba matere (character)
* Vrstni red rojstva (integer)
* Število živorojenih (integer)
vir: https://pxweb.stat.si/SiStatData/pxweb/sl/Data/-/05J1027S.px (CSV)


3.tabela: rojsta po spolu in statističnih regijah

* Leto (integer)
* Živorojeni (integer)
* Mrtvorojeni (integer)
* Spol (character)
* Regija (character)

vir: https://podatki.nijz.si/Selection.aspx?px_path=NIJZ%20podatkovni%20portal__1%20Zdravstveno%20stanje%20prebivalstva__03%20Porodi%20in%20rojstva&px_tableid=PIS_TB_6.px&px_language=sl&px_db=NIJZ%20podatkovni%20portal&rxid=e282d9e8-19d0-451f-a4de-e7d2147cc4b1 (HTML)


4.tabela: rodnost
* Leto (integer)
* Država (character)
* Rodnost (število otrok, ki se rodi v letu na 1000 prebivalcev) (double)
 
5.tabela: število prebivalcev
* Leto (integer)
* Država (character)
* Število prebivalcev (integer)

6.tabela: BDP držav
* Leto (integer)
* Država (character)
* BDP (double)

7.tabela: število splavov
* Leto (integer)
* Država (character)
* Število splavov (integer)


viri: (CSV)
- https://data.oecd.org/pop/population.htm
- https://gateway.euro.who.int/en/indicators/hfa_587-7011-number-of-abortions-all-ages/
- https://data.worldbank.org/indicator/SP.DYN.CBRT.IN?end=2019&start=2019&view=map




## Program

Glavni program in poročilo se nahajata v datoteki `projekt.Rmd`.
Ko ga prevedemo, se izvedejo programi, ki ustrezajo drugi, tretji in četrti fazi projekta:

* obdelava, uvoz in čiščenje podatkov: `uvoz/uvoz.r`
* analiza in vizualizacija podatkov: `vizualizacija/vizualizacija.r`
* napredna analiza podatkov: `analiza/analiza.r`

Vnaprej pripravljene funkcije se nahajajo v datotekah v mapi `lib/`.
Potrebne knjižnice so v datoteki `lib/libraries.r`
Podatkovni viri so v mapi `podatki/`.
Zemljevidi v obliki SHP, ki jih program pobere,
se shranijo v mapo `../zemljevidi/` (torej izven mape projekta).
