## **24 _Juni_** Server Request Verarbeitung

*[direkt zur Praktikumsaufgabe](#a--praktikumsaufgabe)*
*[direkt zu Q&A](#-qa-fragen-und-antworten)*

Inhalte: 
- Node.js URL Modul
- handleRequest aus EIA2-Inverted L06
- s. auch Implementation 2 Video(s)

- POST Anfrage über fetch und Auslesen auf Serverseite (vllt nur in die Bonusaufgabe rein? Oder ein Vermerk dass "nicht Prüfungsrelevant"?)

Beispielcode Clientseite
```typescript
await fetch(serverAddress, {
  method: "POST",
  headers: {
    "Content-Type": "text/plain",
  },
  body: JSON.stringify(data)
});
```
Beispielcode Serverseite
```typescript
if (_request.method == "POST") {
  let body = "";
  _request.on("data", data => {
    body += data;
  });
  _request.on("end", async () => {
    let post: any = JSON.parse(body);
  });
}
```


### Was Sie jetzt im Prinzip können:
- asynchrone Kommunikation
- Server-Client Kommunikation
- Daten
  - schicken
  - empfangen
  - aufbereiten
  - umwandeln


### Typescript Dokumentation

https://www.typescriptlang.org/

## **A _---_** Praktikumsaufgabe

>**Bei Problemen/Unklarheiten:** können Sie ins Praktikum kommen oder per Discord/Mail fragen stellen.

### Aufgabe 1

Ändern Sie den Servercode dahingehend, dass er statt einfach nur einem URL Bounce die in der URL (im query Teil / über eine GET Anfrage) übergebenen Variablen und Werte zunächst in ein Javascript Objekt / Assoziatives Array umwandelt, bzw diese aus der URL ausließt (s. `Url.parse()`). Geben Sie nun unter verschiedenen Pfaden die Informationen auf verschidene Weisen zurück:

- unter `/html` formatieren Sie die übergebenen Daten gut lesbar als HTML Text/Code. Dieser zurückgegebene HTML Code soll nun auf der Formularseite einfach als Antwort des Servers in die Seite ohne weitere Formatierungen eingebunden werden.
- unter `/json` formatieren Sie die übergebenen Daten als JSON Objekt und geben das zurück. Auf der Formularseite parsen Sie dieses in ein JS Objekt und geben dieses auf der Konsole aus. Vergleichen Sie (mit bloßem Auge) das Objekt welches Sie zurück bekommen haben mit dem Objekt das sie los geschickt haben. Wenn die Objekte gleich sind, haben Sie alles richtig gemacht.

### Bonusaufgabe

Versuchen Sie, statt über GET über POST eine Anfrage zu verschicken und auszulesen. Legen Sie dazu am besten eine neue HTML Seite an, mit einem ganz simplen "Login" Bereich (Benutzername/Email, Passwort, Button). Verschicken Sie die Daten mit `fetch()`, lesen sie die Daten auf der Serverseite aus, und schicken Sie diese in einer gut formatierten Form zurück (um überprüfen zu können, dass die Daten auch wirklich angekommen sind). Alternativ können Sie die übergebenen Daten auch mit (vorher festgelegten) "korrekten" Logindaten auf der Serverseite überprüfen und dann stattdessen als Serverantwort das Ergebnis des Loginversuchs zurückgeben.

>### **Achtung!:** Beachten Sie die [<ins>Coding Style Guidelines</ins>](https://hs-furtwangen.github.io/GIS-SoSe-2020/codingstyle/). Code der diesen Guidelines nicht entpricht wird nicht akzeptiert! Code der W3 Errors oder JS-Errors aufweist wird ebenfalls nicht akzeptiert! Verstöße führen zu einer Ampelstufe 🚦

### **Abgabetermin: 28.06.2020 um 18:00!**

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
