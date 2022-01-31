# Xcode snippets

Snippets di codice Obj-C e Swift per lo sviluppo iOS e OSX utili per migliorare il tuo lavoro in termini di velocità ma anche di qualità del codice. (Vedi la [Swift Style Guide di Tiknil](https://github.com/tiknil/swift-style-guide))

## Come tenerli aggiornati su XCode? ##

#### Link simbolico e repo locale ####

Pullare il repo e impostare i riferimenti simbolici alla cartella corretta, in questo modo: 
 * Pullare il presente repository (o meglio una vostra fork + pull, così potrete fare delle pull request se avrete snippets interessanti!) in una vostra cartella (da ora `$XCODE_SNIPPETS_FOLDER`)
 * Fare una copia di backup del contenuto della cartella `~/Library/Developer/Xcode/UserData/CodeSnippets` sul vostro mac: sono tutti i vostri snippets creati finora, se è vuota, meglio così!
 * Eliminate la cartella
 * Da Terminale eseguite il comando 

`ln -s $XCODE_SNIPPETS_FOLDER/snippets ~/Library/Developer/Xcode/UserData/CodeSnippets` 

   così da creare un link simbolico tra il vostro repo e la cartella dove XCode si aspetta di trovare i vostri snippets
 * Potete anche copiare nella cartella del repo gli snippets di cui avete fatto il backup
 * Chiudete e riaprite XCode e i vostri snippets dovrebbero trovarsi già lì

## Snippets ##

#### `def` ####

Questo snippet è molto comodo per organizzare il codice di implementazione delle classi in modo coerente. Basta cominciare a digitare `def` e lo snippet proporrà i `// MARK: ` per raggruppare il codice in maniera ordinata

![def code snippet swift](https://github.com/tiknil/xcode-snippets/blob/master/images/def_code_snippet_swift.gif)

#### `com`... ####

Questo gruppo di snippet (`comblank`, `comfull`, `comparam` e `comreturn`) sono tutti relativi ai commenti delle dichiarazioni dei metodi (e non solo).
Essi predispongono i caratteri che servono a far identificare i commenti all'IDE ma con anche i campi `@param`/`- Parameter :` e `@return`/`- Returns:` con i relativi *placeholder* in modo tale da velocizzare l'inserimento e guidarlo nella maniera corretta

![com code snippets swift](https://github.com/tiknil/xcode-snippets/blob/master/images/com_code_snippet_swift.gif)


#### `wea` e `guardself` ####

Per utilizzare `self` all'interno dei blocchi è utile usare gli snippet `wea` (che genera il codice `[weak self]`) e `guardself` (che genera il codice `guard let self = self else { return }`) da utilizzare all'inizio dei blocchi per non incorrere a leak dell'istanza stessa. 

![wea_guardself_snippets](https://github.com/tiknil/xcode-snippets/blob/master/images/wea_guardself_snippet.gif)


### Rx snippet ###

#### `obse` ####

Questo snippet crea il codice necessario per costruire un observable con tanto di gestione dei potenziali leak dell'istanza 

![obse_snippets](https://github.com/tiknil/xcode-snippets/blob/master/images/obse_snippet.gif)

#### `guardselfrx` ####

Questo snippet è un'evoluzione dei precedenti in quanto viene usato all'interno delle funzioni che creano un Completable, Single o Maybe.

![guardselfrx_snippets](https://github.com/tiknil/xcode-snippets/blob/master/images/guardselfrx_snippet.gif)


### MVVM Tiknil pattern snippet ###

#### `vc` ####

Questo snippet crea il boilerplate di un viewcontroller adeguato per il pattern mvvm Tiknil, con i placeholder dove inserire il nome della view che si sta realizzando

![vc_snippets](https://github.com/tiknil/xcode-snippets/blob/master/images/vc_snippet.gif)


#### `vm` ####

Questo snippet crea il boilerplate di un viewmodel adeguato per il pattern mvvm Tiknil, con i placeholder dove inserire il nome del viewmodel che si sta realizzando

![vm_snippets](https://github.com/tiknil/xcode-snippets/blob/master/images/vm_snippet.gif)







