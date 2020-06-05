## **10 _Juni_** Typescript und Javascript

*[direkt zur Praktikumsaufgabe](#a--praktikumsaufgabe)*
*[direkt zu Q&A](#-qa-fragen-und-antworten)*

Lektion 07 - to be done


## Json (Java Script Object Notation)

JSON ist eine Syntax um Daten speichern und austauschen zu können und wurde ursprrünglich für JavaScript entwickelt, aber wird von vielen anderen Sprachen ebenfalls benutzt. JSON ist ein mit JavaScript-Objektnotation geschrieber Text. JSON ist ein Datenformat in dem Daten für Menschen les-/veränderbar abgespeichert weden.

- JSON steht für JavaScript-Objektnotation
- JSON ist ein lightweight Datenaustauschformat
- JSON ist leicht zu lesen/verstehen
- JSON ist sprachunabhängig

### Daten austauschen: 
Die Daten in JSON liegen in Textform vor, und wir können jedes TS/JavaScript-Objekt in JSON konvertieren und aus JSON einladen. JSON kann auch an und von einem Server gesendet werden. Wir können jedes beliebige vom Server empfangene JSON in TS/JavaScript-Objekte umwandeln.

Auf diese Weise können wir komfotabel mit den Daten als TS/JavaScript-Objekte arbeiten.

### Daten speichern
Wenn Sie Daten in einem TS/JavaScript-Objekt gespeichert haben, können Sie das Objekt in JSON konvertieren und an einen Server senden:

```TypeScript
let myObj: Person = {name: "John", age: 31, city: "New York"};
let myJSON: String = JSON.stringify(myObj);
```

### Einlesen von Daten
Wenn Sie Daten im JSON-Format erhalten, können Sie diese in ein TS/JavaScript-Objekt konvertieren:

```TypeScript
let myJSON: String = '{"name":"John", "age":31, "city":"New York"}';
let myObj: Person = JSON.parse(myJSON);
document.getElementById("demo").innerHTML = myObj.name;
```


### Typescript Dokumentation

https://www.typescriptlang.org/

## **A _---_** Praktikumsaufgabe

>**Bei Problemen/Unklarheiten:** können Sie ins Praktikum kommen oder per Discord/Mail fragen stellen.

tba

Erstellen Sie ein neues Verzeichnis und kopieren Sie die Dateien der letzten Aufgabe hinein. 

Die Aufgabe baut auf der Shop Aufgabe der letzten 3 Wochen auf. 

Ziel der Praktikumsaufgabe ist es Daten über mehrere HTML Seiten hinweg speichern zu können. In dieser Aufgabe geht es darum zu speichern welche Artikel von einem Kunden in den Warenkorb gelegt wurden. Außerdem sollen die auf der Website angezeigten Artikel per JSON geladen werden. 

>### **Achtung!:** Beachten Sie die [<ins>Coding Style Guidelines</ins>](https://hs-furtwangen.github.io/GIS-SoSe-2020/codingstyle/). Code der diesen Guidelines nicht entpricht wird nicht akzeptiert! Code der W3 Errors oder JS-Errors aufweist wird ebenfalls nicht akzeptiert! Verstöße fürhen zu einer Ampelstufe 🚦

## Teilaufgabe 1:

Bisher werden Ihre Artikel über ein sog. "hardcoded" Array eingelesen. Änderungen sind nur dann möglich wenn Sie das Array bearbeiten. Ein besserer Weg ist es deshalb die Daten und den Code voneinander zu trennen. Auf diese Art und Weise können jederzeit Artikel hinzugefügt oder aus dem Shop genommen werden.

Erstellen Sie ein JSON File mit allen Ihren Artikeln. Sie können dies von Hand oder mithilfe von online JSON Generatoren durchführen oder indem Sie folgenden Hinweis beachten.

>**Hinweis:** Damit Sie die JSON nicht von Hand befüllen müssen, können Sie mithilfe von `JSON.stringify(data_array)` aus Ihrem Daten-Array ein JSON Dokument erzeugen.

Lesen Sie nun die einzelnen Artikel, welche vorher in einem Array gespeichert waren aus der neun JSON Datei aus. 

>**Hinweis:** Die `fetch()` Methode funktioniert nur auf Servern. Wenn Sie also wie gewohnt die HTML Datei nur lokal auf Ihrer Maschine in den Bwoser ziehen, fnuktioniert `fetch()` nicht. Laden Sie Ihre Aufgabe für diesen Teil hoch & testen Sie dann.

Erzeugen Sie anhand der eingelesenen Daten die Artikel auf Ihrer Webseite.

>**Hinweis:** Es gibt mehrere Wege wie sie die Kategorie eines Artikels in einer JSON Datei speichern können. Sie können z. B. jeden Artikel mit einer "Kategorie-ID" versehen und die Artikel beim einlesen der JSON sortieren.

## Teilaufgabe 2:

Verwenden Sie hierfür den [localStorage](https://www.w3schools.com/jsref/prop_win_localstorage.asp). Wenn ein User der Website einen Artikel über einen der "Kaufen" Buttons in den Warenkorb legt, soll der jeweilige Artikel im local Storage gespeichert werden. 

Legen Sie eine Warenkorb Seite an (falls Sie noch keine haben). Auf der Warenkorb Seite werden alle Artikel die  ein User per Button in den Warenkorb gelegt hat dynamisch per Code generiert und angezeigt. Auf der Warenkorb Seite wird außerdem der Gesamtpreis der Bestellung angezeigt. 

User haben die Mögkichkeit einzelne Artikel zu entfernen. Jeder dynamisch generierte Artikel hat einen "Entfernen/Löschen" Button/Text.

User können ihren gesamten Warenkorb löschen. Hierfür gibt es ebenfalls einen Button, der den localStorage leert & die Artikel aus dem Warenkorb entfernt. 

## Bonusaufgabe (keine Pflicht):

User können einen Artikel mehrmals in den Warenkorb legen (z. B. 5 Äpfel). Im Warenkorb kann die Anzahl der Artikel eines Typs geändert werden.


### **Abgabetermin: 14.06.2020 um 18:00!**

Bitte erstellen Sie nach Fertigstellung einen Link als oberstes Element (unter dem GitHub issues link) in Ihrer Steckbrief.htm, der auf das Ergebnis verweist (bspw. nutzername.github.io/GIS-SoSe-2020/Aufgabe_6).

>### **Achtung!:** Eine fehlerhafte Abgabe fürt zu einer 🚦 die **im Praktikum** verteidigt werden muss. Keine Abgabe zu 2 🚦 von denen nur 1e 🚦 verteidigt werden kann.

---

## **?! _<small>Q&A</small>_** Fragen und Antworten

(die Publikation der Zusammenfassung erfolgt nach dem Q&A Termin)

Zusammenfassung von: [&lt;GitHub Nutzername&gt;](https://github.com/link-zu-github-profil)

### Erste Frage?
LoremLabore labore cillum mollit pariatur reprehenderit dolor laboris reprehenderit dolor sit officia ea non. Lorem reprehenderit exercitation labore eiusmod aute do nostrud officia aute proident sunt. Labore non tempor aliqua voluptate. Exercitation culpa officia ut aliqua nostrud laborum irure est. Minim eu sunt culpa adipisicing laborum consectetur aliqua quis.

### Zweite Frage?
Mollit aliquip veniam sit eiusmod tempor anim ipsum tempor. Aliqua sunt voluptate ea dolor. Nulla est mollit consectetur cupidatat ut cillum ipsum minim. Est ex et nulla laborum fugiat dolore. Aliquip laboris sint exercitation commodo dolor sint mollit qui sunt ipsum fugiat occaecat id enim.

## ...
