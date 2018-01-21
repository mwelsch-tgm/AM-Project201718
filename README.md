# 3AHIT-AM
AM Klassenaufgabe Markdown Guide:

##1. Ordner Aufbau
###1.1 Dateiort
Mit euren Dokumenten bekommt ihr auch einen Github Link zu einem Preset wie der Projektordner aussehen wird. Deine Datei soll in einen Unterordner mit Namenskürzel abgespeichert werden.
Beispiel: 
/hauptfile.tex
/mkisser/diff1_001_mkisser.tex
Ich habe hier jetzt Linux notation verwendet.

###1.2 Dateinamen
Benennt die Dateien (der Latex Files) nach folgendem Schema <Dokumentname>_<Namenskürzel>.tex
Beispiel: 
diff1_001_mkisser.tex
Das erleichtert das Sortieren der Daten.

###1.3 Bilder
Bilder sollen sich in eurem Unterverzeichnis in einem eigenen Ordner befinden.
Beispiel:
/mkisser/img/image.png


##2. Dokument Aufbau
###2.1 Grundaufbau
Die .tex Datei soll wie folgt beginnen:
\documentclass[../mainfile.tex]{subfiles}
Das bedeutet, dass eure Datei eine Unterdatei des Projektes ist.
Da am Ende nur das mainfile.tex kompiliert wird müssen sich alle Pfade relativ von dieser Datei aus beziehen.
Für Bilder bedeutet das, dass sie wie folgt eingebunden werden müssten:
Beispiel:
\includegraphics[scale=0.5]{./mkisser/image.png}
ACHTUNG
Ihr könnt das Dokument so noch nicht selbst kompilieren, wenn ihr testen wollt ob alles passt, muss sich der Pfad auf eure Unterdatei beziehen.
Beispiel:
\includegraphics[scale=0.5]{./image.png}

###2.2 Dokument Format
Das Projekt wird mit der Article Class kompiliert, deswegen achtet auf die Kompatiblität der Files.

###2.3 Packages
Bei jedem Package per Kommentar hinzufügen warum es benötigt wird und wieso genau diese Parameter verwendet werden, das kann sonst zu massiven Kompatiblitätsproblemen führen und teile des Dokuments müssten neu gemacht werden.

###2.4 Überschriften
Kapitelüberschriften: \section
Definitionen von Kapitel: \subsection
Unterkapitel: \subsection
Definition von Unterkapitel: \subsubsection
Beispiele: Allgemein immer mit der selben "Stufe" der letzten Überschrift aber als '*' Version anführen: \subsection*

###2.5 Graphen
Diese können entweder als Bild eingefügt werden, oder mit LaTeX selbst gemacht werden.
Bei letzterem solltet ihr den Graphen als standalone extra erstellen und wie folgt einbinden:
\includestandalone[]{./mkisser/graph}

#Abgabe Checklist:
- Ist die Datei richtig benannt?
- Ist die Documentclass richtig gesetzt?
- Sind alle relativen Pfade richtig gesetzt?
- Sind alle Packages richtig Dokumentiert?
