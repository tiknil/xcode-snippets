# Xcode snippets

Snippets di codice Obj-X per lo sviluppo iOS e OSX utili per migliorare il tuo lavoro in termini di velocità ma anche di qualità del codice. (Vedi [Obj-C Style Guide by Tiknil](https://github.com/tiknil/objective-c-style-guide))

## Come tenerli aggiornati su XCode? ##

#### (1) XCode plugin ####

Installare [ACCodeSnippetRepository](https://github.com/acoomans/ACCodeSnippetRepositoryPlugin) by Arnaud Coomans (@acoomans) in XCode buildando il sorgente oppure tramite [Alcatraz](https://github.com/supermarin/Alcatraz) plugin package manager. Quindi configurare il plugin impostando come repository degli snippets questo repository. (Richiede il fork del repo)

oppure, se per qualche motivo non dovesse funzionare il plugin sopracitato:

#### (2) Link simbolico e repo locale ####

Pullare il repo e impostare i riferimenti simbolici alla cartella corretta, in questo modo: 
 * Pullare il presente repository (o meglio una vostra fork + pull, così potrete fare delle pull request se avrete snippets interessanti!) in una vostra cartella (da ora `$XCODE_SNIPPETS_FOLDER`)
 * Fare una copia di backup del contenuto della cartella `~/Library/Developer/Xcode/UserData/CodeSnippets` sul vostro mac: sono tutti i vostri snippets creati finora, se è vuota, meglio così!
 * Eliminate la cartella
 * Da Terminale eseguite il comando 

`ln -s $XCODE_SNIPPETS_FOLDER/snippets ~/Library/Developer/Xcode/UserData/CodeSnippets` 

   così da creare un link simbolico tra il vostro repo e la cartella dove XCode si aspetta di trovare i vostri snippets
 * Potete anche copiare nella cartella del repo gli snippets di cui avete fatto il backup
 * Chiudete e riaprite XCode e i vostri snippets dovrebbero trovarsi già lì

## Alcuni esempi ##

#### `def` ####

Questo snippet è molto comodo per organizzare il codice di implementazione delle classi in modo coerente. Basta cominciare a digitare `def` e lo snippet proporrà i `#pragma mark` per raggruppare il codice in maniera ordinata

![def code snippet](https://github.com/tiknil/xcode-snippets/blob/master/images/def_code_snippet.gif)

#### `com`... ####

Questo gruppo di snippet (`comblank`, `comfull`, `comparam` e `comreturn`) sono tutti relativi ai commenti delle dichiarazioni dei metodi (e non solo).
Essi predispongono i caratteri che servono a far identificare i commenti all'IDE ma con anche i campi `@param` e `@return` con i relativi *placeholder* in modo tale da velocizzare l'inserimento e guidarlo nella maniera corretta

![com code snippets](https://github.com/tiknil/xcode-snippets/blob/master/images/com_code_snippet.gif)

