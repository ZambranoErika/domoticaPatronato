# domoticaPatronato

##Intro
Progetto domotico per uso domestico, per accendere e spegnere le luci da remoto.
Il progetto utilizza un **Raspberry 3B+** e una scheda relè.
il software utilizzato è **OpenHabian** e **MQTT**(tramite mosquitto). 
L'attuazione dell'impianto avviene tramite il servizio cloud di OpenHab, su una paginaweb, oppure tramite la app di openhab
![openhab screenshot](https://image.ibb.co/eoFCVq/openHab-screen.png)

### stato del progetto
Il primo prototipo funziona, lo sviluppo è concluso, essendo servito per uso didattico, all'interno del corso, Digital Tecnology and development.
attivo mantenimento 


##Hardware
BOM (Bill of materials):
* raspberry Pi 3+
* modulo relè optoisolato, con il numero di canali necessari
* cavi
* Jumper Dupont
* un led per canale
* un pulsante 6*6 mm


##Software
istruzione per l'installazione:

1. installare openHabian, proseguendo da [guida ufficiale](https://www.openhab.org/download/)
1. prima del primo avvio creare il file (vuoto) `ssh ` nella root della SD, e non deve esserci nessuna estenzione
1. Trovare l'ip del raspberry e trovare un client SSH (*ad esempio putty*) per connettersi.
1. Di default per connettersi la password è **openhabian** ed anche l'ip
1. aggiornare il sistema con: 
    ```
    sudo apt upgrade
    sudo apt update
     ```
  
1. nella cartella /etc/openhab2/items/ crea all'interno su nano il tuo file con la estenzione *user.items* indicando i diversi pin ai relè come indicato nel sito [ufficiale](https://www.openhab.org/docs/concepts/items.html#item-metadata)

**grassetto**

*corsivo* *

**_grassetto corsivo_** **_

