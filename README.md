# Multi-line-equation-by-beamer
Here, the last frame demonstrates how to use beamer documentclass to present a multi-line equation line by line. By defining 

      \newcommand{\pauseditem}{\pause \item[]}

it can be done as 

      \begin{frame}
      ...
      \begin{itemize}
      \begin{eqnarray}
            (first line of the equation ending with \\)
            \pauseditem  (second line of the equation ending with \\)
            \pauseditem  (third line of the equation ending with \\)
              ...
            \pauseditem  (last line of the equation without ending \\)
      \end{eqnarray}
      \end{itemize}
      ...
      \end{frame}

Although some error messages would be reported during compiling the Latex file, the slides can be generated properly. 

