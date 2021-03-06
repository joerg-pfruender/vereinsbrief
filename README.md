# Vereinsbrief

Electron Applikation zur Erstellung eines Geschäftsbriefs für einen Verein

Basiert auf [JAVA TM](https://www.java.com/de/), [LaTeX](https://www.latex-project.org/) und [Electron](https://github.com/atom/electron)


## Zur Installation

Vor der Installation von "Vereinsbrief" ist die Installation von Java 8 und LaTeX nötig:

* [JAVA TM SE](http://www.oracle.com/technetwork/java/javase/downloads/jre8-downloads-2133155.html)
* [LaTeX](https://www.latex-project.org/get/)

* [TeX Live](https://www.tug.org/texlive/acquire-netinstall.html) Unter Windows getestet mit TeX Live, Achtung: Installation dauert sehr lange
* Ubuntu-Linux: `sudo apt-get install texlive-latex-base texlive-latex-extra texlive-latex-recommended xzdec`

Bei Bedarf müssen evtl. noch TeX-Pakete nachinstalliert werden:


`tlmgr init-usertree`
 
`tlmgr update --all`

`tlmgr install adjustbox`

## Zur Benutzung

Wenn mal was nicht so aussieht, wie Du dachtest, schau mal bei LaTeX nach, wie man's formatieren soll:
[https://wch.github.io/latexsheet/latexsheet.pdf](https://wch.github.io/latexsheet/latexsheet.pdf)

Wichtige Sonderzeichen, die man escapen muss:

* \ -> \\
* $ -> \$
* % -> \%
* & -> \&
* & -> \&

Ich habe überlegt, diese immer zu ersetzen, aber dann bekommen die LaTeX-Profis wieder Probleme. Daher nicht.


## Einfache Anpassungen

Dieses Programm soll "hackbar" sein.

### Die Datei `vereinsbrief.tex.ftl` kann an eigene Bedürfnisse angepasst werden.

Platzhalter haben die Form `${mein_platzhalter}`.
Wenn ein größeres Textfeld im Formular erscheinen soll, dann `${mein_platzhalterLang}`.

### Die Datei `logo.eps` kann durch ein eigenes Logo für den Briefkopf rechts oben ersetzt werden.

Wenn die Größe des Logos beibehalten wird, dann müssen auch keine Anpassungen in `vereinsbrief.tex.ftl` gemacht werden.   


## Zur Weiterentwicklung

Basiert auf [Electron](https://github.com/atom/electron).

Es müssen vorhanden sein:
* [Node.js](https://nodejs.org/en/download/current/)
* [npm](https://www.npmjs.com/get-npm)
* [JAVA TM SE JDK 8](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)
* [Maven](https://maven.apache.org/)


Wichtige Befehle:
* `mvn package` Java bauen
* `make`
* `npm install` Electron-App bauen
* `npm start`   Electron-App starten
* `electron-packager ./ Vereinsbrief --all` Electron apps erstellen
* `tar -zcvf Vereinsbrief-linux-x64.tar.gz Vereinsbrief-linux-x64` tar.gz für Linux64 packen

Vielen Dank an:

* an [Olle Törnström](https://github.com/olle) für die Vorlage von [https://github.com/olle/electron-starter](https://github.com/olle/electron-starter)
* an Michael Lenzen für das LaTeX-Template
* an [Benni und Jonas](http://be-jo.net/) für die gute g-brief-Vorlage
* an die Macher von electron, LaTeX, Spring-Boot, Freemarker, Apache-Maven und alle anderen, auf denen das Projekt basiert.
* an Gott, der uns alle geschaffen hat.
  