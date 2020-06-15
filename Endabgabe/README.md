# **E _---_** Endabgabe

*[direkt zu Q&A](#-qa-fragen-und-antworten)*

Entwickeln Sie **EINE** von diesen drei Anwendungen. Sie haben komplett freie Auswahl.

Ihre Aufgabe muss selbstverständlich online einsehbar, über den Steckbrief erreichbar und benutzbar sein.

## Deadline: Sonntag, 26.07.2020, 23:59

## Hinweise zur Abschlussarbeit

- In der Woche vom 27.6. bis zum 02.06. werden Ihre Arbeiten von den Dozenten korrigiert. In der Woche darauf (03.-07.08.) werden Sie ihre Arbeit mündlich "verteidigen", bzw eine mündlichen Prüfung absolvieren. In dieser mündlichen Prüfung geht es im Allgemeinen um die Lehrinhalte des Semesters und im Besonderen um ihre Endabgabe. Dort bekommen Sie dann auch direkt ihre Note für das Modul mitgeteilt. Nährere Infos zum Ablauf und Zeitplan der mündlichen Prüfungen werden später nachgereicht.

- Der Kriterienkatalog für die Bewertung kann [hier](Kriterienkatalog) eingesehen werden.

- Implementieren Sie Ihre Abschlussarbeit syntaktisch korrekt gemäß Ihrer technischen Analyse und nach den festgelegten Stil-Regeln mit Hilfe von Typescript, NodeJS, MongoDB, HTML, und CSS.
- Testen Sie die Applikation regelmäßig, ausgiebig und frühzeitig. Lassen Sie auch andere Personen testen um festzustellen, ob die Anwendung bedienbar und fehlertolerant ist. 
- Beachten Sie die [Coding Style Guidelines](https://hs-furtwangen.github.io/GIS-SoSe-2020/codingstyle/). Code der diesen Guidelines nicht entspricht führt zu Abzug! Code der W3 Errors oder JS-Errors aufweist führt ebenfalls zu Abzügen!
- **Abgabe**
  - Platzieren Sie wie üblich einen Link auf die fertige und lauffähige Anwendung im Steckbrief
  - Stellen Sie zudem auf diese Art auch ein gepacktes Archiv (z.B. .zip) zur Verfügung, welches die Projektordner inklusive aller erforderlichen Dateien, also TS, JS (sowohl server als auch client seitig), HTML, CSS, aber auch Bild- und Audiodaten, enthält. 
    - Datenbanken und deren Inhalte sind nicht abzugeben. Stattdessen ist eine einfache Beschreibung / Darstellung ihrer Datenbankstruktur beizufügen.
    - Es sollte auch eine kurze(!) Anleitung beigefügt sein, wie man die Anwedung zum laufen bringt (z.B. welche Datei muss als Node Server ausgeführt werden? welche html Datei im Browser geöffnet? Muss ein LiveServer verwendet werden?)
    - Achten Sie auf eine sinnvolle Ordner-/Dateistruktur.

- Die Aufgaben lassen nicht zufällig einiges an Interpretationsspielraum. Toben Sie sich aus, machen Sie sich Gedanken, werden Sie kreativ, haben Sie Spaß.
- **Bei der Endabgabe muss jeder seine komplett eigene Lösung erarbeiten.** Unter diesem Gesichtspunkt ist Gruppenarbeit nur sehr eingeschränkt bei allgemeineren Problemen möglich. Die Aufgaben sind eigentlich weit genug gestellt, dass es keine zwei gleichen (oder verdächtig ähnliche) Abgaben geben sollte.

### Typescript Dokumentation

https://www.typescriptlang.org/

### Weitere Hinweise

Haben Sie keine Angst vor nicht komplett funktionierenden Abgaben. Sofern kleinere Teile nicht funktionieren aber Sie im mündlichen Teil erklären können was nicht funktioniert und warum, und was Sie versucht haben um das Problem zu lösen, können Sie immernoch eine sehr gute Note erreichen.

Es wird dringend empfohlen...
- ...nicht einfach Ihren alten Code zu kopieren. Nehmen Sie was sie bereits haben als Grundlage, aber nicht als Kopierresource. Einzelne Zeilen oder Konzepte können Sie ggf. übernehmen, aber bedenken Sie die aktuellen Anforderungen (und erinnern Sie sich an die Steine die Sie sich während dem Praktikum selbst in den Weg gelegt haben und vermeiden Sie diese).
- ...nicht einfach drauf los zu Coden. Nehmen Sie sich die Zeit, und machen Sie sich zumindest ein bisschen einen Plan und halten Sie diesen Plan in geeigneter Form fest. Optimalerweise fallen Ihnen an diesem Punkt schon mögliche Schwierigkeiten (und Lösungen) ein, wodurch Sie dann nicht nachdem Sie schon die Hälfte gecodet haben nochmal alles wegschmeißen müssen. Dies hilft Ihnen auch selbst dabei, Ihre Gedanken zu sortieren und zu organisieren. Dazu gehören solche Überlegungen wie
  - Wie sollte das Frontend aussehen und funktionieren? Welche Seiten brauche ich?
  - Wie sollen meine Datenstrukturen aussehen? Was für Interfaces brauche ich?
  - Welcher Player (Client/Server/Datenbank) übernimmt welche Funktionalität?
  - Wie kann ich diese Funktionalität so implementieren, dass ich damit möglichst wenig Arbeit habe, sowohl beim Entwickeln als auch bei ~~potentiellen~~ _wahrscheinlichen_ Änderungen? 
  - Wie sollte die Datenbank strukturiert sein?  
  - Wie arbeitet was miteinander zusammen?
  - (Diese Überlegungen dürfen Sie gerne mit abgeben, damit wir sehen was Sie sich dabei gedacht haben. Besonders im Fall dass irgendetwas nicht so ganz funktioniert ist das hilfreich!)

Sollten Sie damit Probleme haben wie sie Anfangen können, hier ein paar Tips:

- Überlegen Sie sich, wie Ihre Anwendung umgesetzt werden könnte. Höchstwahrscheinlich werden Sie dies nicht sofort von Anfang bis Ende durchdenken und niederschreiben können.
- Meist empfiehlt es sich, zuerst einen groben Ablauf darzustellen, um Teilaspekte zu identifizieren. Erstellen Sie dann für die Teilprobleme wieder Darstellungen. So wandert ihr Fokus von „wie setzte ich die Anwendung um?“ zu „wie setze ich diesen Teil oder diesen Aspekt der Anwendung um?“. 
- Im Idealfall lassen sich Probleme auf diese Art so weit aufgliedern, bis sich für alle Unterprobleme einfache Lösungen finden, und damit das Gesamtproblem gelöst ist. In allen anderen Fällen hilft Ihnen diese Vorgehensweise zumindest, nicht über alles gleichzeitig nachdenken zu müssen und sich nicht schon am Anfang in Details zu verlieren.

>**Bei Problemen/Unklarheiten:** können Sie ins Praktikum kommen oder per Discord/Mail fragen stellen.

**Wir freuen uns auf spannende Abgaben von Ihnen!**

# Aufgaben

_Erinnerung: Sie müssen nur **EINE** dieser drei Aufgaben entwickeln._

## Kursseite

Entwickeln Sie eine neue Kursseite für GiS. Diese sollte es den Studierenden erlauben, sich über einen Link zu registrieren, welcher daraufhin auf der Kursseite auf einen (selbstverwalteten) Steckbrief zusammen mit einem Profilbild verweist, welche angezeigt werden (Email oder sonstige Validierung ist nicht notwendig). Außerdem müssen von einer Professor-Ansicht (welche z.B. durch ein Passwort oder eine seperate Seite umgesetzt werden kann) aus...
- ... Feedback gegeben werden können.
- ... Ampeln gegeben und wieder entfernt werden können.
- ... Gruppen gewechselt werden können.
- ... Sternchen (oder andere Boni) verteilt werden können.
- ... Der registrierte Link angepasst werden können

Ermöglichen Sie den Seitenbesuchern, nach Gruppe zu sortieren.

Bauen Sie außerdem gerne weitere Features ein, die Sie für sinnvoll halten (z.B. Timestamps, anderes Layout, etc etc), sowohl für die Professoren als auch die Studierenden. Orientieren Sie sich nicht allzu stark an der exitierenden Seite, sondern höchstens um zu wissen, was man alles verbessern könnte 😉

## Eisdiele(r)

Entwickeln Sie eine Online-Eisdiele, bei der es zwei Ansichten gibt:
- Eine für die Kunden, in der diese über verschiedene Auswahlmöglichkeiten (Eissorte, Menge, div. Toppings, Becher oder Waffel, etc.) sich das Eis ihrer Träume zusammenstellen können und direkt live eine visuelle Darstellung davon angezeigt bekommen. Nachdem Lieferdaten (Name, Adresse) eingegeben wurden, soll die Bestellung in einer Datenbank abgelegt werden.
- Eine für den Eisdielenbetreiber um die eingegangenen Bestellungen zu verwalten (einsehen, bearbeiten, löschen, etc). Machen Sie sich keine Sorgen um das "schützen" der Besitzer-Seite sondern machen Sie diese einfach frei zugänglich.

## HFUChat

Entwickeln sie einen Online-Chatraum mit persistenten Chatverläufen. Das heißt, dass vorherige Nachrichten auch noch vorhanden sind, wenn man sich nach einigen Tagen erneut einloggt. Erlauben Sie mindestens zwei verschiedene (globale) Chaträume, welche von der gleichen Seite aus auswähl- und nutzbar sind. Erlauben Sie Nutzern, sich mit Nutzername und Passwort zu registrieren und dann anzumelden. Machen Sie sich keine Sorgen über Datensicherheit, sondern teilen Sie Ihren Nutzern einfach freundlich mit, [dass es dafür kein Budget mehr gab](https://pics.me.me/pick-a-password-dont-reuse-your-bank-password-we-didnt-45247832.png).
Lediglich eingeloggt Nutzer sollen in der Lage sein, Chatnachrichten zu sehen und zu schreiben.


---

## **?! _<small>Q&A</small>_** Fragen und Antworten

(die Publikation der Zusammenfassung erfolgt nach dem Q&A Termin)

Zusammenfassung von: [&lt;GitHub Nutzername&gt;](https://github.com/link-zu-github-profil)

### Erste Frage?
LoremLabore labore cillum mollit pariatur reprehenderit dolor laboris reprehenderit dolor sit officia ea non. Lorem reprehenderit exercitation labore eiusmod aute do nostrud officia aute proident sunt. Labore non tempor aliqua voluptate. Exercitation culpa officia ut aliqua nostrud laborum irure est. Minim eu sunt culpa adipisicing laborum consectetur aliqua quis.

### Zweite Frage?
Mollit aliquip veniam sit eiusmod tempor anim ipsum tempor. Aliqua sunt voluptate ea dolor. Nulla est mollit consectetur cupidatat ut cillum ipsum minim. Est ex et nulla laborum fugiat dolore. Aliquip laboris sint exercitation commodo dolor sint mollit qui sunt ipsum fugiat occaecat id enim.

## ...
