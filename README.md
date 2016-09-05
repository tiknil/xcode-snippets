# Xcode snippets

Snippets di codice Obj-C e Swift per lo sviluppo iOS e OSX utili per migliorare il tuo lavoro in termini di velocità ma anche di qualità del codice. (Vedi [Obj-C Style Guide by Tiknil](https://github.com/tiknil/objective-c-style-guide) e [Swift Style Guide di Tiknil](https://github.com/tiknil/swift-style-guide))

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

Questo snippet è molto comodo per organizzare il codice di implementazione delle classi in modo coerente. Basta cominciare a digitare `def` e lo snippet proporrà i `#pragma mark` per raggruppare il codice in maniera ordinata

**Obj-C** 

![def code snippet](https://github.com/tiknil/xcode-snippets/blob/master/images/def_code_snippet.gif)

**Swift**

![def code snippet swift](https://github.com/tiknil/xcode-snippets/blob/master/images/def_code_snippet_swift.gif)

#### `com`... ####

Questo gruppo di snippet (`comblank`, `comfull`, `comparam` e `comreturn`) sono tutti relativi ai commenti delle dichiarazioni dei metodi (e non solo).
Essi predispongono i caratteri che servono a far identificare i commenti all'IDE ma con anche i campi `@param`/`- Parameter :` e `@return`/`- Returns:` con i relativi *placeholder* in modo tale da velocizzare l'inserimento e guidarlo nella maniera corretta

**Obj-C**

![com code snippets](https://github.com/tiknil/xcode-snippets/blob/master/images/com_code_snippet.gif)

**Swift**

![com code snippets swift](https://github.com/tiknil/xcode-snippets/blob/master/images/com_code_snippet_swift.gif)


#### `ws` e `ss` ####

Per utilizzare `self` all'interno dei blocchi è utilissimo utilizzare la libreria [libextobjc](https://github.com/jspahrsummers/libextobjc) by @jspahrsummers che mette a disposizione due direttive al compilatore, `@weakify(self)` e `@strongify(self)`, da utilizzare rispettivamente prima del blocco e dentro il blocco per non incorrere a problemi dovuti al retain cycle dell'oggetto. 

Anche per questo abbiamo creato due snippet (dato che queste direttive non vengono autocompletate da Xcode): 

![ws_ss_snippets](https://github.com/tiknil/xcode-snippets/blob/master/images/ws_ss_snippet.gif)

#### `logm` ####

Snippet utile per eseguire il log del nome della classe e del metodo per semplificare il debug. 

![logm_snippet](https://github.com/tiknil/xcode-snippets/blob/master/images/logm_snippet.gif)

#### `strf` ####

Snippet utile per implementare il blocco `[NSString stringWithFormat:@"...",....]` per velocizzare la stesura di codice ripetitivo. 

![strf_snippet](https://github.com/tiknil/xcode-snippets/blob/master/images/strf_snippet.gif)


#### `pragma` #####

Snippet utile per velocizzare la scrittura dei `#pragma mark`. Di per sé da quando usiamo `def` come snippet, questo non viene più utilizzato :wink:

![pragma_snippet](https://github.com/tiknil/xcode-snippets/blob/master/images/pragma_snippets.gif)


#### `cnst_v` e `cnst_v` #####

Snippet utili per velocizzare la scrittura delle AutoLayout constraints.

`cnst_v` predispone l'inserimento di constraints nella view parent utilizzando il [Visual Format Language](https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/AutolayoutPG/VisualFormatLanguage.html)

![cnst_v_snippet](https://github.com/tiknil/xcode-snippets/blob/master/images/cnst_v.gif)

`cnst_d` predispone l'inserimento di una constraint normale nella view parent.

![cnst_d_snippet](https://github.com/tiknil/xcode-snippets/blob/master/images/cnst_d.gif)
