## **1 _JuLi_** Datenbanken Grundlagen

*[direkt zur Praktikumsaufgabe](#a--praktikumsaufgabe)*
*[direkt zu Q&A](#-qa-fragen-und-antworten)*

<img src="https://assets.amuniversal.com/b1e4d2d09fcd012f2fe600163e41dd5b">
<small>Quelle: <a href="https://dilbert.com/strip/1995-11-17">https://dilbert.com/strip/1995-11-17</a></small>  

# Datenbanken

Ein Server hält seine Daten grundsätzlich nur so lange vor, wie er läuft. Sobald er heruntergefahren wird (oder abstürzt), gehen die im Arbeitsspeicher & Variablen gespeicherten Daten verloren. Nun könnte man natürlich für jeden zu speichernden Datensatz (wie z.B eine Bestellung in unserem onlineshop) eine Datei anlegen (z. B. JSON), oder alle Daten irgendwie in einer großen Datei sammeln, allerdings sollten diese Daten ja auch schnell manipulierbar, durchsuchbar, analysierbar und vieles mehr sein. Schließlich sollten auch alte Bestellungen irgendwann gelöscht, alle Bestellungen eines bestimmten Kunden herausgesucht oder oder zur Optimierung des Angebots die Häufigkeit der Bestellung einer bestimmten Artikel-Kombination ermittelt werden können. Für all dies müssten wieder entsprechende Algorithmen und Datenstrukturen konzipiert implementiert werden. Da solche Anforderungen bei der Entwicklung interaktiver Anwendungen aber sehr häufig auftreten und oft ähnlich sind, gibt es bereits Standardsoftware, welche Daten speichert, verwaltet und auswertet: Datenbanksysteme!  

## Relationale Datenbanken
Seit den 1970er Jahren dominieren relationale Datenbanken, bei denen die Daten in Tabellenstrukturen untergebracht werden und durch Querverweise ein Netz von Tabellen aufgespannt wird, den IT Bereich. Mit der Structured-Query-Language (SQL) wurde eine Abfragesprache entwickelt, mit der komplexe Anweisungen formuliert werden können, welche eine jeweilige Datenbanksoftware dann selbständig ausführt um Daten aus dem Bestand zu liefern oder zu manipulieren. Heute ist insbesondere die Open-Source-Datenbanksoftware MySQL sehr weit im Internet verbreitet.
> **FunFact:** Dem Namen MySQL wird meist intuitiv die Bedeutung "MeinSQL" zugesprochen. Tatsächlich aber hat der finnische Entwickler Michael Widenius sein 1994 gestartetes Open-Source-Projekt nach seiner Tochter My benannt.

## NoSQL-Datenbanken
Mit dem durch das Internet stetig wachsenden Datenaufkommen wurde der Bedarf an Skalierungsmöglichkeiten immer größer. Die Leistung und Kapazität einer Datenbank sollte also während des Betriebs durch Einsatz von mehr Hardware einfach vergrößert werden können. Relationale Datenbanksysteme sind aber ursprünglich nicht dafür ausgelegt, die Daten zu verteilen. 
NoSQL bzw. dokumentenorientierte Datenbanken adressieren dieses Problem. Die zu verwaltenden Daten müssen dabei nicht in starr definierte Tabellenform gebracht werden, sondern jeder Datensatz kann als beliebig strukturiertes Dokument abgelegt werden.  
Das No in NoSQL bedeutet "Not only", es gibt also auch Systeme, die mit SQL arbeiten können. Dokumentenorientierte Datenbanken sind eine Variante der NoSQL-Datenbanken, es gibt noch andere.

## MongoDB
2009 wurde mit MongoDB eine NoSQL-Datenbanksoftware veröffentlicht, die Javascript als interne Sprache nutzt. Abfragen und Aggregationsfunktionen können direkt als Javascript-Anweisungen formuliert werden, außerdem können ganze Anweisungsfolgen zum Datenbanksystem geschickt und dort ausgeführt werden.  

> **FunFact:** Der Name MongoDB leitet sich von *humongous* ab, womit die groteske Größe der Datenmengen gemeint ist, die mit dieser Software verwaltet werden können.

Für Sie ist der riesige Vorteil der Nutzung dieser Datenbanksoftware, dass Sie keine weitere Abfrage- oder Programmiersprache lernen müssen. Die Anweisungen, die MongoDB für Node.js bereit stellt, sind auch in TypeScript definiert, so dass Sie sie mit der gewohnten Unterstützung einsetzen können, genauso wie die modernen Konzepte der ansynchronen Kommunikation mit dem Datenbanksystem wie `Promise` und `async/await`.  
Wenn auch viele aktuelle Anwendungen im Internet noch von JavaScript, PHP und MySQL dominiert sind, sind Sie mit Node.js, TypeScript und MongoDB sehr zukunftsträchtig aufgestellt.

Durch den Einsatz einer Datenbanksoftware ist es nicht mehr erforderlich, eine Datenverwaltung selbst zu entwickeln. Komplexität entsteht nun aber durch die Kommunikation zwischen den Systemen Client, Server und Datenbanksystem.


# Allgemeine Datenbankstruktur
```plaintext
MongoDB-Instanz (auch ggf. Cluster genannt)
├   admin
├   config
├   local
├ Database_1
├ Database_2
│ ├ Collection_1
│ ├ Collection_2
│ │ ├ {key: value, key: value, ...}
│ │ ├ {key: value, key: value, ...}
│ │ ├ {key: value, key: value, ...}
│ │ └ ...
│ ├ Collection_3
│ └ ...
├ Database_3
└ ...
``` 
- Eine MongoDB-Instanz kann mehrere Datenbanken verwalten.
- Die Datenbanken admin, config und local werden dabei standardmäßig angelegt und sind für die interne Funktionalität erforderlich
- Es können beliebig viele eigene Datenbanken angelegt werden
- In jeder Datenbank können beliebig viele Collections untergebracht sein
- Jede Collection enthält eine beliebige Anzahl an Dokumenten
- Ein Dokument ist im Wesentlichen lediglich ein JSON-String, bzw ein JSON Objekt

### Beispielstruktur für einen Onlineshop

Da jede Bestellung vom Server leicht in einen JSON-String umgewandelt wird, bietet es sich an, diese beispielsweise in einer Collection namens `orders` abzulegen. Das Angebot des Shops könnte in einer Collection `offers` liegen. Dabei wäre es möglich, das komplette Angebot als ein einziges Dokument abzulegen, so wie es derzeit auch vorliegt (als ein Array). Allerdings wäre die Funktionalität einer Datenbank besser genutzt, wenn man das Angebot auf mehrere Dokumente aufteilt. Diese könnten so aussehen:
```typescript
{ name: "Blue Shirt", price: 25.00, category: "Shirts" }
{ name: "Red Shirt", price: 24.99, category: "Shirts" }
{ name: "Fancy Tophat", price: 100.00, category: "Hats" }
...
```
Auch ist es möglich und vielleicht sinnvoll, eigene Collections für Shirts, Hats,  etc. anzulegen und darin für jeden Artikel ein eigenes Dokument.
```typescript
Collection Shirts
{ name: "Blue Shirt", price: 25.00 }
{ name: "Red Shirt", price: 24.99 }
...
Collection Hats
{ name: "Fancy Tophat", price: 100.00 }
{ name: "Cheap MAGA Hat (made in China)", price: 1.20}
...
```
Diese Collections könnte man auch in einer eigenen Datenbank für das Shop-Angebot anlegen und damit strenger von den Bestellungen trennen.  

> **Achtung:** Wie also die Informationen in Datenbanken strukturiert sein sollen, ist eine Designentscheidung, die Sie treffen müssen!

## Installation
Wie der Server kann auch die Datenbanksoftware als Service im Netz genutzt werden. Ebenso ist es aber sinnvoll, während der Entwicklung lokal testen zu können.
> - Installieren Sie MongoDB auf ihrer Maschine. Besuchen Sie hierzu das [MongoDB Manual](https://docs.mongodb.com/manual/administration/install-community/) (MongoDB **nicht** als Service und auch **nicht** MongoCompass installieren)
> - Finden Sie den Ordner, in den Sie MongoDB installiert haben. Darin sollten Sie die ausführbaren Programme `mongod` und `mongo` sehen.

Im unteren Beispiel wurde MongoDB in einem Ordner `Test` installiert, die Datenbanken sollen im Ordner `Database` angelegt werden.  

```plaintext
Test
├ MongoDB
│ └ bin
│   ├ mongod (ggf .exe)
├   └ ...
└ Database
```  

> - Um eine Datenbank anzulegen, rufen Sie in einem Terminal die Datenbanksoftware `mongod` auf und geben als Parameter "--dbpath" den Pfad zu dem Ordner an, in dem Sie die Datenbanken haben möchten. Den Ordner müssen Sie zuvor kreiert haben.   

Arbeitet das Terminal gerade im Ordner Test, dann lautet der Aufruf

```
MongoDB/bin/mongod --dbpath Database
``` 

**Hinweis:** Nutzen Sie hier besser das Terminal  (aka Kommandozeileninterpreter, Shell, Command, Konsole) ihres Betriebssystems. So können Sie besser mehrere Fenster kontrollieren als innerhalb von VSCode.

Wenn alles funktioniert, gibt MongoDB einige Meldungen im Terminal aus und unter den letzten befinden sich "Listening on ..." und "waiting for connections on port ...". Das Programm läuft jetzt offensichtich als Server auf ihrem Localhost und wartet am angegebenen Port auf Kommunikationspartner.

> - Schauen Sie nun den Inhalt des Datenbankordners an. MongoDB hat hier einige Informationen zur Verwaltung ihrer Daten abgelegt.

## Mongo Shell
Die eigentlichen Daten kann man so nicht einsehen, sie werden in einem effizienten Format gespeichert, das von Menschen nicht gut interpretiert werden kann. Um schnell und einfach von Hand die Datenbank einzusehen und zu manipulieren, bietet MongoDB einen eigenen Kommandozeileninterpreter an: die MongoShell. Dieser Client kann Javascript interpretieren, sich mit dem laufenden Datenbankserver verbinden, Anweisungen an diesen schicken und dessen Antworten ausgeben.  

> **Hinweis:** Wenn bei den nächsten Übungen etwas nicht funktionieren sollte, bitte direkt melden. Bis eine Antwort kommt, können Sie mit dem folgenden Video weiter machen...  

> - Öffnen Sie in einem zweiten Terminalfenster mit `mongo` die MongoShell. Beobachten Sie im ersten Fenster, dass MongoDB einen Verbindungsversuch registriert und diesen akzeptiert.
> - Geben Sie `show dbs` in der Shell ein, es sollten Infos zu den drei internen Datenbanken angezeigt werden.
> - Legen Sie mit `use Test` eine neue Datenbank mit Namen "Test" an. Die Shell bestätigt "switched to db Test". Test ist nun für die folgenden Befehle die Datenbank, mit der gearbeitet wird.
> - Geben Sie `show collections` ein. Da noch keine Collections in Test angelegt sind, sollte nichts ausgegeben werden. Tatsächlich wird auch `show dbs` noch nicht die Datenbank Test ausgeben, da diese noch leer ist.
> - Geben Sie ein `doc = {name: "...", firstname: "...", registration: "..."}` wobei Sie `...` jeweils mit ihrem Nachnamen, Vornamen und ihrer Matrikelnummer ersetzen. Damit erzeugen Sie eine Javascript-Variable namens `doc` und ein Objekt mit Informationen zu Ihnen, auf welches die Variable verweist.
> - Mit `db.Students.insert(doc)` fügen Sie nun den mit `doc` referenzierten Datensatz in eine Collection namens "Students" in die aktuelle genutzte Datenbank, also in Test, ein.
> - Lassen Sie wieder den Überblick über die Datenbanken und über die Collections in der Datenbank Test ausgeben. Test und darin Students sollten nun angezeigt werden. 
> - Den Inhalt der Collection lassen Sie sich jetzt mit `db.Students.find()` anzeigen. Ihr Datensatz sollte auftauchen, wobei dieser um einen Schlüssel "_id" mit einem zugehörigen Wert erweitert wurde. Jedes Dokument erhält nämlich automatisch eine eindeutige Identifikation. 
> - Tragen Sie mit `insert` erneut die Information von `doc` ein und vergleichen Sie, dass nun zwei identische Datensätze vorhanden sind, die sich nur aufgrund ihrer _id unterscheiden.
> - Tragen Sie noch weitere Datensätze mit Informationen zu Ihren Kommilitonen oder zu Fantasiestudis ein. Dabei sollte es Datensätze mit teilweise identischen Informationen geben, so wie man sie bei Geschwistern oder Studis mit gleichen Vornamen vorfindet. Sie können dabei weiter die Variable `doc` verwenden und vor jedem Eintrag die Information darin verändern, oder auch Datensätze direkt als Parameter der `insert`-Anweisung angeben, also `db.Students.insert({...})`
> - Suchen Sie nun mit `db.Students.find({key:value})` nach allen Datensätzen bei denen ein bestimmter Schlüssel `key` einen bestimmten Wert `value` hat.

Nachdem Sie diese Übungen erfolgreich abgeschlossen haben, können Sie nicht nur mit der MongoShell umgehen, sondern haben auch schon die grundlegendsten Anweisungen gelernt, die genauso auch im Code Verwendung finden. Sehr viel weitergehend ist die [Dokumentation](https://docs.mongodb.com/manual/reference/method/). Wenn es nicht richtig geklappt hat, können Sie untenstehendes Video anschauen, indem diese Übungen demonstriert werden. _(Auch hier gilt wieder: Das Video kommt aus dem EIA2 Kurs, darum sind manche Ordnerstrukturen oder Verweise für Sie nicht relevant.)_

<div align="center"><video controls width="30%"> 
  <source src="http://games.hs-furtwangen.de/EIA2_Video/L07_V1_MongoShell.mp4" type="video/mp4"> 
<a href="http://games.hs-furtwangen.de/EIA2_Video/L07_V1_MongoShell.mp4"><img src="../X01_Appendix/Img/video.jpg" width="25%"/></a>
</video>  
</div>

## Online Service - Eigenes Mongo DB Cluster anlegen
Die Datenbank auf dem Entwicklungsrechner ist natürlich nur zum Testen da, von Außen hat niemand darauf Zugriff. Die Bestellungen sollen aber in einer Datenbank gespeichert werden, die ständig und von überall aus erreichbar ist. MongoDB bietet mit Atlas ein eigenes Serviceangebot hierfür.

- Neuen Account & Cluster anlegen
  - Rufen Sie https://www.mongodb.com/ auf
  - Klicken Sie auf `Start Free` (mitte des Screens)
  - Melden Sie sich mit Namen und Mailadresse an
  - Wählen Sie `Create a cluster` unter den free Starter Clusters
  - Wählen Sie `AWS` und eine Free Cluster in `Europa` (Frankfurt sollte am schnellsten sein)
  - Wählen Sie einen `Clusternamen`, vielleicht deinen eigenen Namen oder "GIS-IST-GEIL"?
  - Klicken Sie auf `Create Cluster`
  - Warten Sie, bis das Cluster erstellt wurde (ca. 1-3 Minuten)

- Folgen Sie jetzt dem `Get Started`-Guide! https://docs.atlas.mongodb.com/getting-started/
  - Erlauben Sie ihrem Testuser den Read/Write-Zugriff
  - Erlauben Sie in der Whitelist Zugriff von überall mit der IP-Adresse `0.0.0.0/0`
  - Legen Sie **`KEINE`** Beispieldaten an
  - Wählen Sie `Connect Your Application` und kopieren Sie den Connection-String -> legen Sie ihn zunächst als Kommentar in Ihrem Servercode ab.
- Wählen Sie dann Collections-> Add my own data
  - Legen Sie eine Datenbank `Test` und die Collection `Students` an
  - Klicken Sie auf `Insert Document` und fügen Sie in `Students` ein Dokument ein
  - Experimentieren Sie mit den Icons an dem Dokument

### Typescript Dokumentation

https://www.typescriptlang.org/

## **A _---_** Praktikumsaufgabe

>**Bei Problemen/Unklarheiten:** können Sie ins Praktikum kommen oder per Discord/Mail fragen stellen.

### Aufgabenteil 1
Gehen Sie die oben beschriebenen Schritte für eine lokale Mongo Installation durch.

### Aufgabenteil 2
Gehen Sie die oben beschreibenen Schritte für den Online Service durch und legen Sie dort eine Datenbank an. Experimentieren Sie auch hier mit Collections und Dokumenten, erstellen, manipulieren und löschen Sie mehrere davon. Kreieren Sie außerdem einen User für diese Datenbank, um darauf zugreifen zu können.

Als Abgabe verlinken Sie auf Ihrem Steckbrief einen Link auf die Web-Anwendung [https://mongodbnetbrowser.herokuapp.com/](https://mongodbnetbrowser.herokuapp.com/) und ergänzen sie diesen um die richtigen GET-Query-Parameter, so dass der Inhalt einer gut gefüllten Collection Ihrer mongodb.net/com-Datenbank beim Anklicken des Links angezeigt wird.


>### **Achtung!:** Beachten Sie die [<ins>Coding Style Guidelines</ins>](https://hs-furtwangen.github.io/GIS-SoSe-2020/codingstyle/). Code der diesen Guidelines nicht entpricht wird nicht akzeptiert! Code der W3 Errors oder JS-Errors aufweist wird ebenfalls nicht akzeptiert! Verstöße führen zu einer Ampelstufe 🚦

### **Abgabetermin: 05.07.2020 um 18:00!**

Bitte erstellen Sie nach Fertigstellung einen Link als oberstes Element (unter dem GitHub issues link) in Ihrer Steckbrief.htm, der auf das Ergebnis verweist.

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
