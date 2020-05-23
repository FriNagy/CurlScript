# Textbelt

*CurlScript,  Sende SMS mit https://textbelt.com/* 

minimalistisches Script zum senden von SMS Textnachrichten 


<nav style="background-color:gray;border:2px solid DodgerBlue;">
<a href="/html/"> ___HTML</a> |
<a href="/css/">___CSS</a> |
<a href="/js/">JavaScript</a> |
<a href="/jquery/">jQuery</a>
</nav>


```powershell

php

{
  { "taxCode": (%CO1), "quantity": 1, "amount": (%AMO1), "description": (%DESC1) } // und sonst
"type": "SalesOrder", 
  "date": "(%DOCdate)", eras move
  "customerCode": "(%customerCode)",
  "addresses": { 
  "shipTo": {"line1":"(%TOLINE1)","city": "(%TOCITY)","region": "(%toregion)","country": "US","postalCode": "(%TOPOSTALCODE)"},
  "shipFrom": { "line1": "(%FROM,4)", "city": "(%FROM,3)", "region": "(%FROM,1)", "country": "US", "postalCode": "(%FROM,2)" } }, 
  "lines": [ 
?! test dfsd (%hello%)
  { "taxCode": "(%CO1)", "quantity": 1, "amount": (%AMO1), "description": "(%DESC1)" } // und sonst
if (%CO2) :LASTLINE  // und sonst lasses
 ,{ "taxCode": "(%CO2)", "quantity": 1, "amount": (%AMO2), "description": "(%DESC2)" }
ifnot (%CO3) goto LASTLINE gosub hello :((
 ,{ "taxCode": "(%CO3)", "quantity": 1, "amount": (%AMO3), "description": "(%DESC3)" }
?! (%CO4) :LASTLINE
 ,{ "taxCode": "(%CO4)", "quantity": 1, "amount": (%AMO4), "description": "(%DESC4)" }
:LASTlINE
]}

```

```diff

css

{ "type": "SalesOrder", 
  "date": "(%DOCdate%)", 
  "customerCode": "(%customerCode)",
  "addresses": { 
  "shipTo": {"line1":"(%TOLINE1)","city": "(%TOCITY)","region": "(%toregion)","country": "US","postalCode": "(%TOPOSTALCODE)"},
  ***  "shipFrom": { "line1": "(%FROM,4)", "city": "(%FROM,3)", "region": "(%FROM,1)", "country": "US", "postalCode": "(%FROM,2)" } }, 
  "lines": [ 
@@  { "taxCode": "(%CO1)", "quantity": 1, "amount": (%AMO1), "description": "(%DESC1)" }
+?! (%CO2) :LASTLINE
 ,{ "taxCode": "(%CO2)", "quantity": 1, "amount": (%AMO2), "description": "(%DESC2)" }
+?! (%CO3) :+LASTLINE + :((
 ,{ "taxCode": "(%CO3)", "quantity": 1, "amount": (%AMO3), "description": "(%DESC3)" }
+?! (%CO4) :LASTLINE
 ,{ "taxCode": "(%CO4)", "quantity": 1, "amount": (%AMO4), "description": "(%DESC4)" }
-:LASTlINE
]}

```




zuerst estellen wir die sende Datei:

<code> txt sendmee.txt 
 --data-urlencode phone='(%1)'
 --data-urlencode "message=(%%i %%2)"
  -d key=b02ed54a4991de0ff70726cc6d3faec24e94c6rbIjmVAmeDztlxfgR24uwf6He
<\code>

dann die Steurungsdatei für Curl

``` !> curlin.txt @run
-k
--host https://textbelt.com/text
--out  backfromcurl.txt
```

nach dem start lesen wir die Ausgabedatei, und weisen zu unsere Variablen zu

    !< backfromcurl.txt "success":, "quotaRemaining":} "error":""

also wir haben jetzt 3 Variablen (sehen zwar recht ungewöhnlich aus)

