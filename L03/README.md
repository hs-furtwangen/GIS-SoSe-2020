## **13 _Mai_** Einstieg CSS

*[direkt zur Praktikumsaufgabe](#a--praktikumsaufgabe)*
*[direkt zu Q&A](#-qa-fragen-und-antworten)*

### Einführung
<video controls width="100%"> 
    <source src="https://lehre.gabriel-rausch.de/HFU/EIA1_SoSe20/L03/01_Einstieg_in_CSS.mp4" type="video/mp4"> 
    <a href="https://lehre.gabriel-rausch.de/HFU/EIA1_SoSe20/L03/01_Einstieg_in_CSS.mp4">Zum Video</a>
</video>

CSS (steht für Cascading Style Sheets) ist eine browser-basierte Gestaltungssprache, mit der Webanwendungen visuell angepasst werden können. CSS-Anweisungen können auf drei Arten eingebunden werden: 
* **Inline**: nicht zu empfehlen, da Redundanzen in der Regeldefinition mehrerer Elemente entsteht und ab einer gewissen Deklarationsmenge die Eigenschafts-Werte-Paare nicht mehr pflegbar sein. Zudem ist eine klare Trennung zwischen Inhalt und Gestlatung nicht mehr möglich.
* **Style-Tag im Head**: schafft eine Trennung zwischen Inhalt und Gestaltung, verursacht aber auch eine Redundanz über mehrere HTML-Seiten. 
* **externes CSS-Stylesheet**: im Head des HTML-Dokuments verlinkt ist. Schafft eine klare Trennung zwischen Inhalt und Gestaltung, kann in beliebig vielen HTML-Seiten genutzt und an einer zentralen Stelle administiert werden.

Eine CSS-Anweisung besteht immer aus einem Selektor und der Deklaration, die aus Eigenschaft und Wert besteht.

**Links im Video**

Übersicht von sämtlichen aktuellen CSS-Anweisungen mit Beispielen:

<a href="https://www.w3schools.com/css/">https://www.w3schools.com/css/</a>

### Eigenschaften
<video controls width="100%"> 
    <source src="https://lehre.gabriel-rausch.de/HFU/EIA1_SoSe20/L03/02_CSS_Eigenschaften.mp4" type="video/mp4"> 
    <a href="https://lehre.gabriel-rausch.de/HFU/EIA1_SoSe20/L03/02_CSS_Eigenschaften.mp4">Zum Video</a>
</video>

Die aktuellen Möglichkeiten der visuellen Gestaltung mit CSS sind scheinbar endlos. In diesem Video werden die gängigsten Eigenschaften sowie ein effizienter Workflow mit Visual Studio Code vorgestellt und die Funktionen der verschiedenen CSS-Anweisungen erklärt.

Eigenschaften stehen immer in Abhängigkeit zu dem entsprechenden Element, sodass nicht alle Eigenschaften bei allen Elementen sinnvoll sind oder schlicht keine Auswirkung haben.


### Selektoren
<video controls width="100%"> 
    <source src="https://lehre.gabriel-rausch.de/HFU/EIA1_SoSe20/L03/03_CSS_Selektoren.mp4" type="video/mp4"> 
    <a href="https://lehre.gabriel-rausch.de/HFU/EIA1_SoSe20/L03/03_CSS_Selektoren.mp4">Zum Video</a>
</video>

Um CSS-Anweisungen an bestimmte Elemente eines HTML-Dokument zu adressieren, kann man mithilfe von Selektoren auf ein oder mehrere Elemente zugreifen.

Es gibt verschiedene Arten von Selektoren: die drei Haupt-Selektoren sind **Element-Selektoren** (gebildet aus dem Tag-Namen), **ID-Selektoren** (wirken sich auf Elemente aus, die mit einer eindeutigen ID versehen wurden) und **Klassen-Selektoren** (ermöglichen die Auswahl mehrerer HTML-Elemente, auf die mit der Formatierung zugegriffen werden soll).

### Kaskadierung und Vererbung
<video controls width="100%"> 
    <source src="https://lehre.gabriel-rausch.de/HFU/EIA1_SoSe20/L03/04_Kaskadierung_und_Vererbung.mp4" type="video/mp4"> 
    <a href="https://lehre.gabriel-rausch.de/HFU/EIA1_SoSe20/L03/04_Kaskadierung_und_Vererbung.mp4">Zum Video</a>
</video>

Das Grundprinzip der Kaskadierung bewirkt eine Reihen- oder Rangfolge, in der Eigenschaften in CSS vererbt werden, denn die einzelnen CSS-Selektoren werden unterschiedlich schwer gewichtet. Es ist hilfreich, diese Regeln zu kennen, um zu verstehen, wann welche Anweisungen umgesetzt werden (bzw. warum nicht) und welche Anweisungen andere überschreiben.

Definierte Eigenschaften werden an die (semantisch untergeordneten) Kinderelemente des selektierten Elements vererbt. Werden jedoch die Eigenschaften für die untergeordneten Elemente neu definiert, überschreiben diese die vererbten Eigenschaften.

### Box Model und Masseinheiten
<video controls width="100%"> 
    <source src="https://lehre.gabriel-rausch.de/HFU/EIA1_SoSe20/L03/05_CSS_Box_Model_und_Masseinheiten.mp4" type="video/mp4"> 
    <a href="https://lehre.gabriel-rausch.de/HFU/EIA1_SoSe20/L03/05_CSS_Box_Model_und_Masseinheiten.mp4">Zum Video</a>
</video>

Das CSS-Box-Model beschreibt, dass alle Elemente im Browser auf Basis einer Box beschrieben werden können, die aus einer bestimmten Größe (Höhe x Breite), einem Innenabstand (**padding**), einem Rahmen (**border**) und einem Außenabstand (**margin**) bestehen.

Der Browser arbeitet mit verschiedenen Maßeinheiten, für den Anfang genügt das Pixelmaß (**px**). Ansonsten gibt es beispielsweise noch Angaben in **pt** (statisch, Anwendung im Druck), **em** und **rem** (relative Angabe) oder **Prozent**.

### Take Aways
<video controls width="100%"> 
    <source src="https://lehre.gabriel-rausch.de/HFU/EIA1_SoSe20/L03/06_Take_Aways.mp4" type="video/mp4"> 
    <a href="https://lehre.gabriel-rausch.de/HFU/EIA1_SoSe20/L03/06_Take_Aways.mp4">Zum Video</a>
</video>

* CSS definiert die Darstellung von Inhalten im Browser und kann auf drei Wegen eingebunden werden: Inline, im Head oder als externes Stylesheet.
* CSS-Anweisungen bestehen aus Selektor(-pfad/-kette) und Deklaration und es gibt viele verschiedene CSS-Eigenschaften zur Manipulation der Darstellung im Browser.
* Es gibt drei Haupt-Selektoren, welche eine Art Rangfolge besitzen.
* Eigenschaften werden von Eltern- an Kinderelemente vererbt, können aber auch überschrieben werden.
* Das CSS-Box-Model beschreibt verschiedene Abstandsmaße für Elemente.

---

## **A _---_** Praktikumsaufgabe

Die Portfolio-Website aus der letzten Aufgabe wird nun mit CSS ergänzt, um verschiedene Gestaltungsaspekte zu realisieren.

Für dieses Projekt erstellen Sie einen Unterordner (bspw. /Aufgabe3) in Ihrem bestehenden GiS-Git-Repository und erstellen dort eine Kopie Ihres aktuellen (ggf verbesserten) Portfolios aus der vorherigen Aufgabe, an dem Sie nun weiterarbeiten werden.

Gestalten Sie ihre Webseite nach freien Stücken, **beachten Sie dabei aber die [Kundenanmerkungen](https://gabriel-rausch.github.io/EIA1-SoSe20/L03/task_material/Anmerkungen.pdf)!** Versuchen Sie dabei, ihr Design möglichst ansprechend zu gestalten. Als _mögliche_ Vorlage können Sie [diese Designs](https://github.com/gabriel-rausch/EIA1-SoSe20/tree/master/L03/task_material/screenshots) hinzuziehen (dies ist nur ein Vorschlag, Sie können auch ein eigenes Design entwickeln. Es muss aber mindestens den Kundenanmerkungen genügen).  
Scheuen Sie sich nicht vor strukturellen Änderungen ihres HTML Codes, um das Design besser umsetzen zu können. HTML und CSS müssen eng zusammenarbeiten um das gewünschte Ergebnis einfach und effizient zu erreichen.  

Das Grafikelement für den geforderten Hintergrund finden sie [hier](https://gabriel-rausch.github.io/EIA1-SoSe20/L03/task_material/images/bg.png).

Verwenden Sie zur Umsetzung des CSS ein **extern eingebundenes Stylesheet** (kein inline oder style tag). Verwenden Sie außerdem jeden der drei Haupt-Selektoren mindestens zweimal. Des weiteren sollte das Box-Modell mindestens einmal angewandt werden.  
Es bietet sich wahrscheinlich an, für alle drei Seiten die selbe Stylesheetdatei zu verwenden, dies ist aber kein muss (denn wie immer beim Programmieren gilt: Wer Code kopiert, macht irgendwas falsch).

Achten Sie auch hier weiterhin auf die Konformität mit den Regeln des W3C und nutzen Sie ggf. den Validator.

### **Abgabetermin: 17.05.2020 um 18:00!**

Bitte erstellen Sie nach Fertigstellung einen Link als oberstes Element (unter dem GitHub issues link) in Ihrer Steckbrief.htm, der auf das Ergebnis verweist (bspw. nutzername.github.io/GIS-SoSe-2020/Aufgabe_3).

---

## **?! _<small>Q&A</small>_** Fragen und Antworten

(die Publikation der Zusammenfassung erfolgt nach dem Q&A Termin)

Zusammenfassung von: [&lt;GitHub Nutzername&gt;](https://github.com/link-zu-github-profil)

### Erste Frage?
LoremLabore labore cillum mollit pariatur reprehenderit dolor laboris reprehenderit dolor sit officia ea non. Lorem reprehenderit exercitation labore eiusmod aute do nostrud officia aute proident sunt. Labore non tempor aliqua voluptate. Exercitation culpa officia ut aliqua nostrud laborum irure est. Minim eu sunt culpa adipisicing laborum consectetur aliqua quis.

### Zweite Frage?
Mollit aliquip veniam sit eiusmod tempor anim ipsum tempor. Aliqua sunt voluptate ea dolor. Nulla est mollit consectetur cupidatat ut cillum ipsum minim. Est ex et nulla laborum fugiat dolore. Aliquip laboris sint exercitation commodo dolor sint mollit qui sunt ipsum fugiat occaecat id enim.

## ...
