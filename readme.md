Dit is de Github repository geëxporteerd uit Sparx Enterprise Architect door middel van een AMEFF bestand. 

1.	Opmerking vooraf.

    Sparx is niet Archimate-gecertificeerd (noch 2 noch 3.1). Dus interoperabiliteit is potentieel een probleem. 

2.	Creëren van AMEFF

    Sinds 3.1 heeft Sparx een exportfunctie naar een "Architect Exchange File" . Het resultaat is een file van ongeveer 8 mb. Dit duurt ongeveer een minuut.

3.	Importeren in Archi.

    Dat lukt helaas niet meteen.  Want het blijkt dat de AMEFF van Sparx ongeldig is. Dit blijkt na speurwerk te zitten in het diagram Bedrijfsfunctiemodel DUO.  De functies in dit model zijn geplaatst in een drietal “dingen”. Ik weet niet precies wat dat zijn, maar ze hebben geen eigenschappen, alleen een naam. In AMEFF is dat vertaald naar een node van het type Label. Dat mag volgens de regels geen  subnodes hebben.  Daarom is de AMEFF van Sparx ongeldig.  Nadat de nodes zijn veranderd in het type Container lukt het wel. Conclusie: deze modelleerconstructie, die alleen in genoemd diagram voorkomt,  verbieden en vervangen door containers! Na aanpassing wordt de AMEFF in Archi gelezen in pakweg 10 sec.


4.	Folderstructuur in Archi

    Archi heeft een vaste hoofdfolderstructuur, die licht afwijkt van de structuur in Sparx. Met name de views zijn allemaal bijeengebracht onder de map Views. De Sparx-folders waar ze vandaan komen zijn subfolders geworden. Het is wel herkenbaar. Maar er zijn ook "anonieme" folders. Die hebben slechts de algemene naam Folder en verder niet. Voorbeeld: de view Organisatie DUO.  Dat is een deels genest overzicht van actoren.  De anonieme folders  blijken te slaan op de diagramnesten. Dat is redundant én het verduistert de modeltree. Ik hoop dat we dit kunnen reorganiseren. Conclusie:  Even opletten wat er gebeurt bij een round trip.

5.	Historische modellen verwijderen

    In Sparx staan nog historische diagrammen en elementen van bedrijfsobjecten. Die heb ik verwijderd. Omdat het versiebeheer in Github formeel geregeld kan worden met branches. Met branches kun je aangeven wat de productieversie is, wat de developversie en dergelijke.
 
6.	Laden  in Github

    Met de extensie coArchi is het mogelijk dit product omzetten in een Collaboration Workspace voor Github of Gitlab o.i.d en vervolgens te publiceren. Daarmee is het publiek, hoewel niet meteen leesbaar. Het kan leesbaar worden gemaakt door iedereen met (co)Archi. Personen zijn aangemerkt als collaborator kunnen modellen wijzigen en (laten) opnemen in de master. Zie de WIKI hoe dat in zijn werk gaat.