- `"success":,` `"quotaRemaining":}` `"error":""`

\if `"success":,` = true :gesendet :smsfehler :progfehler
 
 <span style="font-family:Papyrus; font-size:4em;">VERLIEBT!</span>
 
[]:# (This actually is the most platform independent comment)
 
[//]:# This actually is the most platform independent comment)

und ein xml:

~~~ xml trim nolf 
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:ses="https://finanzonline.bmf.gv.at/fon/ws/session">
 <soapenv:Header/>
   <soapenv:Body>
      <ses:loginRequest>
         <ses:tid>(%tid       )</ses:tid>
         <ses:benid>(%benid   )</ses:benid>
         <ses:pin>(%invo1)(%pin)</ses:pin>
         <ses:herstellerid>(%herrid)</ses:herstellerid>
      </ses:loginRequest>
   </soapenv:Body>
 </soapenv:Envelope>
~~~

oder eben ein JSON

~~~ powershell <!-- !> json.tmp NOLF NOLF //////////////////////////////////

{ "type": "SalesOrder", 
  "date": "(%DOCdate)", 
  "customerCode": "(%customerCode)",
  "addresses": { 
  "shipTo": {"line1":"(%TOLINE1)","city": "(%TOCITY)","region": "(%toregion)","country": "US","postalCode": "(%TOPOSTALCODE)"},
  "shipFrom": { "line1": "(%FROM,4)", "city": "(%FROM,3)", "region": "(%FROM,1)", "country": "US", "postalCode": "(%FROM,2)" } }, 
  "lines": [ 
  { "taxCode": "(%CO1)", "quantity": 1, "amount": (%AMO1), "description": "(%DESC1)" }
?! (%CO2) :LASTLINE // wenn kein zweites code, > lasses
 ,{ "taxCode": "(%CO2)", "quantity": 1, "amount": (%AMO2), "description": "(%DESC2)" }
?! (%CO3) :LASTLINE
 ,{ "taxCode": "(%CO3)", "quantity": 1, "amount": (%AMO3), "description": "(%DESC3)" }
?! (%CO4) :LASTLINE
 ,{ "taxCode": "(%CO4)", "quantity": 1, "amount": (%AMO4), "description": "(%DESC4)" }
:LASTlINE
]}

~~~

<!-- Hallo Frigyes --->



curl -K cmdlpars.txt  // wir starten curl. alle Parameter sind in cmdlpars.txt  

!< back.txt %am="date":" %tax="totalTax":^, %amount="totalAmount":^, %nont="nonTaxableAmount":^,

<< Total Tax: (%tax)\n\n\nvon: (%Amount)\nnonTaxable: (%nont)\n\nin Schein: (%oldwert)  (Kunde: (%KUNUM))

!> .\getan.txt cpout850 /////////////

(%tax)


 
 wenn Null war alles OK,
 

:gutgemacht

!>> sms.log am: (%%d) (%%z)  Tel.Nr: (%%1) Text: (%%2) 

>> 
>> Gut gemacht ...  
>> 
>> es bleiben noch:  (%"quotaRemaining":}) freie SMS

?!  "quotaRemaining":}    10   eof

>> Leider nun mehr 10 Freie SMS
>> sende SMS to Admin 

!> sendmee.txt 

 --data-urlencode phone='+4366488250150'
 --data-urlencode "Hey Admin! nun mehr 10 Freie SMS bei Textbelt! bitte verl├ñngern..."
 -d key=b02ed54a4991de0ff707267ccc6d3faec24e94c6rbIjmVAmeDztlxfgR24uwf6He

<x> curl -k -s -S -k -X POST https://textbelt.com/text -K sendmee.txt -o stepl.txt

?? eof 


?? writemee


``` 

Hallo da sind wir zwischen die Stühle //dssadf

```
[//]:#dl style="background-color:Tomato;border: 3px solid;border-color: black #444 #888 #ccc;font-family:consolas;">
