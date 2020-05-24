### Curlscript first steps

Hello World Programm (kürzer geht kaum)

     > Hello World...
    
 
mit `>` am **Zeilenanfang** wird eine Ausgabe gestartet,
wir geben die Zeile ohne rechte Leerzeichen, mit abschliessende Zeilenschaltung aus.
Die Zeilenschaltung am Zeilenenende wird abgeschaltet wenn die Zeile mit `>~` startet.

<details>
 <summary>Click to show more...</summary>
     
| Befehl        | Code    | Aktion         
| ------------- |---------| 
| writeln       | `>`     | 
| write         | `>~`    | 
| write-get-ln  | `><`    |  

</details>

natürlich auch mehrzeilig, mit Unicode

     > Hello World...
     > Grüßt Euch, привет, csókolom, 你好

aber auch mit Variablen:

     > Hello (%USERNAME%)
 <details>
  <summary>Click to show more...</summary>
  <markdown>   
 | Befehl        | Code    |      
 | ------------- |---------| 
 | writeln       | `>`     | 
 | write         | `>~`    |        
  </markdown>
</details>
