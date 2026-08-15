# LateX Handige Beamer Code
Werkt binnen een nieuwe project op 
[https://www.overleaf.com/](https://www.overleaf.com/) (eigen afbeelding paden gebruiken)

```latex
\documentclass{beamer}

% https://www.overleaf.com/learn/latex/Beamer#Reference_guide
\usetheme{Copenhagen} % this style has a section navigation bar
\usecolortheme{seahorse}

% \setbeamertemplate{navigationsymbols}{} % don't show navigation symbols
% \setbeamertemplate{headline}{} % remove copenhagen section navbar
\setbeamercovered{transparent} % make invisible elements transparent
%\setbeamersize{text margin left=30mm,text margin right=30mm} 


\usepackage{graphicx} % Required for inserting images
\usepackage{lipsum}   % filler text
\usepackage{xcolor}   % change text color

\title{Beamer}
\author{Peter Cypers}
\date{\today}

\begin{document}

{
\usebackgroundtemplate{\includegraphics[width=\paperwidth,height=\paperheight]{img/RM-presentatation-intro.jpg}}
\maketitle
}
\section{Introduction}

\begin{frame}{Overview}
    \tableofcontents
\end{frame}

{
\usebackgroundtemplate{\includegraphics[width=\paperwidth,height=\paperheight]{img/RM-presentatation-intro.jpg}}
\begin{frame}
    \frametitle{My Slide}
    Some text
    
    \textcolor{red}{Some red text}
    
\end{frame}
}

{
\usebackgroundtemplate{\includegraphics[width=\paperwidth,height=\paperheight]{img/RM-bg-02.jpg}}
\begin{frame}
    \frametitle{Oplijsting voorstellen}

    {\color{white}
    \begin{itemize}
    
        \item[] \textcolor{white}{\textbf{Specialisatiedomein:} Ontwikkeling van een modulaire en contextbewuste Linux-desktopomgeving voor gebruikers die regelmatig wisselen tussen verschillende computer-activiteiten} 
        \item[] \textcolor{white}{\textbf{Interprofessioneel:} Ontwerp en evaluatie van een digitale ecologische voetafdruk-tracker ter ondersteuning van duurzaam dagelijks gedrag bij studenten aan HOGENT: gebruik van gamification-technieken ter bevordering van gebruikersretentie.} 
    \end{itemize}
    }
\end{frame}
}

\section{Tutorial}

\begin{frame}{List Pause}
    \begin{itemize}
        \item One \pause
        \item Two \pause
        \item Three
    \end{itemize}
\end{frame}

\begin{frame}{List Only 1}
    \begin{itemize}
        \item<1> One
        \item<2> Two
        \item<3> Three
    \end{itemize}
\end{frame}

\begin{frame}{List Only 2}
    \begin{itemize}
        \item<1-> One
        \item<2-> Two
        \item<3-> Three
    \end{itemize}

    I can do an \alert<1>{Alert}. I can also do a \textbf<2>{bold font}. Or \emph<3>{Emphasis}.
    
\end{frame}

\begin{frame}{Blocks}
\begin{block}{Title}
    Normal content
\end{block}

\begin{alertblock}{Warning}
    Alert-colored content
\end{alertblock}

\begin{exampleblock}{Example}
    Example-colored content (usually green)
\end{exampleblock}
\end{frame}

\begin{frame}{Special Environments}
\begin{block}{Remark}
some text
\end{block}

\begin{example}
This is an example
\end{example}

\begin{theorem} [Pythagoras]
$a^2+b^2=c^2$
\end{theorem}

\begin{proof}<2>
Left to the interested reader.
\end{proof}
\end{frame}

\section{Columns}

\begin{frame}{Two Column Frame}
    \begin{columns}
        \column{0.5\textwidth} \lipsum[1][1]
        \column{0.5\textwidth} \lipsum[1][2]
    \end{columns}
\end{frame}

\end{document}
```