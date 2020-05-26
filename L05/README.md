## **27 _Mai_** Typescript und Javascript

*[direkt zur Praktikumsaufgabe](#a--praktikumsaufgabe)*
*[direkt zu Q&A](#-qa-fragen-und-antworten)*

### Einrichtung Typescript in VSCode
<video controls width="100%"> 
    <source src="https://scheuerle.net/lehre/gis/videos/05_Einrichtung_Typescript.mp4" type="video/mp4"> 
    <a href="https://scheuerle.net/lehre/gis/videos/05_Einrichtung_Typescript.mp4">Zum Video</a>
</video>

Denken Sie daran, immer wenn sie Ihren VSCode Editor öffnen, den BuildTask zu starten. Wenn Sie es automatisieren möchten, schauen sie eigenverantwortlich [hier](https://code.visualstudio.com/docs/editor/tasks) oder [hier](https://marketplace.visualstudio.com/search?term=Typescript%20Auto%20Compiler&target=VSCode&category=All%20categories&sortBy=Relevance).


`Strg + Shift + B` für die Build Tasks oder über `Terminal > Buildaufgabe ausführen`. Wählen sie "watch/Überwachen" um bis Sie VSCode schließen die js Dateien immer übersetzt zu bekommen oder "make/Erstellen" um einmal das gesamte Projekt zu übersetzen.

_Laden Sie die .js.map Dateien und selbstverständlich auch die .ts Dateien mit hoch._

**Links im Video**

- <a href="https://nodejs.org/">NodeJS</a>  
- [TSLint Erweiterung](https://marketplace.visualstudio.com/items?itemName=ms-vscode.vscode-typescript-tslint-plugin)
- [Konfigurations Dateien (tsconfig & tslint)](https://github.com/hs-furtwangen/GIS-SoSe-2020/tree/master/config_files)

**Terminal Befehle**
- `npm -v`
- `npm i -g typescript`
- `npm i -g tslint`
- `tsc --version`
  - falls es dabei in Powershell Probleme gibt, Powershell als Administrator ausführen, den folgenden Befehl ausführen und mit J/Y bestätigen.  
  `Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope LocalMachine`

### Vorwort JavaScript / Typescript
<video controls width="100%"> 
    <source src="https://scheuerle.net/lehre/gis/videos/05_JSTS_Vorwort.mp4" type="video/mp4"> 
    <a href="https://scheuerle.net/lehre/gis/videos/05_JSTS_Vorwort.mp4">Zum Video</a>
</video>

### JavaScript / Typescript Einführung
<video controls width="100%"> 
    <source src="https://scheuerle.net/lehre/gis/videos/05_JSTS_Einfuehrung.mp4" type="video/mp4"> 
    <a href="https://scheuerle.net/lehre/gis/videos/05_JSTS_Einfuehrung.mp4">Zum Video</a>
</video>

### Typescript Kontrollstrukturen
<video controls width="100%"> 
    <source src="https://scheuerle.net/lehre/gis/videos/05_TS_Kontrollstrukturen.mp4" type="video/mp4"> 
    <a href="https://scheuerle.net/lehre/gis/videos/05_TS_Kontrollstrukturen.mp4">Zum Video</a>
</video>

### DOM Manipulation
<video controls width="100%"> 
    <source src="https://lehre.gabriel-rausch.de/HFU/EIA1_SoSe20/L06/L06_05_DOM_Manipulation.mp4" type="video/mp4"> 
    <a href="https://lehre.gabriel-rausch.de/HFU/EIA1_SoSe20/L06/L06_05_DOM_Manipulation.mp4">Zum Video</a>
</video>

### Typescript Dokumentation

[https://www.typescriptlang.org/](https://www.typescriptlang.org/)

## **A _---_** Praktikumsaufgabe

Überarbeiten Sie Ihren Shop aus Aufgabe 4 dahingehend, dass Sie die Artikel auf der Seite über TypeScript generieren.
Es sollten keine Artikel mehr im HTML direkt stehen, sondern durch TypeScript, nachdem die Seite geladen wurde, generiert werden.
Entwickeln sie dafür eine passende Datenstruktur über `interface`s, so dass alle artikelrelevanten Informationen (s. A4) in einem Array abgelegt, abgefragt und verwendet werden können. Legen Sie dann alle benötigten Informationen in Ihrem Code ab und generieren Sie über geeignete Schleife(n) nachdem die Seite geladen ist die Artikel dynamisch hinzu.
Wenn Sie können, trennen sie die Daten und die Funktionalität in unterschiedliche TS Dateien (ein gemeinsamer `namespace` ist  hier empfohlen). Beachten Sie die [Coding Style Guidelines](https://hs-furtwangen.github.io/GIS-SoSe-2020/codingstyle/).

**Klarstellung**: Das interface sollte einen Artikel abbilden, und sämtliche relevanten Artikelinformationen zu einem Artikel sollte in diesem Interface sinnvoll abgelegt werden können. Die Sammlung aller Artikel soll dann in sinnvoller Weise abgebildet werden, z.B. in _einem_ Array in dem alle Artikel liegen. Bedenken Sie dabei die Skalierbarkeit und Anpassbarkeit (wie schwierig ist es, einen Artikel hinzuzufügen/entfernen/ändern?)! Bei einer kleinen Änderung sollten Sie nicht mehr Änderungen an ihrem Code vornehmen müssen als die reine Information zu verändern. 

### Recherchehinweise:
[Auf DOM Elemente über JS zugreifen](https://www.w3schools.com/js/js_htmldom_elements.asp)  
[das HTML von DOM Elementen verändern](https://developer.mozilla.org/en-US/docs/Web/API/Element/innerHTML)  
[Template Strings](https://www.typescriptlang.org/docs/handbook/release-notes/typescript-1-4.html#template-strings)  

### Freiwillige Übungsaufgaben
[Übungsaufgaben mit Fokus auf Konsolenausgaben zum Selbststudium](https://github.com/Plagiatus/EIA/blob/master/Aufgaben.md) mit Lösungen. (Diese Aufgaben wurden ursprünglich für das Ende von EIA1 konzipiert um sich auf EIA2 vorzubereiten, stellen aber allgemein eine gute Ressource zum Selbststudium dar, inklusive einfacher Aufgaben zur Wiederholung als auch sehr komplizierte Aufgaben. _Keine offizielle Aufgabe, lediglich als Bonusmaterial wenn Sie Zeit und Lust haben noch etwas mehr zu üben!_)

### **Abgabetermin: 31.05.2020 um 18:00!**

Bitte erstellen Sie nach Fertigstellung einen Link als oberstes Element (unter dem GitHub issues link) in Ihrer Steckbrief.htm, der auf das Ergebnis verweist (bspw. nutzername.github.io/GIS-SoSe-2020/Aufgabe_5).

---

## **?! _<small>Q&A</small>_** Fragen und Antworten

(die Publikation der Zusammenfassung erfolgt nach dem Q&A Termin)

Zusammenfassung von: [&lt;GitHub Nutzername&gt;](https://github.com/link-zu-github-profil)

### Erste Frage?
LoremLabore labore cillum mollit pariatur reprehenderit dolor laboris reprehenderit dolor sit officia ea non. Lorem reprehenderit exercitation labore eiusmod aute do nostrud officia aute proident sunt. Labore non tempor aliqua voluptate. Exercitation culpa officia ut aliqua nostrud laborum irure est. Minim eu sunt culpa adipisicing laborum consectetur aliqua quis.

### Zweite Frage?
Mollit aliquip veniam sit eiusmod tempor anim ipsum tempor. Aliqua sunt voluptate ea dolor. Nulla est mollit consectetur cupidatat ut cillum ipsum minim. Est ex et nulla laborum fugiat dolore. Aliquip laboris sint exercitation commodo dolor sint mollit qui sunt ipsum fugiat occaecat id enim.

## ...
