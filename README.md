# Deklinatora demo

Šis ir vienkāršs piemērs, kā var pielietot [Deklinators Node.js moduli](https://www.npmjs.com/package/deklinators) pārlūkprogrammas vidē.

Rezultāts ir apskatāms šeit: https://deklinators.s3.lv

## Sagatavošana web videi

Lai varētu izpildīt Node.js moduļu kodu tīmekļa pārlūka vidē, ir nepieciešams veikt dažus papildus soļus. Kādu utilītprogrammu izmantot šim nolūkam, ir gaumes jautājums. Šajā gadījumā tiek lietots [Browserify](https://browserify.org/). Ja šim repozitorijam ir izpildīta `npm install` komanda, tad zem `node_modules/.bin/` būs atrodama `browserify` utilītprogramma, kuru varam izmantot pārlūkprogrammai saprotama JavaScript faila sagatavošanai:

```
$ npx browserify index.js -s deklinators > deklinatorsBundle.js
```

Pēc šīs komandas izpildes tiek izveidots `deklinatorsBundle.js` fails, kas satur visu nepieciešamo JavaScript mūsu mazajai demonstrācijai. Uz mājas lapas servera tiek novietoti divi faili: `index.html` un `deklinatorsBundle.js`.