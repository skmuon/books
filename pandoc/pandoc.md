# Tips for Pandoc

```
Convert a doc.md (markdown) files into a single PDF document
$pandoc -s -o doc.pdf doc.md

Convert multiple md files to single PDF document
$pandoc -s -o doc.pdf part01.md part02.md

Changing the page margins in resulting PDF
$pandoc -s -v geometry:margin=1in -o doc.pdf doc.md

Create HTML or DOCX document
$pandoc -s -o doc.html doc.md
$pandoc -s -o doc.docx doc.md
```




