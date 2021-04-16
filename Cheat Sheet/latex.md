# Overview
This file contains cheats for writing a technical report. We often forget important ```Latex``` tags while writing a paper. You can search from this document for it. 

# Important Links
Although latex needs to be installed on host machine, we can use different online resources to use latex online. Some of the important links are:
- *Overleaf* : ```https://www.overleaf.com/project```
- *Overleaf Teamplates* : ```https://www.overleaf.com/latex/templates```
- *Overleaf Documentation* : ```https://www.overleaf.com/learn```
- *Table Generator* : ```https://www.tablesgenerator.com/```

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
# Paper Formats
There are different kind of paper templates available. The most common ones are:
- Springer format
- IEEE format
Tags can be different based on the format. Different tags are given below:
