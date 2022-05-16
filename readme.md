Dit is de Github repository geëxporteerd uit Sparx Enterprise Architect door middel van een AMEFF bestand. 

1.	Opmerking vooraf.

    Sparx is niet Archimate-gecertificeerd (noch 2 noch 3.1). Dus interoperabiliteit is potentieel een probleem. 

2.	Creëren van AMEFF

    Sinds 3.1 heeft Sparx een exportfunctie naar een "Architect Exchange File" . Het resultaat is een file van ongeveer 8 mb. Dit duurt ongeveer een minuut.

3.	Importeren in Archi.

    Dat lukt helaas niet meteen.  Want het blijkt dat de AMEFF van het kernmodel in Sparx ongeldig is. Dit blijkt na speurwerk te zitten in het diagram Bedrijfsfunctiemodel DUO.  De functies in dit model zijn geplaatst in een drietal “dingen”. Ik weet niet precies wat dat zijn, maar ze hebben geen eigenschappen, alleen een naam. In AMEFF is dat vertaald naar een node van het type Label. Dat mag volgens de regels geen  subnodes hebben.  Daarom is de AMEFF van Sparx ongeldig.  Nadat de nodes zijn veranderd in het type Container lukt het wel. Conclusie: deze modelleerconstructie, die alleen in genoemd diagram voorkomt,  verbieden en vervangen door containers! Na aanpassing wordt de AMEFF in Archi gelezen in pakweg 10 sec.


4.	Folderstructuur in Archi

    Archi heeft een vaste hoofdfolderstructuur, die licht afwijkt van de structuur in Sparx. Met name de views zijn allemaal bijeengebracht onder de map Views. De Sparx-folders waar ze vandaan komen zijn subfolders geworden. Het is wel herkenbaar. Maar er zijn ook "anonieme" folders. Die hebben slechts de algemene naam Folder en verder niet. Voorbeeld: de view Organisatie DUO.  Dat is een deels genest overzicht van actoren.  De anonieme folders  blijken te slaan op de diagramnesten. Dat is redundant én het verduistert de modeltree. Ik hoop dat we dit kunnen reorganiseren. Conclusie:  Even opletten wat er gebeurt bij een round trip.

5.	Historische modellen verwijderen

    In Sparx staan nog historische diagrammen en elementen van bedrijfsobjecten. Die heb ik verwijderd. Omdat het versiebeheer in Github formeel geregeld kan worden met branches. Met branches kun je aangeven wat de productieversie is, wat de developversie en dergelijke.
 
6.   Model pushen naar Github

     Met de extensie coArchi is het mogelijk dit model te publiceren in een lege repository van Github of Gitlab o.i.d.  In totaal blijken er in het kernmodel iets meer van 10.000 verschillende elementen vertaald naar Github files (zo'n 4000 elementen en 6000 relaties). Het blijkt dat Github, althans de vrije versie, enkele beperkingen oplegt aan de upload:
     
     * Elke folder mag maximaal 1000 files bevatten. Dat komt in het kernmodel maar op één plek voor: in de folder Relations met alle 6000 relaties in één folder. Daarom zijn de relaties ingedeeld naar soort en  verdeeld over subfolders. Na wat gewurm lukt het wel.  
     
     * Een push naar github mag maximaal 3000 gewijzigde files bevatten. Aangezien het er meer dan 10.000 zijn levert de initiële push wat gedoe op. Dat heb ik in delen gedaan.  
     
           Daarmee is het model publiek gemaakt, hoewel niet gemakkelijk leesbaar. Het  kan leesbaar worden gemaakt door iedereen met (co)Archi. Personen die  zijn aangemerkt als collaborator kunnen modellen wijzigen en (laten) opnemen in de master. Zie de WIKI hoe dat in zijn werk gaat.

