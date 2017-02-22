#Running Text

##Special Characters
When Special characters show up in input stream, Tex doesn't typeset them but,
instead changes state.


| Token | Purpose | Command
|---| ---| ---|
| # | parameter reference | \#
| $ | math mode switch | \\$
| % | start of comment | \\%
| & | alignment tab | \\&
| ~ | test tie token | \\textasciitilde
| _ | math subscript | \\_
| ^ | math superscript | \\textasciicircum
| { | start of group | \\{
| } | end of group | \\}
| \ | start of command | \\textbackslash or \\backslash

###Tieing Text
LaTex is a large rewriting machine that repeatedly turns token sequences into
token sequences. At some state, it turns token sequence into lines. This where
LaTex determins the line breaks.o
The tilde(~) defines an inter-word space that cannot be turned into a line
break. As such it may be viewed as an operator that ties words.

###Grouping
Grouping is a common technique in LaTex. The opening brace ({) starts a group
and closing brace (}) closes it. Grouping has two purposes. The first purpose
of grouping is that it turns several things into one compound thing. 

This may be needed, for example, if you want to pass several words to command
that typesets its arguments in bold face text.

The second purpose of grouping is that it lets you change certain settings and
keep the changes local to that group. Inside the group, you may have several
paragraphs. 

