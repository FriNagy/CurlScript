# CurlScript

CurlScript dient zur *Automatisierung* von Web-Anfragen ... (und anderen Sachen)   

Achtung!  
In diesem Repo sind nur die Scripten hinterlegt, ihr benötigt zusätzlich das Programm "cps.exe", das diese Scripten abarbeitet. 

Das Programm "cps.exe" findet ihr in bin Ordner. Das Programm ist derzeit noch kein open source. Wenn sich jemand an seiner mit Entwicklung beteiligen will, kann ich ihm die entsprechenden Source gerne zumailen. Derzeit sind ca. 7000 Zeilen in C++ VS2019.  

Es ist leicht übertrieben, diese Erweiterung als Script zu bezeichnen, aber für unsere Zwecke reicht es allemal. Wir können Steuerungs-Dateien erstellen, curl mit dieser Datei und diversen Parametern starten und danach das Ergebnis auswerten und von diesen abhängig dann wieder neuen Dateien erstellen, curl bei Bedarf erneut starten und Ergebnisse zurückliefern lassen usw. bis uns das exit, EOF, oder ein error scheidet ...


## Samples by category

zum Anfangen ein Einzeiler, aber es werden mehr... [minimal Hello World](samples/HelloWorld) 


<div id="paypal-button-container"></div>
<script src="https://www.paypal.com/sdk/js?client-id=sb&currency=EUR" data-sdk-integration-source="button-factory"></script>
<script>
  paypal.Buttons({
      style: {
          shape: 'rect',
          color: 'silver',
          layout: 'horizontal',
          label: 'paypal',
          tagline: true
      },
      createOrder: function(data, actions) {
          return actions.order.create({
              purchase_units: [{
                  amount: {
                      value: '3'
                  }
              }]
          });
      },
      onApprove: function(data, actions) {
          return actions.order.capture().then(function(details) {
              alert('Transaction completed by ' + details.payer.name.given_name + '!');
          });
      }
  }).render('#paypal-button-container');
</script>


<!--
### App settings
<table>
 <tr>
  <td><a href="Samples/Package">App package information</a></td>
  <td><a href="Samples/ApplicationData">Application data</a></td>
  <td><a href="Samples/Store">Store</a></td>
 </tr>
</table>
-->

