# A dékáni hivatal „működő” kapcsolati űrlapja – hibariport

Repó: https://github.com/KrisztianB9/umfst-bh01-kapcsolati-urlap
Készítette: Bacso Krisztian, InfoLM3

## 1. hiba 
- **Hiba leírása és reprodukálása (lépések, böngésző, segédtechnológia):** 
A kepernyoolvaso angol kiejtessel probalja felolvasni a magyar szoveget, ami erthetetlenne teszi ezt. 
Reprodukalas: oldal megnyitasa bongeszoben bekapcsolt kepernyoolvasoval.
- **Gyökérok (melyik sor, melyik szabály sérül):**
A 2. sorban hianyzik a <html> nyito tagbol a nyelv meghatarozasa. 
- **Javítás (commit link, előtte/utána kódrészlet):**
  https://github.com/KrisztianB9/umfst-bh01-kapcsolati-urlap/commit/84b403a35839c12d8382ecaa400cf1373535d29b
- **Hogyan tesztelted (W3C validátor, Lighthouse, Tab-bejárás, képernyőolvasó):**
Lighthouse Accessibility audit hibat ad vissza, illetve kepernyoolvasoval valo meghallgatas.
- **Tanulság / érintett alapelv (pl. Szemantika előbb, stílus később; WCAG-kritérium):**
A weboldal nyelvenek programozottan azonisithatonak kell lennie.

## 2. hiba
- **Hiba leírása és reprodukálása (lépések, böngésző, segédtechnológia):**
A kepernyoolvaso a fejlecben talalhato logohoz erve a fajl nevet olvassa fel.
Reprodukalas: oldal bejarasa kepernyoolvasolval.
- **Gyökérok (melyik sor, melyik szabály sérül):**
A 11. sorban az <img> tagbol hianyzik az alt attributum.
- **Javítás (commit link, előtte/utána kódrészlet):**
  https://github.com/KrisztianB9/umfst-bh01-kapcsolati-urlap/commit/e7cdf95522522cf2883156c1281218ccfc3f2074
- **Hogyan tesztelted (W3C validátor, Lighthouse, Tab-bejárás, képernyőolvasó):**
W3C validator, kepernyoolvaso teszt.
- **Tanulság / érintett alapelv (pl. Szemantika előbb, stílus később; WCAG-kritérium):**
Minden nem-szoveges tartalomnak rendelkeznie kell szoveges alternativaval, hogy a latasserultek is ertsek.

## 3. hiba
- **Hiba leírása és reprodukálása (lépések, böngésző, segédtechnológia):**
A <h1> elem szovege fekete szinu marad, pedig a CSS-ben beallitottuk zoldre.
Reprodukalas: az oldal megnyitasa.
- **Gyökérok (melyik sor, melyik szabály sérül):**
a CSS kod 3. soraban a color attributum el van gepelve colour-ra, ezert nem ismeri fel.
- **Javítás (commit link, előtte/utána kódrészlet):**
  https://github.com/KrisztianB9/umfst-bh01-kapcsolati-urlap/commit/30de42a638b9663d02871a54ee0cda8859e89bc1
- **Hogyan tesztelted (W3C validátor, Lighthouse, Tab-bejárás, képernyőolvasó):**
A DevTools Styles paneljenek ellenorzese, vizualis ellenorzes.
- **Tanulság / érintett alapelv (pl. Szemantika előbb, stílus később; WCAG-kritérium):**
Szemantika es szintaxis pontossaga.

## 4. hiba
- **Hiba leírása és reprodukálása (lépések, böngésző, segédtechnológia):**
A kepernyoolvaso a beviteli mezokre lepve csak annyit mond: "szerkesztes, ures". Mivel csak placeholder van, ahogy elkezdunk gepelni, a kepernyoolvaso elnemul es a latasserult elveszti a kontextust.
Reprodukalas: oldal megnyitasa es kepernyoolvasoval valo bejaras.
- **Gyökérok (melyik sor, melyik szabály sérül):**
Az urlapmezoknek (input,select,textarea) nincsen label cimke elemei. A fejleszto csak placeholder elemeket hasznalt.
- **Javítás (commit link, előtte/utána kódrészlet):**
  https://github.com/KrisztianB9/umfst-bh01-kapcsolati-urlap/commit/54a80159a6a83f93d6194134442610ccb84fc955
- **Hogyan tesztelted (W3C validátor, Lighthouse, Tab-bejárás, képernyőolvasó):**
Lighthouse Accessibilty audit, kepernyoolvasasos teszteles.
- **Tanulság / érintett alapelv (pl. Szemantika előbb, stílus később; WCAG-kritérium):**
A placeholder soha nem helyettesiti a label-t.

## 5. hiba
- **Hiba leírása és reprodukálása (lépések, böngésző, segédtechnológia):**
Mobilon az email cim mezore kattintva a hagyomanyos billentyuzet jelenik meg, ahol nincs mar egybol @ szimbolum. Emellett az urlap bekuldheto olyan email cimmel, hogy "alma", ami nyilvanvaloan nem email cim.
Reprodukalas: mobilon rakattintani a mezore, tesztadat beirasa.
- **Gyökérok (melyik sor, melyik szabály sérül):**
Az email cim bekeresere szolaglo <input> type-ja text-re van rakva, ami egy sima szoveges mezo.
- **Javítás (commit link, előtte/utána kódrészlet):**
  https://github.com/KrisztianB9/umfst-bh01-kapcsolati-urlap/commit/cd60e4d3319e36a556f33f0316c1da8f5d975f83
- **Hogyan tesztelted (W3C validátor, Lighthouse, Tab-bejárás, képernyőolvasó):**
Mobilos bongeszo es az urlap kitoltese @ nelkul. Hibat dob vissza nelkule.
- **Tanulság / érintett alapelv (pl. Szemantika előbb, stílus később; WCAG-kritérium):**
A megfelelo szemantikus input tipus hasznalata drasztikusan noveli a mobilelmenyt, illetve ad egy alapveto biztonsagi reteget.

## 6. hiba
- **Hiba leírása és reprodukálása (lépések, böngésző, segédtechnológia):**
W3C validator sulyos hibat jelez az utolso sorokban, tab billentyuvel navigalva ketszer kell kattintani hogy atugorjunk a gombon.
- **Gyökérok (melyik sor, melyik szabály sérül):**
A 29. sorban a gomb egy anchor tagbe van csomagolva. Mivel mind az <a> es a <button> fokuszalhato elem, a bongeszo ket kulon Tab-megallot hoz letre.
- **Javítás (commit link, előtte/utána kódrészlet):**
  https://github.com/KrisztianB9/umfst-bh01-kapcsolati-urlap/commit/48d25d5a8c787cdd25683a55517fcc5677890e59
- **Hogyan tesztelted (W3C validátor, Lighthouse, Tab-bejárás, képernyőolvasó):**
W3C validator, es billentyuzetes bejaras.
- **Tanulság / érintett alapelv (pl. Szemantika előbb, stílus később; WCAG-kritérium):**
Urlap bekuldesehez nincs szukseg <a> linkre, a <button> elem onmagaban elvegzi ezt a feladatot.

## 7. hiba
- **Hiba leírása és reprodukálása (lépések, böngésző, segédtechnológia):**
Billentyuzettel navigalva az urlapon nem lathato semmilyen vizualis visszajelzes, hogy eppen hol tartunk.
- **Gyökérok (melyik sor, melyik szabály sérül):**
A CSS kod 6. soraban az outline: none; letiltja az alapmeretezett bongeszos fokuszkeretet es nem ad helyette semmilyen alternativ vizualis jelzest.
- **Javítás (commit link, előtte/utána kódrészlet):**
  https://github.com/KrisztianB9/umfst-bh01-kapcsolati-urlap/commit/56d05918390bb8279343b670c5c51ff8c8bcdd5d
- **Hogyan tesztelted (W3C validátor, Lighthouse, Tab-bejárás, képernyőolvasó):**
Lighthouse Accessibility audit, billentyuzetes bejaras.
- **Tanulság / érintett alapelv (pl. Szemantika előbb, stílus később; WCAG-kritérium):**
Sose tavolitsuk el az outline: none; beallitassal a fokuszkeretet, vagy adjunk meg helyette egy jol lathato fokuszbeallitast.

## Összegzés
- Mit tanultam: Az accessibility nem csupan egy extra kenyelmi funkcio, hanem a helyes HTML szemantika es CSS alapveto kovetelmenye. A vizualis visszajelzesek, a beviteli mezok pontos azonositasa elengedhetetlen a kisegito technologiak es a billentyuzetes hasznalat szamara.
- Melyik alapelv sérült a leggyakrabban: A vizualis es kisegito visszajelzesek elhagyasa (hianyzo lang, alt, label elemek, illetve letiltott "outline").
