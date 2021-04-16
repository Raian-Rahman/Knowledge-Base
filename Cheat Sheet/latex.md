# Overview
This file contains cheats for writing a technical report. We often forget important ```Latex``` tags while writing a paper. You can search from this document for it. 

# Important Links
Although latex needs to be installed on host machine, we can use different online resources to use latex online. Some of the important links are:
- *Overleaf* : ```https://www.overleaf.com/project```
- *Overleaf Teamplates* : ```https://www.overleaf.com/latex/templates```
- *Overleaf Documentation* : ```https://www.overleaf.com/learn```
- *Table Generator* : ```https://www.tablesgenerator.com/```

# Conventions while writing paper
- Always reference the tables or images using ```\ref{label}``` tag
- Never use ``$eqn$`` sign to write equation. Use 
    ``` latex
    \begin{align}
        (a+b)^2 = a^2 + 2ab + b^2
    \end{align}
    ```
- If citation of a website is not found, add the link to the website in the footnote
- Don't add too much details on a caption of table. But, we can explain an image in the caption
- To show multiplication sign, use ```\times``` to show the multiplication sign in an equation
- Use $0.00002$ to show the number in a paper. Don't use it as plain text
- Always put table or figures at the top or bottom of the page. Putting image in between will cause waste of space


# Basic Tags
There are some basic operaion in latex. Some of the important tasks are given below:

## Document Formatting
### Specifying Multiple Columns
To have multiple colimns in a text we need to could use multicols tag. Code is demonstrated below:
``` latex
\usepackage{multicols}

\begin{multicols}{2}
\end{multicols}
```
### Page and Margin
Documents can be both single column and multicolumn. Also, sometimes, we need to specify the margin size. These can be done with ```geometry``` package of latex. 

To set the paper's size and margin size, we can use the following command:
``` latex
\usepackage[
a4paper, % for specifying the size
total = {8 in, 6 in} %for specifying the page margin
]{geometry}
```
### Horizontal Line
To add horizontal line we could use ```\hline``` tag

### Vertical and Horizontal Spacing
We often need vartical and horizontal spacing in a page. For vertical spacing we will get free space between the lines of the specified length. Horizontal spacing will provide us with the same operation like ```\vspace``` but in a *horizontal* way. Code is demontrated below:
``` latex
\begin{document}
We are writing \latex code.\\
\vspace{0.2 in} % vertical space between these two lines
A space between them
\end{document}
```
### Including Images in paper
**[A Rule of thumb while writing a paper is always put images in the top or bottom of the page]**

Images can be included using ```graphicx``` package. An example of including images in a document is given below:
``` latex
\usepackage{graphics}
\begin{figure}[t] %specifying where to put the image
     \centering % to make the image center aligned
     \includegraphics[width = \textwidth]{Paper Pipeline.png}  %\textwidth is used to specify the width of a page,
     \caption{write a caption}  % it is used to add caption in an image. Put caption before include graphics to 
                                % add captions over the image 
     \label{steady_state}       % add a label to reference the image
\end{figure}
```
### Including Multiple Images as a single image
Multiple images can be included using ```subfig``` package. An example of including images in a document is given below:
``` latex
\usepackage{subfig}
\usepackage{graphics}

\begin{figure}
     \centering
     \subfloat[][caption for particular image]{\includegraphics[width = 1.5 in]{mislabel_0.png}\label{<figure0>}}
     \hspace{.05 in} %hspace is added to add horizontal space between the images
     \subfloat[][caption for particular image]{\includegraphics[width = 1.5 in]{mislabel_1.png}\label{<figure1>}}
     \hspace{.05 in} %hspace is added to add horizontal space between the images
     \subfloat[][caption for particular image]{\includegraphics[width = 1.5 in]{mislabel_2.png}\label{<figure2>}}
     \caption{add captions}
     \label{mislabeled}
\end{figure}
```

### Designing Table in a paper
Tables can easily be designed using Graphical User Interface with ```https://www.tablesgenerator.com/```. After developing the table, we could add those into document by generating a latex code and paste it into the document. **No demonstration is given here**

To fix the width of a table we could use ```\resizebox``` package. 

A demonstration is given below:
``` latex
\usepackage{graphicx}
\begin{table}[]
\centering
\caption{whatever caption you want}
\label{tab:my-table}
\resizebox{\textwidth}{!}{%
\begin{tabular}{lll}
a & b & c \\
d & e & f \\
g & h & i
\end{tabular}
}
\end{table}
```
# Paper Formats
There are different kind of paper templates available. The most common ones are:
- Springer format
- IEEE format
Tags can be different based on the format. Different tags are given below:
