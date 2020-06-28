## **8 _JuLi_** Datenbankzugriff über Server
*[direkt zur Praktikumsaufgabe](#a--praktikumsaufgabe)*
*[direkt zu Q&A](#-qa-fragen-und-antworten)*



## MongoDB in Node
Bisher wurde die Datenbank noch direkt über die MongoShell angesprochen. Damit wir aber die Datenbank ohne manuelles Zutun verwenden können, müssen wir diese mit unserem Node.JS Server verbinden. Was eben von Hand mit der MongoShell erledigt wurde, soll also das Node.js-Programm bewerkstelligen. Hierzu muss Node zunächst um die entsprechenden Module für die Arbeit mit MongoDB erweitert werden. Führen Sie also die Kommandos `npm install @types/mongodb` sowie `npm install mongodb` auf der obersten Ebene ihres GIS-Projektes / Repositories aus. 

Die Datei `package.json` sollte nun neue Einträge unter `dependencies` aufweisen, welche auf die Module und Versionen von MongoDB verweisen. Damit weiß dann auch z.B. Heroku, mit welchen Modulen das Projekt arbeitet, ohne dass diese Module im Github-Repository mitgeliefert werden. Überprüfen Sie zudem noch einmal die Datei `.gitignore`, damit nicht versehentlich diese Module in Ihre Versionskontrolle geraten.

Das Node-Modul `mongodb` stellt verschiedene Standardobjekte zur Verfügung, mit denen die Datenbankoperationen innerhalb der Node-Umgebung ausgeführt werden können. Wie zuvor die Module `http` und `url` wird auch `mongodb` importiert, in diesem Fall z.B. als `Mongo`: 
```typescript
import * as Mongo from "mongodb";
```

### MongoClient
Stellt, wie zuvor die MongoShell, innerhalb der Node-Umgebung eine Verbindung mit dem Datenbanksystem her. Ein neues MongoClient-Objekt erwartet für seine Erzeugung als Parameter einen URL und gegebenenfalls noch Zusatzoptionen. Seine Methode `connect` liefert eine Promise, auf deren Erfüllung gewartet werden kann.
```typescript
let mongoClient: Mongo.MongoClient = new Mongo.MongoClient(_url, options);
await mongoClient.connect();
```

### Collection
Eine Variable von diesem Typ referenziert direkt eine Collection der Datenbank. Darauf können dann die aus der MongoShell bekannten Operationen ausgeführt werden. 
```typescript
let orders: Mongo.Collection = mongoClient.db("Cocktailbar").collection("Orders");
orders.insert({...});
```

## Implementation

<div align="center"><video controls width="30%"> 
  <source src="http://games.hs-furtwangen.de/EIA2_Video/L07_V3_Implementation.mp4" type="video/mp4"> 
<a href="http://games.hs-furtwangen.de/EIA2_Video/L07_V3_Implementation.mp4">Video</a>
</video>    
</div>

## Test
> - Starten Sie den Server in einem dritten Terminalfenster. MongoDB sollte den Verbindungsversuch erkennen und eine zweite Connection anzeigen.
> - Starten Sie den Client in einem kleinen neuen Browserfenster. Am besten ordnen Sie die Fenster so an, so dass Ihr Bildschirm nun horizontal und vertikal halbiert erscheint. 
> - Setzen Sie mit dem Client mehrere unterschiedliche Anfragen ab und beobachte die Ausgaben im Serverfenster. 
> - Fragen Sie mit der MongoShell die Collection "Orders" der Datenbank "Cocktail" ab um zu schauen, ob die Bestellungen/Datensätze eingetragen wurden (oder eben welche Benennung Sie gewählt haben).
> - Ersetzen Sie nun im Servercode den URL zum Datenbankserver mit dem von ihrer remote DB kopierten Connection-String (s. L10). Sie können ihn sich auch unter Clusters->Connect noch einmal anzeigen lassen.
> - Starten Sie ihren lokalen Server neu. Setzen Sie mit dem Client weitere Datensätze ab und prüfen Sie in Atlas ob die Datensätze in der Online-Datenbank ankommen.

<div align="center"><video controls width="30%"> 
  <source src="http://games.hs-furtwangen.de/EIA2_Video/L07_V4_Test.mp4" type="video/mp4"> 
<a href="http://games.hs-furtwangen.de/EIA2_Video/L07_V4_Test.mp4"><img src="../X01_Appendix/Img/video.jpg" width="25%"/></a>
</video>    
</div>

### Ausbau 
> - Erweiteren Sie ihren Server derart, dass beim Start ein Argument entgegen genommen (z.B. eine der beiden Zeichenketten "local" und "remote") und anhand dessen entschieden wird, ob die lokale oder die Online-Datenbank genutzt wird.
> - Lassen Sie nun Heroku Ihren Server bauen. Passen Sie dazu die Steuerdatei `package.json` so an, dass der Pfad zum neuen Server eingetragen ist und bei der Startanweisung das Argument mitgegeben wird z.B. 
  ```typescript
  "scripts": {
    "start": "node PfadZumServer/Server.js remote"
  },
  ```
> - Implementieren Sie eine Funktion retrieveOrders, welche mit `orders.find()` alle Bestellungen ausliest und ein Array von `Orders` zurückliefert. Nutzen Sie dazu die asynchrone Funktion `toArray()` des Cursor-Objektes.
> - Implementieren Sie eine Erweiterung der Funktion `handleRequest`, so dass retrieveOrders aufgerufen und das Ergebnis als (JSON-)Zeichenkette in die Serverantwort eingefügt wird, wenn der Server dazu aufgefordert wird, z.B. mit dem Query-String `command=retrieve`, oder unter einem eigenen Pfad `/retrieve`. Eine Clientsoftware könnte damit die Datensätze abrufen.

### Typescript Dokumentation

https://www.typescriptlang.org/

## **A _---_** Praktikumsaufgabe

>**Bei Problemen/Unklarheiten:** können Sie ins Praktikum kommen oder per Discord/Mail fragen stellen.

Legen Sie eine HTML Seite an, auf der sich folgendes befindet:
- ein simples Formular (mit mindestens 3 verschiedenen Eingabefeldern)
- ein Bereich (z.B. ein div oder ein output) in dem eine Serverantwort angezeigt werden kann
- zwei Buttons die folgendes auslösen sollen:
  - Versand der im Formular eingegebenen Daten an den Server, welcher die Daten in Ihre remote Datenbank schreibt. (Bonus: leeren Sie das Formular danach)
  - Anfrage an den Server, die in der Datenbank gespeicherten Daten abzufragen und zurück zu geben. Die zurück gegebenen Daten werden im designierten Ausgabefeld als JSON String angezeigt. (Bonus: Formatieren Sie die zurückgegebenen Daten in sinnvoller Weise)
- (Bonus: Fügen Sie den ausgegebenen Objekten je einen Button hinzu, welcher es dem Nutzer erlaubt, die Daten wieder aus der Datenbank zu entfernen (natürlich wieder über eine Serveranfrage, welche dann die Daten wieder aus der Datenbank entfernt)).

#### Lösungshinweise:
- evtl kann es sinnvoll sein (besonders bei der Bearbeitung der Bonusaufgaben), den Code für die Datenbank auf dem Server in eine eigene Datei auszulagern.
- Testen Sie auf jeden Fall erstmal alles lokal, dann mit ihrer remote Datenbank, dann mit github pages.
- Testen Sie ausgiebig auch andere Datenbank-Funktionalitäten mit Ihrem Node Server, um ein Gefühl dafür zu bekommen, wie der Server mit der Datenbank kommuniziert, welche Rückgabewerte man bekommt, etc.

>### **Achtung!:** Beachten Sie die [<ins>Coding Style Guidelines</ins>](https://hs-furtwangen.github.io/GIS-SoSe-2020/codingstyle/). Code der diesen Guidelines nicht entpricht wird nicht akzeptiert! Code der W3 Errors oder JS-Errors aufweist wird ebenfalls nicht akzeptiert! Verstöße führen zu einer Ampelstufe 🚦

### **Abgabetermin: 12.07.2020 um 18:00!**

Bitte erstellen Sie nach Fertigstellung einen Link als oberstes Element (unter dem GitHub issues link) in Ihrer Steckbrief.htm, der auf das Ergebnis verweist (bspw. nutzername.github.io/GIS-SoSe-2020/Aufgabe_11). Außerdem einen Link zu ihrem Servercode auf Github.com.

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
