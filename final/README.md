## **Ω _---_** Prüfungsaufgabe

*[direkt zu Q&A](#-qa-fragen-und-antworten)*

Die Prüfungsaufgabe ist, gemeinsam mit der mündlichen Prüfung, die Prüfungsleistung für das Modul GIS. Die Prüfungsaufgabe und die mündliche Prüfung ersetzen zusammen die schriftliche Klausur, die dieses Semester nicht durchgeführt werden kann.

Ihnen stehen drei Aufgabenstellungen zur Wahl (siehe unten), die Sie selbstständig bearbeiten sollen. Die Lösung der Aufgabe ist im besten Fall eine lauffähige Anwendung, die der jeweiligen Beschreibung genügt und in Ihrem Steckbrief (auf der Praktikumsseite) veröffentlicht ist.

Die Bewertung der Aufgabenlösungen folgt einem einheitlichen [Kriterienkatalog](criteria). Sie werden in der mündlichen Prüfung aufgefordert die Details der Implementierung Ihrer Lösung zu erläutern.

### Letztmöglicher Abgabetermin ist Sonntag, 26. Juli 2020, 23:59.

Die mündliche Prüfung besteht aus einer detaillierten Auseinandersetzung mit Ihrer Lösung der gewählten Prüfungsaufgabe und allgemeinen Fragen zu den Lehrinhalten des Moduls. Nährere Informationen zum Ablauf und Zeitplan der mündlichen Prüfungen werden rechtzeitig veröffentlicht.

#### Allgemeine Hinweise

- **Jeder muss eine eigene Lösung erarbeiten.** Unter diesem Gesichtspunkt ist Gruppenarbeit nur sehr eingeschränkt bei allgemeineren Problemen möglich. So wie die Aufgaben gestellt sind, ist es äußerst unwahrscheinlich, dass es zwei oder mehr gleiche (oder verdächtig ähnliche) Lösungen gibt. Einander gleichende Lösungen werden nicht akzeptiert.

<!-- - Ihre Abgabe wird nur akzeptiert, wenn Sie die <a id="raw-url" href="https://github.com/hs-furtwangen/GIS-SoSe-2020/raw/master/final/Eidesstattliche_Erkl%C3%A4rung.pdf">Eidesstattliche Erklärung</a> unterschreiben und gemeinsam mit Ihrer Lösung abgeben. -->

- Implementieren Sie Ihre Lösung der gewählten Endaufgabe syntaktisch korrekt mit Hilfe von *HTML*, *CSS*, *Typescript*, *NodeJS* und *MongoDB*.

- Testen Sie die Applikation regelmäßig, ausgiebig und frühzeitig. Lassen Sie auch andere Personen testen um festzustellen, ob die Anwendung bedienbar und fehlertolerant ist. 

- Die Aufgaben lassen nicht zufällig einiges an Interpretationsspielraum. Toben Sie sich aus, machen Sie sich Gedanken, seien Sie kreativ, haben Sie Spaß.

- Die Prüfungsaufgabe ist **nicht** Teil des Praktikums und muss für das Bestehen des Praktikums nicht abgegeben werden.

#### Hinweise zur Abgabe
- Fügen Sie – wie für die Praktikumsaufgaben – in den Steckbrief einen Link auf die fertige und lauffähige Anwendung ein.
- Fügen Sie außerdem im Steckbrief einen Link auf eine Archivdatei (z.B. eine ZIP-Datei) mit folgendem Inhalt ein:
  1. alle Dateien, die zur Ausführung der Anwendung notwendig sind: Javascript/Typescript-Quellcode (client- und server-seitig), HTML- und CSS-Quellcode sowie ggf. Bild- und Audiodateien
  2. eine kurze(!) Anleitung, wie man die Anwendung ausführt (z.B. Welche Datei muss als Node Server ausgeführt werden? – Welche html Datei im Browser geöffnet? – Muss ein *LiveServer* verwendet werden?)
  3. eine einfache Beschreibung/Darstellung ihrer Datenbankstruktur in JSON-ähnlicher Syntax oder als Graphen (Baumstruktur)
  4. eine (unterschriebene) *Eidesstattliche Erklärung*, welche die eigenständige Lösungserarbeitung bestätigt (z.B. als PDF nach [dieser Vorlage](ee.pdf))

- Achten Sie auf eine sinnvolle Ordner-/Dateistruktur.

- Benennen Sie das Datenarchiv nach folgendem Schema: `<Nachname>_<Vorname>_<Matrikelnummer>.zip`

- Der Inhalt der Datenbaken ist nicht abzugeben.

## Aufgaben zur Wahl

Zur Erinnerung: _Sie müssen nur **EINE** dieser drei Aufgaben bearbeiten._

### Aufgabe A: Eisdiele

Entwickeln Sie eine Online-Eisdiele, bei der es zwei Ansichten gibt:

- eine Ansicht für die Kunden, in der diese sich über verschiedene Auswahlmöglichkeiten (Eissorte, Menge, diverse Toppings, Becher oder Waffel, etc.) ihr Eis zusammenstellen können und davon laufend eine visuelle Darstellung angezeigt bekommen. Nachdem die Auswahl abgeschlossen ist und Lieferdaten (Name, Adresse) eingegeben wurden, soll die Bestellung in einer Datenbank abgelegt werden

- eine Ansicht für die Eisdielenbetreiber um die eingegangenen Bestellungen einzusehen, zu bearbeiten, und zu löschen (die Betreiber-Seite braucht nicht durch ein Passwort geschützt werden und kann frei zugänglich bleiben)

### Aufgabe B: HFU Chat

Entwickeln sie einen Online-Chat mit persistenten Chatverläufen (d.h. Chatverläufe werden auch noch angezeigt, wenn man sich nach beliebiger Zeit erneut einloggt) und folgenden Eigenschaften:

- es gibt mindestens zwei verschiedene (globale) Chaträume, welche von der gleichen Seite aus auswähl- und nutzbar sind

- die Nutzer können sich mit Nutzername und Passwort registrieren und dann anmelden (*einloggen*) um an den Chats teilzunehmen (sorgen Sie sich hierbei nicht um die Datensicherheit)

- lediglich angemeldete Nutzer sollen in der Lage sein, Chatnachrichten zu sehen und zu schreiben

### Aufgabe C: Neue Praktikumsseite

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

#### Empfehlungen und Tipps

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
5. erste grundsätliche CSS-Stilvorlage anlegen
6. Media Queries und responsive Design einfügen
7. TS-Code für den dynamischen Seitenaufbau implementieren (mit Beispieldaten)
8. TS-Code für Seiteninteraktion mit Event Listenern implementieren
9. Datenbank anlegen und strukturell aufbauen
10. NodeJS Server anlegen und mit DB verbinden
11. Schnittstellen/Kommunikationsbedarf zwischen Client und Server definieren
12. Server-Client Kommunikation implementieren

**Bei Problemen/Unklarheiten:** sollten Sie zum Praktikum kommen oder per Discord/Mail Fragen stellen.

#### Typescript Dokumentation

[https://www.typescriptlang.org/](https://www.typescriptlang.org/)

---

## **?! _<small>Q&A</small>_** Fragen und Antworten

(die Publikation der Zusammenfassung erfolgt nach dem Q&A Termin)

Zusammenfassung von: [&lt;GitHub Nutzername&gt;](https://github.com/link-zu-github-profil)

### Erste Frage?
LoremLabore labore cillum mollit pariatur reprehenderit dolor laboris reprehenderit dolor sit officia ea non. Lorem reprehenderit exercitation labore eiusmod aute do nostrud officia aute proident sunt. Labore non tempor aliqua voluptate. Exercitation culpa officia ut aliqua nostrud laborum irure est. Minim eu sunt culpa adipisicing laborum consectetur aliqua quis.

### Zweite Frage?
Mollit aliquip veniam sit eiusmod tempor anim ipsum tempor. Aliqua sunt voluptate ea dolor. Nulla est mollit consectetur cupidatat ut cillum ipsum minim. Est ex et nulla laborum fugiat dolore. Aliquip laboris sint exercitation commodo dolor sint mollit qui sunt ipsum fugiat occaecat id enim.

## ...
