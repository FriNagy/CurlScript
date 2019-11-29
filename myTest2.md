# Textbelt

*CurlScript,  Sende SMS mit https://textbelt.com/* 

curl starten mit Parameter ... , Ausgabe nach step1.txt, stderr nach lasterr.txt
mit -s silent -S aber Fehlermeldungen -k https ohne zert. erlauben


[//]:test

[//]:test2
[//]::Meyer
[/]:test

[//]: Meyer und ich 

[/]: een es te


<h1>My First Page</h1>
<p>This is my first page.</p>
<a href="#faq">Click here to read the Frequently Asked Questions</a>
<hr/>
  <h3 id="faq">Frequently asked questions</h3>
<p>The first rule about fight club is that you do not talk about fight club.</p>
<p>However, if you do have questions, please e-mail me at foo@bar.com</p>


<dl style="background-color:Tomato;border:2px solid DodgerBlue;font-family:consolas;">
  <dt>Definition list</dt>
  <dd>Is something people use sometimes.</dd>

  <dt>Markdown in HTML</dt>
  <dd>Does *not* work **very** well. Use HTML <em>tags</em>.</dd>
</dl>

[//]:# (das wird IN md nicht ausgegeben, aber als Script ausgeführt)

:= :MYLOOP

:> MYLOOP

:>:MYLOOP

 <p>Here is a quote from WWF's website:</p>
<blockquote cite="http://www.worldwildlife.org/who/index.html">
For 50 years, WWF has been protecting the future of nature.
The world's leading conservation organization,
WWF works in 100 countries and is supported by
1.2 million members in the United States and
close to 5 million globally.
</blockquote> 
<p>Display a gauge:</p>
<meter value="2" min="0" max="10">2 out of 10</meter><br>
<meter value="0.6">60%</meter>

<p><strong>Note:</strong> The &lt;meter&gt; tag is not supported in Internet Explorer, Edge 12, Safari 5 and earlier versions.</p>

<nav>
<a href="/html/">HTML</a> |
<a href="/css/">CSS</a> |
<a href="/js/">JavaScript</a> |
<a href="/jquery/">jQuery</a>
</nav>



<canvas id="myCanvas">Your browser does not support the HTML5 canvas tag.</canvas>

<script>
var c = document.getElementById("myCanvas");
var ctx = c.getContext("2d");
ctx.fillStyle = "#FF0000";
ctx.fillRect(0, 0, 80, 100);
</script>


<!-- # das auch nich wird nicht ausgegeben DAS --(%>) ABER
 geht natürlich auch in block
 wie gesgt Leerzeichen auch da als kommenter
 wir betrachten nur die Zeilen die mit #, :, !, ?, >, (%  starten
 bzw. mit dem Wort: curl cmd command ps run cps
# das auch nich wird nicht ausgegeben -->


~~~
curl -s -S -k -X POST httpS://textbelt.com/text \
    --data-urlencode phone='+43664880150' \
    --data-urlencode "message=Hallo! wollte nur schönen Tag wünschen!" \
    -d key=my-geheim-key -o step1.txt 2>lasterr.txt 
?? :(
~~~

  exit-code (=lastexit) auswerten (if lastexit not 0 goto exefehler)
?!  lastexit 0 exefehler 

    // curl output einlesen, Variable(n) suchen und zuweisen ( zB: "success":, suche "success": und zuweise bis ',')
    !<  step1.txt "success":, 

    // Variablen prüfen, ( if  ("success":,) not (true) goto @leider: )
    ?!  "success":, true leider

    // Rückmeldung ausgeben
>> 
>> _OK_ SMS  gesendet ...  
>>
?? exit 0

@exeFEHLER:
>> 
>> *** Curl hat einen Fehler gemeldet (Exit Code: (%%vlastexit))
>>     siehe lasterr.txt
>> 
?? exit 7

@leider:
>> 
>> *** Fehler beim senden von SMS 
>> 
?? exit 9

