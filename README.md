# Multi-line-equation-by-beamer
Many people use LaTeX mainly for its ability to generate good-looking and consistent equations. As a LaTeX documentclass, beamer can further help to make frames and slides for presentations, where no problem for single-line euqations at all. However, after many tests, I believe the following way is the only reasonable one for presenting a multi-line equation line by line with beamer, with no unexpected manual effort. 

By defining 

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

Although some error messages would be reported during compiling the LaTeX file, the slides can be generated properly. As an example, in the slides of the last frame, all equal signs are aligned and equation numbers are generated for each line without any further manual interference. 

