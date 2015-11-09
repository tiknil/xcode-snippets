# Xcode snippets

Snippets di codice Obj-X per lo sviluppo iOS e OSX utili per migliorare il tuo lavoro in termini di velocità ma anche di qualità del codice. (Vedi [Obj-C Style Guide by Tiknil](https://github.com/tiknil/objective-c-style-guide))

## Come tenerli aggiornati su XCode? ##

#### (1) XCode plugin ####

Installare [ACCodeSnippetRepository](https://github.com/acoomans/ACCodeSnippetRepositoryPlugin) by Arnaud Coomans (@acoomans) in XCode buildando il sorgente oppure tramite [Alcatraz](https://github.com/supermarin/Alcatraz) plugin package manager. Quindi configurare il plugin impostando come repository degli snippets questo repository. That's all!

oppure, se per qualche motivo non dovesse funzionare il plugin sopracitato:

#### (2) Link simbolico e repo locale ####

Pullare il repo e impostare i riferimenti simbolici alla cartella corretta, in questo modo: 
 * Pullare il presente repository (o meglio una vostra fork + pull, così potrete fare delle pull request se avrete snippets interessanti!) in una vostra cartella (da ora `$XCODE_SNIPPETS_FOLDER`)
 * Fare una copia di backup del contenuto della cartella `~/Library/Developer/Xcode/UserData/CodeSnippets` sul vostro mac: sono tutti i vostri snippets creati finora, se è vuota, meglio così!
 * Eliminate la cartella
 * Da Terminale eseguite il comando 

`ln -s $XCODE_SNIPPETS_FOLDER ~/Library/Developer/Xcode/UserData/CodeSnippets` 

   così da creare un link simbolico tra il vostro repo e la cartella dove XCode si aspetta di trovare i vostri snippets
 * Potete anche copiare nella cartella del repo gli snippets di cui avete fatto il backup
 * Chiudete e riaprite XCode e i vostri snippets dovrebbero trovarsi già lì
