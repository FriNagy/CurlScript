# Test Markdown F.Nagy
<script src="https://kit.fontawesome.com/e40298b918.js" crossorigin="anonymous"></script>
An h1 header
============
<h1><img src="https://img.fortawesome.com/349cfdf6/fa-free-logo.svg" alt="Font Awesome Free" width="50%"></h1>

<i class="fa fa-motorcycle" style="font-size:60px;color:blue;"></i>

Paragraphs are separated by a blank line.

2nd paragraph. *Italic*, **bold**, and `monospace`. 
Itemized lists look like:

  * this one
  * that one
  * the other one

Note that --- not considering the asterisk --- the actual text
content starts at 4-columns in.

> Block quotes are
> written like so.
>
> They can span multiple paragraphs,
> if you like.

Use 3 dashes for an em-dash. Use 2 dashes for ranges (ex., "it's all
in chapters 12--14"). Three dots ... will be converted to an ellipsis.
Unicode is supported. ☺

- <kbd>Cmd+N</kbd> - New.
- <kbd>Cmd+Alt+Shift+N</kbd> - New from Template.
- <kbd>Cmd+Shift+N</kbd> - Duplicate.

[//]:test
[//]:test
[//]::Meyer
[/]:test
[/]:Meyer
[/]:een

An h2 header
------------

Here's a numbered list:

 1. first item
 2. second item
 3. third item


- Markdown files with extension: `md`, `mkd`, `mkdn`, `mdwn`, `mdown`, `markdown`, `markdn`, `mdtxt`, `mdtext` or `txt`.
- Evernotes' exports with extension: `enex`.


<div align="center">
    <kbd>Markdown</kbd> also supports &#9608; <b>HTML</b> &#9608; <i>syntax</i> <!--invisible--> <br/>
    <a href="http://www.youtube.com/watch?feature=player_embedded&v=vq2jYFZVMDA" target="_blank">
        <img src="http://img.youtube.com/vi/vq2jYFZVMDA/0.jpg" alt="GitHub Video"
        border="1" width="460" height="250"/>
    </a>
</div>


Note again how the actual text starts at 4 columns in (4 characters
from the left side). Here's a code sample:

    # Let me re-iterate ...
    for i in 1 .. 10 { do-something(i) }

As you probably guessed, indented 4 spaces. By the way, instead of
indenting the block, you can use delimited blocks, if you like:

~~~
define foobar() {
    print "Welcome to flavor country!";
}
~~~

Here's our logo (hover to see the title text):

Inline-style: 
![alt text](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Logo Title Text 1")

Reference-style: 
![alt text][logo]

[logo]: https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Logo Title Text 2"

[comment]: heloo

[//]: # (This may be the most platform independent comment)
<!-- 
(which makes copying & pasting easier). You can optionally mark the
delimited block for Pandoc to syntax highlight it:
-->

(which makes copying & pasting easier). You can optionally mark the
delimited block for Pandoc to syntax highlight it:

~~~python
import time
# Quick, count to ten!
for i in range(10):
    # (but not *too* quick)
    time.sleep(0.5)
    print(i)
~~~

und jetzt das gleiche mit diff

~~~diff cps

Scriptlines start with:
:... Label
::   goto 
>   Ausgabe 
>>   Ausgabe writeln
!>  File-Aus
!<  Eingabe ( File o. Messagebox)
??  IF oder
?!  IFNOT
#... Command
+ plus
- minus
< direkt ein
**** DIFF
+++ DIFF

#include mypass.cpo

%HEUTE Sunday

> Hello! on (%COMPUTERNAME%)
>>!

?? (%USERNAME = "Frigyes") ::EEN +1 ::UNDEF
>> also jemand andere
:: ENDE
:EEN
>> SZia Frigyes, hogy vagy
:UNDEF
!> temp.pdf < (%tmp)\nagy\test.vor nolf cpin,850
:) curl -K sss
!< .\defout.txt 
:(
exit 7

~~~
### An h3 header ###

Now a nested list:

 1. First, get these ingredients:

      * carrots
      * celery
      * lentils

 2. Boil some water.

 3. Dump everything in the pot and follow
    this algorithm:

        find wooden spoon
        uncover pot
        stir
        cover pot
        balance wooden spoon precariously on pot handle
        wait 10 minutes
        goto first step (or shut off burner when done)

    Do not bump wooden spoon or it will fall.

Notice again how text always lines up on 4-space indents (including
that last line which continues item 3 above).

Here's a link to [a website](http://foo.bar), to a [local
doc](local-doc.html), and to a [section heading in the current
doc](#an-h2-header). Here's a footnote [^1].

[^1]: Some footnote text.


Colons can be used to align columns.

| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |

There must be at least 3 dashes separating each header cell.
The outer pipes (|) are optional, and you don't need to make the 
raw Markdown line up prettily. You can also use inline Markdown.

Markdown | Less | Pretty
--- | --- | ---
*Still* | `renders` | **nicely**
1 | 2 | 3


A horizontal rule follows.


Again, text is indented 4 spaces. (Put a blank line between each
term and  its definition to spread things out more.)

Here's a "line block" (note how whitespace is honored):

| Line one
|   Line too
| Line tree

and images can be specified like so:

![example image](example-image.jpg "An exemplary image")

Inline math equation: $\omega = d\phi / dt$. Display
math should get its own line like so:

$$I = \int \rho R^{2} dV$$

And note that you can backslash-escape any punctuation characters
which you wish to be displayed literally, ex.: \`foo\`, \*bar\*, etc.
