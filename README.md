# LaTeX-Vorlage

Vorlage für (deutschsprachige) wissenschaftliche Arbeiten (Hausarbeit, Projektarbeit, Bachelor/Master Thesis).

## Vorraussetzungen

TeXworks und TexLive

Das deutsche Sprachpaket kann unter http://archive.services.openoffice.org/pub/mirror/OpenOffice.org/contrib/dictionaries/ heruntergeladen und im Ordner C:\Users\USER\TeXworks\dictionaries hinterlegt werden.

## Dateien

- packages.tex: Verwendete Pakete
- vars.tex: Variablen
- Meta.tex: PDF Meta Angageb
- Cover.tex: Deckblatt
- Declaration.tex: Eidesstattliche Erklärung
- Intro.tex: Einführung
- List.tex: Verzeichnisse
- Acronym.tex: Abkürzungen
- Docu.tex: Hautpdokument
- Bibliography.tex: Literaturverweise
- Appendix.tex: Anhang
- Beamer.tex: Präsentation

## Elemente

### Text- und Seitenformatierung

Anführungszeichen
```tex
\glqq Text\grqq \ 
```

Kursiv schreiben
```tex
\textit{Text}
```

Fett schreiben
```tex
\textbf{Text}
```

Tiefstellen
```tex
$00110001_{bin}$
```

Neue Seite erzwingen
```tex
\clearpage
```

Absatz
```tex
\\
```

### Labels

Labels (Verweise) werden folgendermaßen definiert

```tex
\label{lbl:name}
```

Eine dokumenteninterne Verlinkung wird folgendermaßen erreicht:
```tex
\ref{lbl:name}
```

Zur besseren Unterscheidung der Labels kann auf folgende Einteilung zurückgegriffen werden

- sec: Oberpunkt
- subsec: Unterpunkt
- subsubsec: Unter Unterpunkt
- subsubsubsec: Unter-Unter Unterpunkt
- pic: Bild
- tbl: Tabelle
- lst: Quelltext einbinden (Listing)

### Abschnitte

Sections können zur Gliederung des Dokuments verwendet werden:

```tex
\section{Oberpunkt}
\label{sec:...}

  \subsection{Unterpunkt}
  \label{subsec:...}

    \subsubsection{Unter-Unterpunkt}
    \label{subsubsec:...}

      \subsubsection*{Unter-Unter Unterpunkt}
      \label{subsubsubsec:...}
```

### Aufzählung

```tex
\begin{itemize}
  \item item
\end{itemize}
```

### Einbinden

#### Bilder

```tex
\begin{figure}[h]
\centering
\includegraphics[scale=0.07]{img/picture}
\caption{...}
\label{pic:picture}
\end{figure}
```

### Listings

Über Listings können Quelltexte eingebunden werden:
```tex
\lstinputlisting[language=sh,label=lst:name,caption=...]{src/name.sh}
```

#### Fußnoten

```tex
\footnote{...}
```

### Abkürzungen

Abkürzungen können in der Datei Acronym.tex definiert werden:
```tex
\acro{GUI}{Graphical User Interface}
```

Um sie in der Dokumentation zu verwenden stehen folgende Befehle zur Verfügung:
```tex
\acs{GUI} -> GUI
\ac{GUI} -> GUI (Graphical User Interface)
\acl{GUI} -> Graphical User Interface
```

### Literaturverweis

Literaturverweise werden in der Datei Bibliography.tex angelegt. Beispiel:
```tex
\bibitem{wiki_boost} Boost (C++-Bibliothek) - Wikipedia, de.wikipedia.org (Stand 10.10.2013)
 \url {http://de.wikipedia.org/wiki/Boost_(C++-Bibliothek)}
```

Der Literaturverweis lässt sich dann im Dokument folgendermaßen referenzieren:
```tex
\cite{wiki_boost}
```

Auch hier empfiehlt sich die Unterteilung der Identifier um direkt erkennen zu können um welchen Quellentyp es sich handelt (hier im Beispiel z.B. Wikipedia)

### Minipages

Minipages können genutzt werden um die Seite in verschiedene Bereiche aufzuteilen, was hilfreich ist wenn man etwas nebeneinander darstellen möchte:

```tex
\begin{minipage}{0.25\textwidth}

\end{minipage}
\begin{minipage}{0.2\textwidth}
  \
\end{minipage}
\begin{minipage}{0.25\textwidth}

\end{minipage}
```

### Folie

```tex
\begin{frame}{Titel}

\end{frame}
```

Pause einfügen:

```tex
\pause
```

# Hinweise zur Verwendung der Vorlage

Diese Vorlage basiert auf anderen Vorlagen, die aus dem Internet zusammen getragen wurden. Es gilt daher folgender Grundsatz (siehe LICENSE):

Hiermit wird unentgeltlich jeder Person, die eine Kopie der Software und der zugehörigen Dokumentationen (die "Software") erhält, die Erlaubnis erteilt, sie uneingeschränkt zu benutzen, inklusive und ohne Ausnahme dem Recht, sie zu verwenden, kopieren, ändern, fusionieren, verlegen, verbreiten, unterlizenzieren und/oder zu verkaufen, und Personen, die diese Software erhalten, diese Rechte zu geben, unter den folgenden Bedingungen:

Der obige Urheberrechtsvermerk und dieser Erlaubnisvermerk sind in allen Kopien oder Teilkopien der Software beizulegen.

DIE SOFTWARE WIRD OHNE JEDE AUSDRÜCKLICHE ODER IMPLIZIERTE GARANTIE BEREITGESTELLT, EINSCHLIESSLICH DER GARANTIE ZUR BENUTZUNG FÜR DEN VORGESEHENEN ODER EINEM BESTIMMTEN ZWECK SOWIE JEGLICHER RECHTSVERLETZUNG, JEDOCH NICHT DARAUF BESCHRÄNKT. IN KEINEM FALL SIND DIE AUTOREN ODER COPYRIGHTINHABER FÜR JEGLICHEN SCHADEN ODER SONSTIGE ANSPRÜCHE HAFTBAR ZU MACHEN, OB INFOLGE DER ERFÜLLUNG EINES VERTRAGES, EINES DELIKTES ODER ANDERS IM ZUSAMMENHANG MIT DER SOFTWARE ODER SONSTIGER VERWENDUNG DER SOFTWARE ENTSTANDEN.