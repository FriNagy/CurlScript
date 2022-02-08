## Curlscript first steps

Hello World Programm (kürzer geht kaum)

     > Hello World...
    
 
mit `>` am **Zeilenanfang** wird eine Ausgabe gestartet,
wir geben die Zeile ohne rechte Leerzeichen, mit abschliessende Zeilenschaltung aus.
Die Zeilenschaltung am Zeilenenende wird abgeschaltet wenn die Zeile mit `>~` startet.

<style id="wp-custom-css">
kbd {
background-color: rgba(100, 255,100, 1);
font: 15px Monaco, Consolas, "Andale Mono", "DejaVu Sans Mono", monospace;
margin-right: 7px;
}
</style>
		
<details>
 <summary>Befehle zu direktausgabe, Click to show more...</summary>
 <markdown>  
      
| Befehl        | Code    |    
| ------------- |---------| 
| writeln       | `>`     | 
| write         | `>~`    | 
| write-get-ln  | `><`    |  
 </markdown>
 </details>

auch mit Unicode...
 
     <kbd>Alt-N</kbd>
Console Codepage und Schriftart sollte natürlich unicode können 

     > Hello World...
     > Grüßt Euch, Привет, Csókolom, 你好

und mit Variablen:

     > Hello World...
     > Grüßt Euch, Привет, csókolom, 你好
     >
     > bin als User: (%USERNAME%) angemeldet
     
Starting from Windows 10 the Windows console support ANSI Escape Sequences  
https://docs.microsoft.com/en-us/windows/console/console-virtual-terminal-sequences  
( HK_CU\Console\VirtualTerminalLevel muss auf 1 sein)

     > Hello World...
     > Grüßt Euch, Привет, csókolom, 你好
     >
     > bin als User: (%USERNAME%) angemeldet
     >               (%/27)[41m  ROT  (%/27)[47m WEISS (%/27)[42m  GRÜN  (%/27)[40m   
     >               (%/27)[41m  ROT  (%/27)[47m WEISS (%/27)[42m  GRÜN  (%/27)[40m   


<details>
  <summary>Click to show more...</summary>
  <markdown>   
       
 | Befehl        | Code    |      
 | ------------- |---------| 
 | writeln       | `>`     | 
 | write         | `>~`    |        
   </markdown>
   
   <details>
  <summary>Click to show more...</summary>
  <markdown>   
       
 | Befehl        | Code    |      
 | ------------- |---------| 
 | writeln       | `>`     | 
 | write         | `>~`    |        
   </markdown>
</details>
</details>
