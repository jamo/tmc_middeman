# TMC plugin ja ääkköongelmat

Osalla kurssilaisilla on ollut ääkkösongelmia TMC-tehtävien virheilmoituksissa. Tällöin ääkköset näkyvät virheilmoituksissa epämääräisinä merkkeinä. 

Mikäli sinulla ei ole ollut tätä ongelmaa, voit lopettaa viestin lukemisen tähän.  
 
Te, joilla tämä ongelma on, tunnistatte sen varmasti ylläolevasta kuvauksesta.  

TMC pluginissa ollut bugi on korjattu, mutta korjatun TMC pluginin massajakelu ei ole mahdollista NetBeanssin 7.2.1 -versiossa olevan bugin* takia.  

Tämä korjaus on kuitenkin saatavilla, ja asentuu mitä todennäköisemmin ongelmitta. 

Tässä vielä ohje muualla hostatun pluginin asennukseen: https://www.youtube.com/watch?v=yxFeZihtRgM

Ohjeet tarvittaessa myös tekstinä:

* Avaa NetBeans, jollei se ole jo auki.  
* Valikosta Tools | Plugins   
    * Välilehti Installed  
        * Rastita "User Installed Plugins / Test My Code Plugin"  ja valitse Uninstall  
        * Vanha TMC plugin asennus poistuu.  
* Uudelleenkäynnistä NB päivityksen jälkeen.  
* Valikosta Tools | Plugins  
    * Välilehti Settings  
        * Vasemmasta sarakkeesta TMC, tai se nimi, jonka sille vanhan TMC pluginin asennuksen  yhteydessä annoit.  
        * Valitse se ja oikeasta yläreunasta Edit  
    	* Vaihda sen URLin tilalle http://jamo.fi/updates/updates.xml  
    * Välilehti Available plugins  
    	* Valitse TMC listasta ja valitse Install.
    	* TMC Plugin asentuu normaalisti, hyväksy käyttöehdot ja allekirjoittamattoman pluginin asennus
 
Mikäli NetBeans käynnistyy TMC:n päivittämisen jälkeen virheettömästi, kaikki on hyvin ja voit jättää tämän ohjeen lopun huomiotta. 
Jos taas saat virheviestin "Warning - could not install some modules", toimi seuraavasti.

### Linux-Käyttäjät
	- Uudelleennimeä kotihakemistossasi oleva .netbeans/ -kansio seuraavalla komennolla 
 	`cd ~/ ; mv .netbeans/ .netbeans.old/`
	
### Mac-käyttäjät:
	Uudelleennimeä kansio ~/Library/Application Support/NetBeans/ 
	`mv  ~/Library/Application\ Support/NetBeans/   ~/Library/Application\ Support/NetBeans.old/ ` 

### Windows-käyttäjät:
  	Uudelleennimeä seuraava kansio:

#### Windows 7 / Vista:
    	C:\Users\%username%\AppData\Roaming\NetBeans
	    JA
	    C:\Users\%username%\AppData\Local\NetBeans

### Windows XP:
    	C:\Documents and Settings\%username%\Application Data\NetBeans

  **HUOM. voit kopioida polun suoraan resurssienhallintaikkunaan.**
  
  (AppData ja Application Data ovat piilotettuja)

Nyt NetBeans käynnistyessään ajattelee käynnistyvänsä ensimmäistä kertaa. Asenna plugin uudestaan videon ohjeiden mukaisesti. Aloita 0:50 kohdalta http://youtu.be/yxFeZihtRgM?hd=1&t=50s .



*http://netbeans.org/bugzilla/show_bug.cgi?id=218373