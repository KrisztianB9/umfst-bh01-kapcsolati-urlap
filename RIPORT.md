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

Elotte: <html>
Utana: <html lang="hu">
- **Hogyan tesztelted (W3C validátor, Lighthouse, Tab-bejárás, képernyőolvasó):**
Lighthouse Accessibility audit hibat ad vissza, illetve kepernyoolvasoval valo meghallgatas.
- **Tanulság / érintett alapelv (pl. Szemantika előbb, stílus később; WCAG-kritérium):**
A weboldal nyelvenek programozottan azonisithatonak kell lennie.