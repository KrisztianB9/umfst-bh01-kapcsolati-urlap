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
Elotte: <html>
Utana: <html lang="hu">
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
Elotte: <img src="logo.png" width="120" height="40">
Utana: <img src="logo.png" width="120" height="40" alt="ÁOK Dékáni Hivatal logó">
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

Elotte: .cim { colour: #0e7c66; font-size: 2rem; }
Utana: .cim { color: #0e7c66; font-size: 2rem; }
- **Hogyan tesztelted (W3C validátor, Lighthouse, Tab-bejárás, képernyőolvasó):**
A DevTools Styles paneljenek ellenorzese, vizualis ellenorzes.
- **Tanulság / érintett alapelv (pl. Szemantika előbb, stílus később; WCAG-kritérium):**
Szemantika es szintaxis pontossaga.

## 4. hiba
- **Hiba leírása és reprodukálása (lépések, böngésző, segédtechnológia):**
- **Gyökérok (melyik sor, melyik szabály sérül):**
- **Javítás (commit link, előtte/utána kódrészlet):**
- **Hogyan tesztelted (W3C validátor, Lighthouse, Tab-bejárás, képernyőolvasó):**
- **Tanulság / érintett alapelv (pl. Szemantika előbb, stílus később; WCAG-kritérium):**

## 5. hiba
- **Hiba leírása és reprodukálása (lépések, böngésző, segédtechnológia):**
- **Gyökérok (melyik sor, melyik szabály sérül):**
- **Javítás (commit link, előtte/utána kódrészlet):**
- **Hogyan tesztelted (W3C validátor, Lighthouse, Tab-bejárás, képernyőolvasó):**
- **Tanulság / érintett alapelv (pl. Szemantika előbb, stílus később; WCAG-kritérium):**

## 6. hiba
- **Hiba leírása és reprodukálása (lépések, böngésző, segédtechnológia):**
- **Gyökérok (melyik sor, melyik szabály sérül):**
- **Javítás (commit link, előtte/utána kódrészlet):**
- **Hogyan tesztelted (W3C validátor, Lighthouse, Tab-bejárás, képernyőolvasó):**
- **Tanulság / érintett alapelv (pl. Szemantika előbb, stílus később; WCAG-kritérium):**

## 7. hiba
- **Hiba leírása és reprodukálása (lépések, böngésző, segédtechnológia):**
- **Gyökérok (melyik sor, melyik szabály sérül):**
- **Javítás (commit link, előtte/utána kódrészlet):**
- **Hogyan tesztelted (W3C validátor, Lighthouse, Tab-bejárás, képernyőolvasó):**
- **Tanulság / érintett alapelv (pl. Szemantika előbb, stílus később; WCAG-kritérium):**

## Összegzés
- Mit tanultam:
- Melyik alapelv sérült a leggyakrabban:
