# Utjecaj imputacije podataka na uspješnost modela strojnog učenja

Ovaj projekt analizira kako različite metode imputacije nedostajućih vrijednosti utječu na performanse modela strojnog učenja s fokusom na klinički skup podataka o pacijentima s rakom dojke. Cilj je ukazati na važnost pravilnog rukovanja nedostajućim vrijednostima te kako svaki podatak može biti ključan za donošenje odluka.

## Ciljevi analize

U kliničkim podacima često nedostaju vrijednosti zbog tehničkih ograničenja, pogrešaka u unosu ili nemogućnosti dobivanja informacija. Nepravilno upravljanje takvim vrijednostima može dovesti do pristranih modela i pogrešnih zaključaka. Ova analiza istražuje:

- koje metode imputacije daju najstabilnije rezultate
- koliko se performanse modela razlikuju ovisno o vrsti imputacije
- koji modeli najbolje reagiraju na određene strategije imputacije

## Skup podataka

- **Izvor**: [cBioPortal: Breast Cancer (MSK, 2018)](https://www.cbioportal.org/study/clinicalData?id=breast_msk_2018)
- **Opis**: Klinički podaci o pacijentima s rakom dojke uključujući status hormona, menopauzalni status, stadij bolesti te ishode preživljavanja
- **Ciljna varijabla**: `Overall Survival Status` (ishod liječenja)
  
## Korištene metode imputacije i modeli strojnog učenja

### Imputacija podataka
- **SimpleImputer** 
- **KNNImputer**

### Modeli strojnog učenja
- **Logistička regresija** 
- **Random Forest** 

### Evaluacijske metrike
- Točnost (Accuracy)
- Preciznost (Precision)
- Odziv (Recall)
- F1-mjera

##  Zaključci

- Random Forest sa Simple Imputer-om je najučinkovitiji model - osigurava visoku točnost i ravnotežu između preciznosti i odziva za obje klase.
- Ostali modeli, osobito s KNN Imputer-om, pokazuju slabije rezultate.
