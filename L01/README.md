## **29 _Apr_** Grundlagen HTML

*[direkt zur Praktikumsaufgabe](#a--praktikumsaufgabe)*
*[direkt zu Q&A](#-qa-fragen-und-antworten)*

### HTML Basics
<video controls width="100%"> 
    <source src="https://scheuerle.net/lehre/gis/videos/01_GIS-EIA1-HTML-Basics.mp4" type="video/mp4"> 
    <a href="https://scheuerle.net/lehre/gis/videos/01_GIS-EIA1-HTML-Basics.mp4">Zum Video</a>
</video>

---

### HTML Syntax und erste Elemente
<video controls width="100%"> 
    <source src="https://scheuerle.net/lehre/gis/videos/01_GIS-EIA1-HTML-Syntax.mp4" type="video/mp4"> 
    <a href="https://scheuerle.net/lehre/gis/videos/01_GIS-EIA1-HTML-Syntax.mp4">Zum Video</a>
</video>

---

### HTML Bilder und Verweise

_Hier gibt es kein Video, stattdessen den ausführlichen Foliensatz zum selbst erarbeiten._
<embed src="https://scheuerle.net/lehre/gis/videos/01_GIS-EIA1-HTML-Bilder-Verweise.pdf" type="application/pdf" width="100%" height = "400px"/>

Den Foliensatz zu **HTML Bilder und Verweise** können Sie auch [hier](https://scheuerle.net/lehre/gis/videos/01_GIS-EIA1-HTML-Bilder-Verweise.pdf) als PDF herunterladen.

---

## **A _---_** Praktikumsaufgabe

Erstellen Sie eine stillose Webstite (HTML-dokument **KEIN CSS oder JS**) zu Ihrer Person die mindestens folgende Elemente enthält: 

- die HTML Basisstruktur mit den HTML Tags [doctype](https://www.w3schools.com/tags/tag_doctype.asp), [html](https://www.w3schools.com/html/html_basic.asp), [head](https://www.w3schools.com/html/html_head.asp), [body](https://www.w3schools.com/tags/tag_body.asp)
- eine Deklaration der [Zeichenkodierung](https://www.w3schools.com/charsets/ref_html_utf8.asp) und eines [Titels](https://www.w3schools.com/tags/tag_title.asp) - siehe [Überschrift](https://www.w3schools.com/tags/tag_hn.asp) (h tag)
- ein Bild von Ihnen - siehe [Image tag](https://www.w3schools.com/html/html_images.asp) 
- jeweils einen Textabsatz zu Ihrer Person und zu Ihrem Studium - siehe [Überschrift](https://www.w3schools.com/tags/tag_hn.asp) (h tag) & [Textblock](https://www.w3schools.com/tags/tag_p.asp) (p tag)
- Einen [Link](https://www.w3schools.com/tags/tag_a.asp) (a tag) auf eine andere Website ihrer Wahl
- Einen [Link](https://www.w3schools.com/tags/att_a_href.asp) (a tag) von einem [Textblock](https://www.w3schools.com/tags/tag_p.asp) (p tag) auf einen anderen ([Anker](https://de.wikipedia.org/wiki/Anker_(HTML)) → verwenden Sie dafür das name/id-Attribut in einem anderen HTML Element)
- mindestens 3 Links auf Websites Ihrer Kollegen

### Tipp

Entdecken Sie die Entwicklungswerkzeuge, die in Ihrem Browser eingebaut sind:
- [Chrome](https://developer.chrome.com/devtools)
- [Firefox](https://developer.mozilla.org/docs/Tools)
- [Safari](https://developer.apple.com/safari/tools/)
- [Opera](https://www.opera.com/dragonfly/)
- [Edge](https://docs.microsoft.com/en-us/microsoft-edge/devtools-guide)

Diese sind extrem hilfreich im Laufe des gesamten Semesters (und darüber hinaus), wir empfehlen Ihnen also dringend sich hier einzulesen.

### Ziel der Aufgabe

Sie haben die grundlegensten Elemente von HTML5 kennengelernt und verstanden und haben Ihre erste, simple & stillose Website erstellt in der Sie sich selbst vorstellen.

### Abgabetermin: 03.05.2020 um 18:00

---

## **?! _<small>Q&A</small>_** Fragen und Antworten

(die Publikation der Zusammenfassung erfolgt nach dem Q&A Termin)

Zusammenfassung von: [&lt;Logophoman&gt;](https://github.com/Logophoman)

### Was ist die Bildgöße für das Profilbild?

85x110 Pixel

### Die Größe ist halt zu klein für ein anständiges Bild. Kann ich das nicht ändern?

Nein, da das Bild auf der Kursseite in dieser Größe angezeigt wird.

### Mit welcher Software kriegt man das Bild auf 85x110?

Eine Liste von Bildbearbeitungssoftwares finden Sie in der nächsten Vorlesung

### In den Folien stand, dass SVG XML basiert ist, was genau bedeutet das?

SVG ist ein Bildformat das in dem Speicherformat XML formattiert ist. Die Struktur von SVG ist XML basiert. 

### Git Kraken braucht manchmal lange zum pushen. Woran liegt das?

An der hohen Auslastung von GitHub. Es muss eine Verbindung aufgebaut und die Daten übertragen werden.

### Auf der Steckbrief Seite sind Änderungen nicht sofort sichtbar. Woran liegt das? 

Da GitHub Pages einige Zeit zum Kompilieren braucht. Das kann zwischen 10 Sekunden und 5 Minuten dauern.

### Wie kann ich mein HTML dirket inspizieren?

Indem Sie es einfach mit einem Browser ihrer Wahl lokal öffnen. Mit Rechtsklick auf ein Element und "Element Untersuchen" kann man das HTML inspizieren. Bei Änderungen die Seite einfach mit F5 oder STRG F5 (löscht alte Files aus dem Cache) neu laden.

### Was ist Occlusion Culling?

Der Prozess wie Elemente "ausgemerzt" werden, die nicht sichtbar sind. Elemente die nicht auf dem Bildschirm angezeigt werden müssen, werden nicht geladen.

### Unteschied zwischen Visual Studio & Visual Studio Code?

Visual Studio ist eine sehr mächtige Entwickungsumgebung mit dem Hauptfokus auf Windows Entwicklung und sehr groß. Visual Studio Code ist eine Lightweight Version von Visual Studio die aber für die Entwicklung für Code aller Art verwendet werden kann. Es ist ein sehr mächtiger Text/Code Editor Für die Vorlesung reicht Visual Studio Code volkommen aus. 

### Wie formattiere ich meinen Code in Visual Studio Code? 

ALT + SHIFT + F -> dadurch wird Ihr Code schöner.

### Was ist auto completion?

Mit ctrl + space oder Tab kann man sich den aktuell eingebenen Befehl automatisch vervollständigen lassen, solange er richig geschrieben ist. Mit den Pfeiltasten kann man zwischen Vorschlägen navigieren und sich den besten aussuchen.

### Gitkraken erkennt in meinem repository eine datei ".DSStore", welche für mich nicht ersichtlich ist, wenn ich in den Ordner schaue. Was ist das?

DS.Store ist eine versteckte Datei, die immer in jedem MAC OS Ordner liegen. Da MAC OS auf Unix basiert, braucht aufgrund der Konvention jeder Ordner diese Datei. Sie ist für den Nutzer normalerweise nicht sichtbar. Sie können eine .gitignore Datei anlegen und die .dsstore Datei dort ignorieren lassen. Sie wird dann nicht auf GitHub abgelegt. 

### Was sind node_modules?

Die Abhängigkeiten von Node.js. Wir kommen bei der Lektion Serverentwicklung darauf zurück. Momentan sind sie noch nicht relevant.

### Was ist eine .gitignore Datei?

In dieser Datei stehen konkrete Dateien, Dateitypen oder Ordner nicht auf GitHub hochgeladen werden sollen. Sie werden von GIT ignoriert. 

### Ist Praktikumanwesenheit Pflicht?

Nein.

### Was ist alles Pflicht? 

Die wöchentlichen Abgaben & die Klausur am Ende des Semester. 