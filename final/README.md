## **Ω _---_** Prüfungsaufgabe und mündliche Prüfung

*[direkt zu Q&A](#-qa-fragen-und-antworten)*

Die Modulprüfung zu GIS besteht im Sommersemester 2020 aus einer Prüfungsaufgabe und einer mündlichen Prüfung. Die Lösung der Prüfungsaufgabe und die mündliche Prüfung ersetzen zusammen die schriftliche Klausur, die dieses Semester nicht durchgeführt werden kann. Zum Bestehen der Modulprüfung müssen beide Prüfungsteile erfolgreich abgeschlossen werden.

Ihnen stehen drei Aufgabenstellungen zur Wahl ([siehe unten](#prüfungsaufgaben-zur-wahl)), die Sie selbstständig bearbeiten sollen. Die Lösung der Aufgabe ist im besten Fall eine lauffähige Anwendung, die der jeweiligen Beschreibung genügt ([siehe unten](#hinweise-zur-abgabe-der-prüfungsaufgabe)).

Die Bewertung der Aufgabenlösungen folgt einem einheitlichen [Kriterienkatalog](criteria). Sie werden in der mündlichen Prüfung aufgefordert die Details der Implementierung Ihrer Lösung zu erläutern.

Der letztmögliche **Abgabetermin für die Lösung der Prüfungsabgabe** ist **Sonntag, 26. Juli 2020, 23:59.**

Die mündliche Prüfung besteht aus einer detaillierten Auseinandersetzung mit Ihrer Lösung der gewählten Prüfungsaufgabe und allgemeinen Fragen zu den Lehrinhalten des Moduls. 

Die **mündlichen Prüfungen** finden am **3., 4. und 5. August** statt (weitere Prüfungen am 6. August sind möglich).

### Hinweise zur Prüfungsanmeldung
⚠ **Achtung: veränderte Modalitäten zur Prüfungsanmeldung seit Dienstag, 14. Juli** ⚠

Um an der Modulprüfung teilzunehmen müssen Sie sich bis spätestens 26. Juli 2020 in das [FELIX-Kursmodul *GIS Modulprüfung SoSe 2020 (MIB und OMB)*](https://felix.hs-furtwangen.de/auth/RepositoryEntry/3983966357) einschreiben. Dieses Kursmodul bietet die Infrastruktur für folgende Schritte zur Moduleprüfung:
1. Abgabe der *Einwilligungserklärung zur Durchführung von Online-Prüfungen*
2. Eintragung eines Termins für die mündliche Prüfung
3. Abgabe der Lösung der Prüfungsaufgabe (siehe unten)

Die Abgabe der Einwilligungserklärung ist Vorraussetzung um zur mündlichen Prüfung zugelassen zu werden. Die Eintragung eines Prüfungstermins für die mündliche Prüfung sowie die Abgabe ihrer Lösung der Prüfungsaufgabe ist erst nach Abgabe der Einwilligungserklärung möglich.

### Allgemeine Hinweise zur Prüfungsaufgabe

- Jeder muss eine **eigene Lösung** erarbeiten! Unter diesem Gesichtspunkt ist Gruppenarbeit nur sehr eingeschränkt bei allgemeineren Problemen möglich. So wie die Aufgaben gestellt sind, ist es äußerst unwahrscheinlich, dass es zwei oder mehr gleiche (oder verdächtig ähnliche) Lösungen gibt. Einander gleichende Lösungen werden nicht akzeptiert.

- Implementieren Sie Ihre Lösung der gewählten Endaufgabe syntaktisch korrekt mit Hilfe von *HTML*, *CSS*, *Typescript*, *NodeJS* und *MongoDB*.

- Testen Sie die Applikation regelmäßig, ausgiebig und frühzeitig. Lassen Sie auch andere Personen testen um festzustellen, ob die Anwendung bedienbar und fehlertolerant ist. 

- Die Aufgaben lassen nicht zufällig einiges an Interpretationsspielraum. Toben Sie sich aus, machen Sie sich Gedanken, **seien Sie kreativ**, **haben Sie Spaß**.

- Die Prüfungsaufgabe ist **nicht** Teil des Praktikums und muss für das Bestehen des Praktikums nicht abgegeben werden.

### Hinweise zur Abgabe der Prüfungsaufgabe
⚠ **Achtung: veränderte Abgabemodalitäten seit Dienstag, 14. Juli** ⚠

- Verwenden Sie – wie für die Praktikumsaufgaben – ein *GitHub* Repository für den Quellcode und die damit assoziierten *GitHub Pages* um die – möglichst lauffähige und vollständige – Anwendung zugänglich zu machen (siehe [Einführung vom 22. April](../L01)).

- Laden Sie im Bereich *Prüfungsaufgabe* des FELIX-Kursmoduls der GIS Modulprüfung (siehe oben) eine Archivdatei (z.B. eine ZIP-Datei) mit folgendem Inhalt hoch
  1. alle Dateien, die zur Ausführung der Anwendung notwendig sind: Javascript/Typescript-Quellcode (client- und server-seitig), HTML- und CSS-Quellcode sowie ggf. Bild- und Audiodateien
  2. eine kurze(!) Anleitung, wie man die Anwendung ausführt z.B.:
  - Welche Datei muss als Node Server ausgeführt werden?
  - Welche html Datei im Browser geöffnet?
  - Muss ein *LiveServer* verwendet werden?
  3. einen (*GitHub Pages*) Link auf die möglichst lauffähige und vollständige Lösung
  4. eine einfache Beschreibung/Darstellung ihrer Datenbankstruktur in JSON-ähnlicher Syntax oder als Graphen (Baumstruktur)
  5. eine (unterschriebene) *Eidesstattliche Erklärung*, welche die eigenständige Lösungserarbeitung bestätigt (z.B. als PDF nach [dieser Vorlage](ee.pdf))

- Die Anleitung (2.), der Link (3.) und die Datenbankstruktur (4.) können gerne in ein Dokument zusammengefaßt werden (z.B. PDF, MarkDown, TXT), so dass es sich hier um 3 bis Dokumente handelt.

- Achten Sie auf eine sinnvolle Ordner-/Dateistruktur für ihren Quellcode sowie für das gesamte Archiv Ihrer Abgabe.

- Benennen Sie das Datenarchiv nach folgendem Schema: `<Nachname>_<Vorname>_<Matrikelnummer>.zip`

- Der Inhalt der Datenbaken ist nicht abzugeben.

- Letztmöglicher **Abgabetermin: Sonntag, 26. Juli 2020, 23:59.**.

### Prüfungsaufgaben zur Wahl

Zur Erinnerung: _Sie müssen nur **eine** dieser drei Aufgaben bearbeiten._

#### Aufgabe A: Eisdiele

Entwickeln Sie eine Online-Eisdiele, bei der es zwei Ansichten gibt:

- eine Ansicht für die Kunden, in der diese sich über verschiedene Auswahlmöglichkeiten (Eissorte, Menge, diverse Toppings, Becher oder Waffel, etc.) ihr Eis zusammenstellen können und davon laufend eine visuelle Darstellung angezeigt bekommen. Nachdem die Auswahl abgeschlossen ist und Lieferdaten (Name, Adresse) eingegeben wurden, soll die Bestellung in einer Datenbank abgelegt werden

- eine Ansicht für die Eisdielenbetreiber um die eingegangenen Bestellungen einzusehen, zu bearbeiten, und zu löschen (die Betreiber-Seite braucht nicht durch ein Passwort geschützt werden und kann frei zugänglich bleiben)

#### Aufgabe B: HFU Chat

Entwickeln sie einen Online-Chat mit persistenten Chatverläufen (d.h. Chatverläufe werden auch noch angezeigt, wenn man sich nach beliebiger Zeit erneut einloggt) und folgenden Eigenschaften:

- es gibt mindestens zwei verschiedene (globale) Chaträume, welche von der gleichen Seite aus auswähl- und nutzbar sind

- die Nutzer können sich mit Nutzername und Passwort registrieren und dann anmelden (*einloggen*) um an den Chats teilzunehmen (sorgen Sie sich hierbei nicht um die Datensicherheit)

- lediglich angemeldete Nutzer sollen in der Lage sein, Chatnachrichten zu sehen und zu schreiben

#### Aufgabe C: Neue Praktikumsseite

Entwickeln Sie eine neue GIS-Praktikumsseite mit folgenden Eigenschaften:

- die Studierenden können sich über ein Formular registrieren, über das sie folgene Informationen eingeben:
  - Vorname
  - Name
  - Matrikelnummer
  - URL eines Links auf einen selbstverwalteten Steckbrief (im Allgemeinen auf ein GitHub Repository) mit einem Profilbild

- die Steckbriefe aller registrierten Studierenden werden auf einer frei zugänglichen Seite zusammen mit folgenden Informationen in einer Liste angezeigt:
  - Feedback zu den Lösungen der Praktikumsaufgaben
  - fünfstufige Praktikumsbewertung ("Ampeln")
  - Sternchen (oder ähnliche Boni)

- eine über ein Passwort zugängliche Professoren-Ansicht erlaubt folgende Aktionen 
  - Einfügen von Feedback zu den Aufgabenlösungen
  - Setzen der aktuellen Praktikumsbewertung (fünfstufige "Ampeln")
  - Verteilung von Sternchen (oder anderen Boni)
  - Anpassung des registrierten Steckbrief-Links

Bauen Sie gerne weitere Features ein, die Sie für sinnvoll halten (z.B. Timestamps, Layout, Gruppen, etc.), sowohl für die Professoren als auch die Studierenden. Eine Validierung der Regsitrierung ist nicht notwendig. Orientieren Sie sich nicht allzu stark an der exitierenden Seite (höchstens um zu wissen, was man alles verbessern könnte :-) ).

### Empfehlungen und Tipps zur Lösung der Prüfungsaufgaben

Haben Sie keine Angst vor nicht komplett funktionierenden Abgaben. Sofern kleinere Teile nicht funktionieren aber Sie im mündlichen Teil erklären können was nicht funktioniert und warum, und was Sie versucht haben um das Problem zu lösen, können Sie immer noch eine sehr gute Note erreichen.

Es wird dringend empfohlen ...
- ... nicht einfach Ihren alten Code zu kopieren. Nehmen Sie was Sie bereits haben als Grundlage, aber nicht als Kopiervorlage. Einzelne Zeilen oder Konzepte können Sie ggf. übernehmen, aber bedenken Sie die aktuellen Anforderungen (und erinnern Sie sich an die Steine, die Sie sich während dem Praktikum selbst in den Weg gelegt haben und vermeiden Sie diese).

- ... nicht einfach drauf los zu Coden. Nehmen Sie sich die Zeit, machen Sie sich einen Plan und halten Sie diesen Plan in geeigneter Form fest (siehe unten). Vermutlich fallen Ihnen an diesem Punkt schon mögliche Schwierigkeiten (und Lösungen) ein, wodurch Sie dann nicht nachdem Sie schon die Hälfte gecodet haben nochmal alles wegschmeißen müssen. Dies hilft Ihnen auch selbst dabei, Ihre Gedanken zu sortieren und zu organisieren. Dazu können z.B. folgende Überlegungen gehören:
  - Wie sollte das Frontend aussehen und funktionieren? Welche Seiten brauche ich?
  - Wie sollen meine Datenstrukturen aussehen? Was für Interfaces brauche ich?
  - Welche Komponente (Client/Server/Datenbank) übernimmt welche Funktionalität?
  - Wie kann ich diese Funktionalität so implementieren, dass ich damit möglichst wenig Arbeit habe, sowohl beim Entwickeln als auch bei potentiellen (wahrscheinlichen!) Änderungen? 
  - Wie sollte die Datenbank strukturiert sein?  
  - Wie arbeitet was miteinander zusammen?

- ... Ihre Notizen mit abzugeben, damit ersichtlich wird, was Sie sich dabei gedacht haben. Besonders für den Fall dass irgendetwas nicht so ganz funktioniert wie geplant, ist das hilfreich für die Prüfer.

Die Vorgehensweise um eine Lösung der von Ihnen gewählten Aufgabe zu erarbeiten könnte z.B. folgende Schritte enthalten:
1. Nutzerseiten strukturieren und skizzieren (z.B. mit Stift und Papier)
2. Datenstrukturen planen, Interfaces anlegen
3. Beispieldaten anlegen (werden später aus DB geladen)
4. benötigte HTML-Seiten anlegen (zunächst statisch mit Beispieldaten gefüllt)
5. erste grundsätzliche CSS-Stilvorlage anlegen
6. Media Queries und responsive Design einfügen
7. TS-Code für den dynamischen Seitenaufbau implementieren (mit Beispieldaten)
8. TS-Code für Seiteninteraktion mit Event Listenern implementieren
9. Datenbank anlegen und strukturell aufbauen
10. NodeJS Server anlegen und mit DB verbinden
11. Schnittstellen/Kommunikationsbedarf zwischen Client und Server definieren
12. Server-Client Kommunikation implementieren

**Bei Problemen/Unklarheiten:** sollten Sie zum Praktikum kommen oder per Discord/Mail Fragen stellen.

### Typescript Dokumentation

[https://www.typescriptlang.org/](https://www.typescriptlang.org/)

---

## **?! _<small>Q&A</small>_** Fragen und Antworten

(die Publikation der Zusammenfassung erfolgt nach dem Q&A Termin)

Zusammenfassung von: [&lt;TawsTm&gt;](https://github.com/TawsTm)

### Reicht bei der fortlaufenden Darstellung eine Anzeige als Zahl?
Man muss nicht unbedingt grafisch jede einzelne Kugel anzeigen, sondern visuell alles abbilden. D.h. es sollte klar dargestellt werden, welche einzelnen Kugeln da sind.

### Darf ich SASS oder ähnliches verwenden?
Wer es versteht und es erklären kann, darf dies gerne verwenden

### Muss die Darstellung auch auf dem Handy/Tablet dargestellt werden?
Ja, da die Website responsive sein soll. Also das Bild muss nicht perfekt sein, aber man sollte alles erreichen können.

### Welches Datum sollen wir auf die Einwilligungserklärung schreiben?
Schreiben Sie bitte den 3-5.08.2020 auf ihre Einwilligung.

### Wie genau soll die Chat-Aktualisierung funktionieren?
Damit es immer direkt bei allen Nutzern aktualisiert wird, müsste man eine Socket Verbindung oder ähnliches aufbauen. Da wir das nicht behandelt haben, wäre es gut, wenn man nicht immer reloaden müsste, sondern nur die neuen Daten vielleicht alle 10 Sekunden erneuert werden (d.h. dem Server sagen, dass er einem alle neuen Nachrichten geben soll).

### Endabgabe Fehler ohne Eigenverschulden
Gehen sie davon aus, dass es funktioniert. Gehen sie z.B. nicht davon aus, dass Heroku abstürzt oder ähnliches. Wenn aufgrund so eines Fehlers etwas bei der Kontrolle nicht funktioniert, werden wir uns darum kümmern.

### Was ist mit REST-Schnittstellen gemeint?
Alles was dazu gehört, inklusive GET und POST.

### Mathe-Prüfung gleichzeitig mit GIS-Prüfung, was tun?
Ihr habt die Möglichkeit euch den Termin für die Prüfung selbst auszusuchen. Am Mittwoch den 08.07.2020 um 9:30 wird die Anmeldung freigeschaltet (wahrscheinlich ein Issue auf GitHub). Bitte schaut selbst, dass ihr keinen überschneidenden Termin wählt. Wenn dies trotzdem passiert, meldet euch bitte zeitnah!

### Aufgaben richtig lesen!
Auch die geforderten Abgabeanforderungen müssen eingehalten werden. Formvorgaben zählen auch zur Prüfungsleistung und können im Notfall bei nicht-Einhaltung zum nicht Bestehen der Prüfung führen.

### Darf man mySQL statt MongoDB nutzen?
Nein, die Vorgaben sind fest.

### Dürfte ich auch einen Jogurt Shop anstatt einer Eisdiele machen?
Solange ihr alle geforderten Features erfüllen könnt, ist das eigentlich kein Problem. Fragt uns einfach per Mail oder Discord ob das was ihr machen wollt auch funktioniert und akzeptiert wird.

### Erfährt man gleich im Anschluss an die mündliche Prüfung seine Note?
Ja.

### Müssen wir lizenzfreie Bilder/Videos benutzen?
Nein, die verwendeten Bilder liegen in eurer Verantwortung. Wir übernehmen aber keine Haftung.

### Dürfen wir einen Canvas o.ä. verwenden?
Wer kann und möchte, darf dies gerne tun.

### Wie wird die Effizienz von CSS bewertet?
Effizienz ist kein Kriterium. Ineffizienz ist euer Problem und kostet euch mehr Zeit, gibt aber keinen Abzug an Punkten. Nutzt die Kaskadierung von CSS.
