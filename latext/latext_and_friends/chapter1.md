#Basics

LATEX was written by Leslie Lamport as an extension of Donald Knuth's TEX
program. It consists of a Turing complete procedural markup language and a
typesetting processor.

The combination of the two lets you control both the visual presentation as
well as the content of your documents. 

1. Write document in a Latex (.tex) input (source) file.
2. Run the latext or _pdf_latex program on input file. This truns input file
   into a device independent (._dvi_) file or portable document format (._pdf_)
   file. If there are errors, fix them.
3. View _dvi_ or _pdf_ file on computer. A _dvi_ file cannot be printed directly it
   needs to be converted to postscript of _pdf_ file.

## The TEX Processors
The four main processors are
```
1. Input Processor
2. Expansion Processor
3. Execution Processor
4. Visual Processor
```
### Input Processor
Turns the source file into a token stream. The resulting token stream is sent
to the Expansion Processor.

### Expansion Processor
Truns the token stream into a token stream. Expandable tokens are repeatedly
expanded until there are no more left. The expansion applies to commands,
conditionals, and some primitive commands. The resulting output is sent to the
Execution Processor

### Execution Processor
Executes executable control sequences. These actions may affect the state.
This applies, for example, to assignmments and command definitions. The
Execution Processor also constructs horizontal, vertical and mathematical
lists. The final output is sent to Visual Processor

### Visual Processor
Creates the _dvi_ or _pdf_ file. This is the final stage. It truns horizontal
lists into paragraphs, breaks vertical lists into pages, and truns
mathematical list into formulae.

## From _tex_ to _dvi_ and Friends
```
Example file : (base name).tex

$latex (base name).tex		# converts source file into output file (.dvi)
$latex (base name)			# extension can be omitted
$xdvi (base name).dvi &		# .dvi file can be viewed by xdvi program
$xdvi -o (base name).ps (base name).dvi		# convert to ps format
$dvipdf (base name).dvi		# converts to pdf file
$pdflatext (base name).text	# easiest way to convert pdf
```

## Writing a Latex Input Document
Latex is a markup language and document preparation system. It forces you to
focus on the content and not on the presentation.

### Content
Contents is determined in terms of text and logical markup. Latext forces to
focus on logical structure of document. This structure is provided as markup
in terms of familiar notions.

### Commands
Main purpose of commands is to provide markup. Lets you define your own
commands. These commands let you do real programming and give ultimate control
over the content. Commands can be reused by making it a library.

### Libraries
There are many existing document classes and packages (style files). Class
files define rules that determine the apperance of output document. They also
provide the required markup commands. Packages are best viewed as library.
They provide useful commands that automate many tedious tasks.

### Show Structure
Carefully formatting the input shows the structure of Latex source files. This
makes it easier to locate the start and end of the sentences and higher level
building blocks such as environments.

### Mimic Output
By formatting the input you can mimic the output. o

### Find Errors
Formatting may help to find the cause of errors more quickly.


## Minor Document Divisions
Latex provides the following divisions
```
part		- An optional unit that is used for major divisions
chapter		- A chapter in a book or report
sections	- A section, subsection, or subsubsection
paragraphs	- A named paragraph or named subparagrah
```
