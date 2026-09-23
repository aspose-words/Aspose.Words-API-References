---
title: "FindReplaceOptions"
linktitle: "FindReplaceOptions"
second_title: "Aspose.Words per Java"
description: "Specifica le opzioni per le operazioni di ricerca/sostituzione in Java."
type: docs
weight: 314
url: /it/java/com.aspose.words/findreplaceoptions/
---

**Inheritance:**
java.lang.Object
```
public class FindReplaceOptions
```

Specifica le opzioni per le operazioni di ricerca/sostituzione.

Per saperne di più, visita l'articolo di documentazione [ Find and Replace ][Find and Replace] .

 **Examples:** 

Mostra come attivare/disattivare la distinzione tra maiuscole e minuscole durante un'operazione di ricerca e sostituzione.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Ruby bought a ruby necklace.");

 // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
 FindReplaceOptions options = new FindReplaceOptions();

 // Set the "MatchCase" flag to "true" to apply case sensitivity while finding strings to replace.
 // Set the "MatchCase" flag to "false" to ignore character case while searching for text to replace.
 options.setMatchCase(matchCase);

 doc.getRange().replace("Ruby", "Jade", options);

 Assert.assertEquals(matchCase ? "Jade bought a ruby necklace." : "Jade bought a Jade necklace.",
         doc.getText().trim());
 
```

Mostra come attivare/disattivare le operazioni di ricerca e sostituzione che riguardano solo parole isolate.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Jackson will meet you in Jacksonville.");

 // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
 FindReplaceOptions options = new FindReplaceOptions();

 // Set the "FindWholeWordsOnly" flag to "true" to replace the found text if it is not a part of another word.
 // Set the "FindWholeWordsOnly" flag to "false" to replace all text regardless of its surroundings.
 options.setFindWholeWordsOnly(findWholeWordsOnly);

 doc.getRange().replace("Jackson", "Louis", options);

 Assert.assertEquals(
         findWholeWordsOnly ? "Louis will meet you in Jacksonville." : "Louis will meet you in Louisville.",
         doc.getText().trim());
 
```


[Find and Replace]: https://docs.aspose.com/words/java/find-and-replace/
## Costruttori

| Costruttore | Descrizione |
| --- | --- |
| [FindReplaceOptions()](#FindReplaceOptions) | Inizializza una nuova istanza della classe FindReplaceOptions con le impostazioni predefinite. |
| [FindReplaceOptions(int direction)](#FindReplaceOptions-int) | Inizializza una nuova istanza di questa classe. |
| [FindReplaceOptions(IReplacingCallback replacingCallback)](#FindReplaceOptions-com.aspose.words.IReplacingCallback) | Inizializza una nuova istanza della classe FindReplaceOptions con la callback di sostituzione specificata. |
| [FindReplaceOptions(int direction, IReplacingCallback replacingCallback)](#FindReplaceOptions-int-com.aspose.words.IReplacingCallback) | Inizializza una nuova istanza di questa classe. |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getApplyFont()](#getApplyFont) | Formattazione del testo applicata al nuovo contenuto. |
| [getApplyParagraphFormat()](#getApplyParagraphFormat) | Formattazione del paragrafo applicata al nuovo contenuto. |
| [getDirection()](#getDirection) | Seleziona la direzione per la sostituzione. |
| [getFindWholeWordsOnly()](#getFindWholeWordsOnly) | True indica che oldValue deve essere una parola isolata. |
| [getIgnoreDeleted()](#getIgnoreDeleted) | Restituisce un valore booleano che indica se ignorare il testo all'interno delle revisioni di cancellazione. |
| [getIgnoreFieldCodes()](#getIgnoreFieldCodes) | Restituisce un valore booleano che indica se ignorare il testo all'interno dei codici di campo. |
| [getIgnoreFields()](#getIgnoreFields) | Restituisce un valore booleano che indica se ignorare il testo all'interno dei campi. |
| [getIgnoreFootnotes()](#getIgnoreFootnotes) | Restituisce un valore booleano che indica se ignorare le note a piè di pagina. |
| [getIgnoreInserted()](#getIgnoreInserted) | Ottiene un valore booleano che indica se ignorare il testo all'interno delle revisioni di inserimento. |
| [getIgnoreOfficeMath()](#getIgnoreOfficeMath) | Ottiene un valore booleano che indica se ignorare il testo all'interno di OfficeMath/>. |
| [getIgnoreShapes()](#getIgnoreShapes) | Ottiene o imposta un valore booleano che indica se ignorare le forme all'interno di un testo. |
| [getIgnoreStructuredDocumentTags()](#getIgnoreStructuredDocumentTags) | Ottiene un valore booleano che indica se ignorare il contenuto di [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/). |
| [getLegacyMode()](#getLegacyMode) | Ottiene un valore booleano che indica che viene utilizzato il vecchio algoritmo di ricerca/sostituzione. |
| [getMatchCase()](#getMatchCase) | True indica un confronto sensibile al maiuscolo/minuscolo, false indica un confronto insensibile al maiuscolo/minuscolo. |
| [getReplacementFormat()](#getReplacementFormat) | Specifica il formato della sostituzione. |
| [getReplacingCallback()](#getReplacingCallback) | Il metodo definito dall'utente che viene chiamato prima di ogni occorrenza di sostituzione. |
| [getSmartParagraphBreakReplacement()](#getSmartParagraphBreakReplacement) | Ottiene o imposta un valore booleano che indica se è consentito sostituire l'interruzione di paragrafo quando non esiste un paragrafo fratello successivo. |
| [getUseLegacyOrder()](#getUseLegacyOrder) | True indica che una ricerca di testo viene eseguita sequenzialmente dall'alto verso il basso considerando le caselle di testo. |
| [getUseSubstitutions()](#getUseSubstitutions) | Ottiene un valore booleano che indica se riconoscere e utilizzare le sostituzioni nei modelli di sostituzione. |
| [setDirection(int value)](#setDirection-int) | Seleziona la direzione per la sostituzione. |
| [setFindWholeWordsOnly(boolean value)](#setFindWholeWordsOnly-boolean) | True indica che oldValue deve essere una parola isolata. |
| [setIgnoreDeleted(boolean value)](#setIgnoreDeleted-boolean) | Imposta un valore booleano che indica se ignorare il testo all'interno delle revisioni di eliminazione. |
| [setIgnoreFieldCodes(boolean value)](#setIgnoreFieldCodes-boolean) | Imposta un valore booleano che indica se ignorare il testo all'interno dei codici di campo. |
| [setIgnoreFields(boolean value)](#setIgnoreFields-boolean) | Imposta un valore booleano che indica se ignorare il testo all'interno dei campi. |
| [setIgnoreFootnotes(boolean value)](#setIgnoreFootnotes-boolean) | Imposta un valore booleano che indica se ignorare le note a piè di pagina. |
| [setIgnoreInserted(boolean value)](#setIgnoreInserted-boolean) | Imposta un valore booleano che indica se ignorare il testo all'interno delle revisioni di inserimento. |
| [setIgnoreOfficeMath(boolean value)](#setIgnoreOfficeMath-boolean) | Imposta un valore booleano che indica se ignorare il testo all'interno di OfficeMath/>. |
| [setIgnoreShapes(boolean value)](#setIgnoreShapes-boolean) | Ottiene o imposta un valore booleano che indica se ignorare le forme all'interno di un testo. |
| [setIgnoreStructuredDocumentTags(boolean value)](#setIgnoreStructuredDocumentTags-boolean) | Imposta un valore booleano che indica se ignorare il contenuto di [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/). |
| [setLegacyMode(boolean value)](#setLegacyMode-boolean) | Imposta un valore booleano che indica che viene utilizzato il vecchio algoritmo di ricerca/sostituzione. |
| [setMatchCase(boolean value)](#setMatchCase-boolean) | True indica un confronto sensibile al maiuscolo/minuscolo, false indica un confronto insensibile al maiuscolo/minuscolo. |
| [setReplacementFormat(int value)](#setReplacementFormat-int) | Specifica il formato della sostituzione. |
| [setReplacingCallback(IReplacingCallback value)](#setReplacingCallback-com.aspose.words.IReplacingCallback) | Il metodo definito dall'utente che viene chiamato prima di ogni occorrenza di sostituzione. |
| [setSmartParagraphBreakReplacement(boolean value)](#setSmartParagraphBreakReplacement-boolean) | Ottiene o imposta un valore booleano che indica se è consentito sostituire l'interruzione di paragrafo quando non esiste un paragrafo fratello successivo. |
| [setUseLegacyOrder(boolean value)](#setUseLegacyOrder-boolean) | True indica che una ricerca di testo viene eseguita sequenzialmente dall'alto verso il basso considerando le caselle di testo. |
| [setUseSubstitutions(boolean value)](#setUseSubstitutions-boolean) | Imposta un valore booleano che indica se riconoscere e utilizzare le sostituzioni nei modelli di sostituzione. |
### FindReplaceOptions() {#FindReplaceOptions}
```
public FindReplaceOptions()
```


Inizializza una nuova istanza della classe FindReplaceOptions con le impostazioni predefinite.

 **Examples:** 

Mostra come riconoscere e utilizzare le sostituzioni nei modelli di sostituzione.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("Jason gave money to Paul.");

 String regex = "([A-z]+) gave money to ([A-z]+)";

 FindReplaceOptions options = new FindReplaceOptions();
 options.setUseSubstitutions(true);

 // Using legacy mode does not support many advanced features, so we need to set it to 'false'.
 options.setLegacyMode(false);

 doc.getRange().replace(Pattern.compile(regex), "$2 took money from $1", options);

 Assert.assertEquals(doc.getText(), "Paul took money from Jason.\f");
 
```

### FindReplaceOptions(int direction) {#FindReplaceOptions-int}
```
public FindReplaceOptions(int direction)
```


Inizializza una nuova istanza di questa classe.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| direction | int |  |

### FindReplaceOptions(IReplacingCallback replacingCallback) {#FindReplaceOptions-com.aspose.words.IReplacingCallback}
```
public FindReplaceOptions(IReplacingCallback replacingCallback)
```


Inizializza una nuova istanza della classe FindReplaceOptions con la callback di sostituzione specificata.

 **Examples:** 

Mostra come tracciare l'ordine in cui un'operazione di sostituzione del testo attraversa i nodi.

```

 public void order(boolean differentFirstPageHeaderFooter) throws Exception {
     Document doc = new Document(getMyDir() + "Header and footer types.docx");

     Section firstPageSection = doc.getFirstSection();

     ReplaceLog logger = new ReplaceLog();
     FindReplaceOptions options = new FindReplaceOptions();
     {
         options.setReplacingCallback(logger);
     }

     // Using a different header/footer for the first page will affect the search order.
     firstPageSection.getPageSetup().setDifferentFirstPageHeaderFooter(differentFirstPageHeaderFooter);
     doc.getRange().replace(Pattern.compile("(header|footer)"), "", options);

     if (differentFirstPageHeaderFooter)
         Assert.assertEquals("First headerFirst footerSecond headerSecond footerThird headerThird footer",
                 logger.Text().replace("\r", ""));
     else
         Assert.assertEquals("Third headerFirst headerThird footerFirst footerSecond headerSecond footer",
                 logger.Text().replace("\r", ""));
 }

 public static Object[][] orderDataProvider() throws Exception {
     return new Object[][]
             {
                     {false},
                     {true},
             };
 }

 /// 
 /// During a find-and-replace operation, records the contents of every node that has text that the operation 'finds',
 /// in the state it is in before the replacement takes place.
 /// This will display the order in which the text replacement operation traverses nodes.
 /// 
 private static class ReplaceLog implements IReplacingCallback {
     public int replacing(ReplacingArgs args) {
         mTextBuilder.append(args.getMatchNode().getText());
         return ReplaceAction.SKIP;
     }

     public String Text() {
         return mTextBuilder.toString();
     }

     private final StringBuilder mTextBuilder = new StringBuilder();
 }
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| replacingCallback | [IReplacingCallback](../../com.aspose.words/ireplacingcallback/) | Il callback da utilizzare per sostituire il testo trovato. |

### FindReplaceOptions(int direction, IReplacingCallback replacingCallback) {#FindReplaceOptions-int-com.aspose.words.IReplacingCallback}
```
public FindReplaceOptions(int direction, IReplacingCallback replacingCallback)
```


Inizializza una nuova istanza di questa classe.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| direction | int |  |
| replacingCallback | [IReplacingCallback](../../com.aspose.words/ireplacingcallback/) |  |

### getApplyFont() {#getApplyFont}
```
public Font getApplyFont()
```


Formattazione del testo applicata al nuovo contenuto.

 **Examples:** 

Mostra come applicare un carattere diverso al nuovo contenuto tramite FindReplaceOptions.

```

 public void convertNumbersToHexadecimal() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.getFont().setName("Arial");
     builder.writeln("Numbers that the find-and-replace operation will convert to hexadecimal and highlight:\n" +
             "123, 456, 789 and 17379.");

     // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
     FindReplaceOptions options = new FindReplaceOptions();

     // Set the "HighlightColor" property to a background color that we want to apply to the operation's resulting text.
     options.getApplyFont().setHighlightColor(Color.GRAY);

     NumberHexer numberHexer = new NumberHexer();
     options.setReplacingCallback(numberHexer);

     int replacementCount = doc.getRange().replace(Pattern.compile("[0-9]+"), "", options);

     System.out.println(numberHexer.getLog());

     Assert.assertEquals(4, replacementCount);
     Assert.assertEquals("Numbers that the find-and-replace operation will convert to hexadecimal and highlight:\r" +
             "0x123, 0x456, 0x789 and 0x17,379.", doc.getText().trim());
 }

 /// 
 /// Replaces numeric find-and-replacement matches with their hexadecimal equivalents.
 /// Maintains a log of every replacement.
 /// 
 private static class NumberHexer implements IReplacingCallback {
     public int replacing(ReplacingArgs args) {
         mCurrentReplacementNumber++;

         int number = Integer.parseInt(args.getMatch().group(0));

         args.setReplacement(MessageFormat.format("0x{0}", number));

         mLog.append(MessageFormat.format("Match #{0}", mCurrentReplacementNumber));
         mLog.append(MessageFormat.format("\tOriginal value:\t{0}", args.getMatch().group(0)));
         mLog.append(MessageFormat.format("\tReplacement:\t{0}", args.getReplacement()));
         mLog.append(MessageFormat.format("\tOffset in parent {0} node:\t{1}", args.getMatchNode().getNodeType(), args.getMatchOffset()));

         return ReplaceAction.REPLACE;
     }

     public String getLog() {
         return mLog.toString();
     }

     private int mCurrentReplacementNumber;
     private final StringBuilder mLog = new StringBuilder();
 }
 
```

**Returns:**
[Font](../../com.aspose.words/font/) - The corresponding [Font](../../com.aspose.words/font/) value.
### getApplyParagraphFormat() {#getApplyParagraphFormat}
```
public ParagraphFormat getApplyParagraphFormat()
```


Formattazione del paragrafo applicata al nuovo contenuto.

 **Examples:** 

Mostra come aggiungere formattazione ai paragrafi in cui un'operazione di ricerca e sostituzione ha trovato corrispondenze.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Every paragraph that ends with a full stop like this one will be right aligned.");
 builder.writeln("This one will not!");
 builder.write("This one also will.");

 ParagraphCollection paragraphs = doc.getFirstSection().getBody().getParagraphs();

 Assert.assertEquals(ParagraphAlignment.LEFT, paragraphs.get(0).getParagraphFormat().getAlignment());
 Assert.assertEquals(ParagraphAlignment.LEFT, paragraphs.get(1).getParagraphFormat().getAlignment());
 Assert.assertEquals(ParagraphAlignment.LEFT, paragraphs.get(2).getParagraphFormat().getAlignment());

 // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
 FindReplaceOptions options = new FindReplaceOptions();

 // Set the "Alignment" property to "ParagraphAlignment.Right" to right-align every paragraph
 // that contains a match that the find-and-replace operation finds.
 options.getApplyParagraphFormat().setAlignment(ParagraphAlignment.RIGHT);

 // Replace every full stop that is right before a paragraph break with an exclamation point.
 int count = doc.getRange().replace(".&p", "!&p", options);

 Assert.assertEquals(2, count);
 Assert.assertEquals(ParagraphAlignment.RIGHT, paragraphs.get(0).getParagraphFormat().getAlignment());
 Assert.assertEquals(ParagraphAlignment.LEFT, paragraphs.get(1).getParagraphFormat().getAlignment());
 Assert.assertEquals(ParagraphAlignment.RIGHT, paragraphs.get(2).getParagraphFormat().getAlignment());
 Assert.assertEquals("Every paragraph that ends with a full stop like this one will be right aligned!\r" +
         "This one will not!\r" +
         "This one also will!", doc.getText().trim());
 
```

**Returns:**
[ParagraphFormat](../../com.aspose.words/paragraphformat/) - The corresponding [ParagraphFormat](../../com.aspose.words/paragraphformat/) value.
### getDirection() {#getDirection}
```
public int getDirection()
```


Seleziona la direzione per la sostituzione. Il valore predefinito è [FindReplaceDirection.FORWARD](../../com.aspose.words/findreplacedirection/\#FORWARD).

 **Examples:** 

Mostra come determinare in quale direzione un'operazione di ricerca e sostituzione attraversa il documento.

```

 public void direction(int findReplaceDirection) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Insert three runs which we can search for using a regex pattern.
     // Place one of those runs inside a text box.
     builder.writeln("Match 1.");
     builder.writeln("Match 2.");
     builder.writeln("Match 3.");
     builder.writeln("Match 4.");

     // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
     FindReplaceOptions options = new FindReplaceOptions();

     // Assign a custom callback to the "ReplacingCallback" property.
     TextReplacementRecorder callback = new TextReplacementRecorder();
     options.setReplacingCallback(callback);

     // Set the "Direction" property to "FindReplaceDirection.Backward" to get the find-and-replace
     // operation to start from the end of the range, and traverse back to the beginning.
     // Set the "Direction" property to "FindReplaceDirection.Forward" to get the find-and-replace
     // operation to start from the beginning of the range, and traverse to the end.
     options.setDirection(findReplaceDirection);

     doc.getRange().replace(Pattern.compile("Match \\d*"), "Replacement", options);

     Assert.assertEquals("Replacement.\r" +
             "Replacement.\r" +
             "Replacement.\r" +
             "Replacement.", doc.getText().trim());

     switch (findReplaceDirection) {
         case FindReplaceDirection.FORWARD:
             Assert.assertEquals(new String[]{"Match 1", "Match 2", "Match 3", "Match 4"}, callback.getMatches().toArray());
             break;
         case FindReplaceDirection.BACKWARD:
             Assert.assertEquals(new String[]{"Match 4", "Match 3", "Match 2", "Match 1"}, callback.getMatches().toArray());
             break;
     }
 }

 public static Object[][] directionDataProvider() {
     return new Object[][]
             {
                     {FindReplaceDirection.BACKWARD},
                     {FindReplaceDirection.FORWARD},
             };
 }

 /// 
 /// Records all matches that occur during a find-and-replace operation in the order that they take place.
 /// 
 private static class TextReplacementRecorder implements IReplacingCallback {
     public int replacing(ReplacingArgs e) {
         mMatches.add(e.getMatch().group(0));
         return ReplaceAction.REPLACE;
     }

     public ArrayList getMatches() {
         return mMatches;
     }
     private ArrayList mMatches = new ArrayList<>();
 }
 
```

**Returns:**
int - Il valore int corrispondente. Il valore restituito è una delle costanti [FindReplaceDirection](../../com.aspose.words/findreplacedirection/).
### getFindWholeWordsOnly() {#getFindWholeWordsOnly}
```
public boolean getFindWholeWordsOnly()
```


True indica che oldValue deve essere una parola isolata.

 **Examples:** 

Mostra come attivare/disattivare le operazioni di ricerca e sostituzione che riguardano solo parole isolate.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Jackson will meet you in Jacksonville.");

 // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
 FindReplaceOptions options = new FindReplaceOptions();

 // Set the "FindWholeWordsOnly" flag to "true" to replace the found text if it is not a part of another word.
 // Set the "FindWholeWordsOnly" flag to "false" to replace all text regardless of its surroundings.
 options.setFindWholeWordsOnly(findWholeWordsOnly);

 doc.getRange().replace("Jackson", "Louis", options);

 Assert.assertEquals(
         findWholeWordsOnly ? "Louis will meet you in Jacksonville." : "Louis will meet you in Louisville.",
         doc.getText().trim());
 
```

**Returns:**
boolean - Il valore booleano corrispondente.
### getIgnoreDeleted() {#getIgnoreDeleted}
```
public boolean getIgnoreDeleted()
```


Restituisce un valore booleano che indica se ignorare il testo all'interno delle revisioni di eliminazione. Il valore predefinito è false.

 **Examples:** 

Mostra come includere o ignorare il testo all'interno delle revisioni di eliminazione durante un'operazione di ricerca e sostituzione.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");
 builder.writeln("Hello again!");

 // Start tracking revisions and remove the second paragraph, which will create a delete revision.
 // That paragraph will persist in the document until we accept the delete revision.
 doc.startTrackRevisions("John Doe", new Date());
 doc.getFirstSection().getBody().getParagraphs().get(1).remove();
 doc.stopTrackRevisions();

 Assert.assertTrue(doc.getFirstSection().getBody().getParagraphs().get(1).isDeleteRevision());

 // We can use a "FindReplaceOptions" object to modify the find and replace process.
 FindReplaceOptions options = new FindReplaceOptions();

 // Set the "IgnoreDeleted" flag to "true" to get the find-and-replace
 // operation to ignore paragraphs that are delete revisions.
 // Set the "IgnoreDeleted" flag to "false" to get the find-and-replace
 // operation to also search for text inside delete revisions.
 options.setIgnoreDeleted(ignoreTextInsideDeleteRevisions);

 doc.getRange().replace("Hello", "Greetings", options);

 Assert.assertEquals(
         ignoreTextInsideDeleteRevisions
                 ? "Greetings world!\rHello again!"
                 : "Greetings world!\rGreetings again!", doc.getText().trim());
 
```

**Returns:**
boolean - Un valore booleano che indica se ignorare il testo all'interno delle revisioni di eliminazione.
### getIgnoreFieldCodes() {#getIgnoreFieldCodes}
```
public boolean getIgnoreFieldCodes()
```


Restituisce un valore booleano che indica se ignorare il testo all'interno dei codici di campo. Il valore predefinito è false.

 **Remarks:** 

Questa opzione influisce solo sui codici di campo (non ignora i nodi tra [NodeType.FIELD\_SEPARATOR](../../com.aspose.words/nodetype/\#FIELD-SEPARATOR) e [NodeType.FIELD\_END](../../com.aspose.words/nodetype/\#FIELD-END)).

Per ignorare l'intero campo, si prega di utilizzare l'opzione corrispondente [getIgnoreFields()](../../com.aspose.words/findreplaceoptions/\#getIgnoreFields) / [setIgnoreFields(boolean)](../../com.aspose.words/findreplaceoptions/\#setIgnoreFields-boolean).

 **Examples:** 

Mostra come ignorare il testo all'interno dei codici di campo.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.insertField("INCLUDETEXT", "Test IT!");

 FindReplaceOptions options = new FindReplaceOptions(); {options.setIgnoreFieldCodes(ignoreFieldCodes);}

 // Replace 'T' in document ignoring text inside field code or not.
 doc.getRange().replace(Pattern.compile("T"), "*", options);
 System.out.println(doc.getText());

 Assert.assertEquals(
         ignoreFieldCodes
                 ? "INCLUDETEXT*est I*!"
                 : "INCLUDE*EX**est I*!", doc.getText().trim());
 
```

**Returns:**
boolean - Un valore booleano che indica se ignorare il testo all'interno dei codici di campo.
### getIgnoreFields() {#getIgnoreFields}
```
public boolean getIgnoreFields()
```


Restituisce un valore booleano che indica se ignorare il testo all'interno dei campi. Il valore predefinito è false.

 **Remarks:** 

Questa opzione influisce sull'intero campo (tutti i nodi tra [NodeType.FIELD\_START](../../com.aspose.words/nodetype/\#FIELD-START) e [NodeType.FIELD\_END](../../com.aspose.words/nodetype/\#FIELD-END)).

Per ignorare solo i codici di campo, si prega di utilizzare l'opzione corrispondente [getIgnoreFieldCodes()](../../com.aspose.words/findreplaceoptions/\#getIgnoreFieldCodes) / [setIgnoreFieldCodes(boolean)](../../com.aspose.words/findreplaceoptions/\#setIgnoreFieldCodes-boolean).

 **Examples:** 

Mostra come ignorare il testo all'interno dei campi.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");
 builder.insertField("QUOTE", "Hello again!");

 // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
 FindReplaceOptions options = new FindReplaceOptions();

 // Set the "IgnoreFields" flag to "true" to get the find-and-replace
 // operation to ignore text inside fields.
 // Set the "IgnoreFields" flag to "false" to get the find-and-replace
 // operation to also search for text inside fields.
 options.setIgnoreFields(ignoreTextInsideFields);

 doc.getRange().replace("Hello", "Greetings", options);

 Assert.assertEquals(
         ignoreTextInsideFields
                 ? "Greetings world!\rQUOTEHello again!"
                 : "Greetings world!\rQUOTEGreetings again!", doc.getText().trim());
 
```

**Returns:**
boolean - Un valore booleano che indica se ignorare il testo all'interno dei campi.
### getIgnoreFootnotes() {#getIgnoreFootnotes}
```
public boolean getIgnoreFootnotes()
```


Restituisce un valore booleano che indica se ignorare le note a piè di pagina. Il valore predefinito è false.

 **Examples:** 

Mostra come ignorare le note a piè di pagina durante un'operazione di ricerca e sostituzione.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

 builder.insertParagraph();

 builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

 // Set the "IgnoreFootnotes" flag to "true" to get the find-and-replace
 // operation to ignore text inside footnotes.
 // Set the "IgnoreFootnotes" flag to "false" to get the find-and-replace
 // operation to also search for text inside footnotes.
 FindReplaceOptions options = new FindReplaceOptions();
 {
     options.setIgnoreFootnotes(isIgnoreFootnotes);
 }
 doc.getRange().replace("Lorem ipsum", "Replaced Lorem ipsum", options);
 
```

**Returns:**
boolean - Un valore booleano che indica se ignorare le note a piè di pagina.
### getIgnoreInserted() {#getIgnoreInserted}
```
public boolean getIgnoreInserted()
```


Restituisce un valore booleano che indica se ignorare il testo all'interno delle revisioni di inserimento. Il valore predefinito è false.

 **Examples:** 

Mostra come includere o ignorare il testo all'interno delle revisioni di inserimento durante un'operazione di ricerca e sostituzione.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");

 // Start tracking revisions and insert a paragraph. That paragraph will be an insert revision.
 doc.startTrackRevisions("John Doe", new Date());
 builder.writeln("Hello again!");
 doc.stopTrackRevisions();

 Assert.assertTrue(doc.getFirstSection().getBody().getParagraphs().get(1).isInsertRevision());

 // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
 FindReplaceOptions options = new FindReplaceOptions();

 // Set the "IgnoreInserted" flag to "true" to get the find-and-replace
 // operation to ignore paragraphs that are insert revisions.
 // Set the "IgnoreInserted" flag to "false" to get the find-and-replace
 // operation to also search for text inside insert revisions.
 options.setIgnoreInserted(ignoreTextInsideInsertRevisions);

 doc.getRange().replace("Hello", "Greetings", options);

 Assert.assertEquals(
         ignoreTextInsideInsertRevisions
                 ? "Greetings world!\rHello again!"
                 : "Greetings world!\rGreetings again!", doc.getText().trim());
 
```

**Returns:**
boolean - Un valore booleano che indica se ignorare il testo all'interno delle revisioni di inserimento.
### getIgnoreOfficeMath() {#getIgnoreOfficeMath}
```
public boolean getIgnoreOfficeMath()
```


Restituisce un valore booleano che indica se ignorare il testo all'interno di OfficeMath/>. Il valore predefinito è true.

 **Examples:** 

Mostra come trovare e sostituire il testo all'interno di OfficeMath.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 Assert.assertEquals("i+b-c\u2265iM+bM-cM", doc.getFirstSection().getBody().getFirstParagraph().getText().trim());

 FindReplaceOptions options = new FindReplaceOptions();
 options.setIgnoreOfficeMath(isIgnoreOfficeMath);
 doc.getRange().replace("b", "x", options);

 if (isIgnoreOfficeMath)
     Assert.assertEquals("i+b-c\u2265iM+bM-cM", doc.getFirstSection().getBody().getFirstParagraph().getText().trim());
 else
     Assert.assertEquals("i+x-c\u2265iM+xM-cM", doc.getFirstSection().getBody().getFirstParagraph().getText().trim());
 
```

**Returns:**
boolean - Un valore booleano che indica se ignorare il testo all'interno di OfficeMath/>.
### getIgnoreShapes() {#getIgnoreShapes}
```
public boolean getIgnoreShapes()
```


Ottiene o imposta un valore booleano che indica se ignorare le forme all'interno di un testo.

Il valore predefinito è  false .

 **Examples:** 

Mostra come ignorare le forme durante la sostituzione del testo.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
 builder.insertShape(ShapeType.BALLOON, 200.0, 200.0);
 builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

 FindReplaceOptions findReplaceOptions = new FindReplaceOptions(); { findReplaceOptions.setIgnoreShapes(true); }
 builder.getDocument().getRange().replace("Lorem ipsum dolor sit amet, consectetur adipiscing elit.Lorem ipsum dolor sit amet, consectetur adipiscing elit.",
     "Lorem ipsum dolor sit amet, consectetur adipiscing elit.", findReplaceOptions);
 Assert.assertEquals("Lorem ipsum dolor sit amet, consectetur adipiscing elit.", builder.getDocument().getText().trim());
 
```

**Returns:**
boolean - Il valore booleano corrispondente.
### getIgnoreStructuredDocumentTags() {#getIgnoreStructuredDocumentTags}
```
public boolean getIgnoreStructuredDocumentTags()
```


Restituisce un valore booleano che indica se ignorare il contenuto di [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/). Il valore predefinito è false.

 **Remarks:** 

Quando questa opzione è impostata su true, il contenuto di [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) verrà trattato come testo semplice.

Altrimenti, [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) verrà elaborato come Story autonomo e il modello di sostituzione verrà cercato separatamente per ogni [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/), in modo che se il modello attraversa un [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/), la sostituzione non verrà eseguita per tale modello.

 **Examples:** 

Mostra come ignorare il contenuto dei tag durante la sostituzione.

```

 Document doc = new Document(getMyDir() + "Structured document tags.docx");

 // This paragraph contains SDT.
 Paragraph p = (Paragraph)doc.getFirstSection().getBody().getChild(NodeType.PARAGRAPH, 2, true);
 String textToSearch = p.toString(SaveFormat.TEXT).trim();

 FindReplaceOptions options = new FindReplaceOptions();
 options.setIgnoreStructuredDocumentTags(true);
 doc.getRange().replace(textToSearch, "replacement", options);

 doc.save(getArtifactsDir() + "StructuredDocumentTag.IgnoreStructuredDocumentTags.docx");
 
```

**Returns:**
boolean - Un valore booleano che indica se ignorare il contenuto di [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/).
### getLegacyMode() {#getLegacyMode}
```
public boolean getLegacyMode()
```


Ottiene un valore booleano che indica che viene utilizzato il vecchio algoritmo di ricerca/sostituzione.

 **Remarks:** 

Utilizza questo flag se hai bisogno esattamente dello stesso comportamento di prima dell'introduzione della funzionalità avanzata di ricerca/sostituzione. Nota che il vecchio algoritmo non supporta funzionalità avanzate come la sostituzione con interruzioni, l'applicazione di formattazione e così via.

 **Examples:** 

Mostra come riconoscere e utilizzare le sostituzioni nei modelli di sostituzione.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("Jason gave money to Paul.");

 String regex = "([A-z]+) gave money to ([A-z]+)";

 FindReplaceOptions options = new FindReplaceOptions();
 options.setUseSubstitutions(true);

 // Using legacy mode does not support many advanced features, so we need to set it to 'false'.
 options.setLegacyMode(false);

 doc.getRange().replace(Pattern.compile(regex), "$2 took money from $1", options);

 Assert.assertEquals(doc.getText(), "Paul took money from Jason.\f");
 
```

**Returns:**
boolean - Un valore booleano che indica che viene utilizzato il vecchio algoritmo di ricerca/sostituzione.
### getMatchCase() {#getMatchCase}
```
public boolean getMatchCase()
```


True indica un confronto sensibile al maiuscolo/minuscolo, false indica un confronto insensibile al maiuscolo/minuscolo.

 **Examples:** 

Mostra come attivare/disattivare la distinzione tra maiuscole e minuscole durante un'operazione di ricerca e sostituzione.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Ruby bought a ruby necklace.");

 // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
 FindReplaceOptions options = new FindReplaceOptions();

 // Set the "MatchCase" flag to "true" to apply case sensitivity while finding strings to replace.
 // Set the "MatchCase" flag to "false" to ignore character case while searching for text to replace.
 options.setMatchCase(matchCase);

 doc.getRange().replace("Ruby", "Jade", options);

 Assert.assertEquals(matchCase ? "Jade bought a ruby necklace." : "Jade bought a Jade necklace.",
         doc.getText().trim());
 
```

**Returns:**
boolean - Il valore booleano corrispondente.
### getReplacementFormat() {#getReplacementFormat}
```
public int getReplacementFormat()
```


Specifica il formato della sostituzione. Il valore predefinito è [ReplacementFormat.TEXT](../../com.aspose.words/replacementformat/\#TEXT).

 **Remarks:** 

Ha effetto solo quando viene utilizzato in [Replacer](../../com.aspose.words/replacer/)

**Returns:**
int - Il valore int corrispondente. Il valore restituito è una delle costanti di [ReplacementFormat](../../com.aspose.words/replacementformat/).
### getReplacingCallback() {#getReplacingCallback}
```
public IReplacingCallback getReplacingCallback()
```


Il metodo definito dall'utente che viene chiamato prima di ogni occorrenza di sostituzione.

 **Examples:** 

Mostra come sostituire tutte le occorrenze di un modello di espressione regolare con un'altra stringa, tenendo traccia di tutte queste sostituzioni.

```

 public void replaceWithCallback() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.writeln("Our new location in New York City is opening tomorrow. " +
             "Hope to see all our NYC-based customers at the opening!");

     // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
     FindReplaceOptions options = new FindReplaceOptions();

     // Set a callback that tracks any replacements that the "Replace" method will make.
     TextFindAndReplacementLogger logger = new TextFindAndReplacementLogger();
     options.setReplacingCallback(logger);

     doc.getRange().replace(Pattern.compile("New York City|NYC"), "Washington", options);

     Assert.assertEquals("Our new location in (Old value:\"New York City\") Washington is opening tomorrow. " +
             "Hope to see all our (Old value:\"NYC\") Washington-based customers at the opening!", doc.getText().trim());

     Assert.assertEquals("\"New York City\" converted to \"Washington\" 20 characters into a 21 node." +
             "\"NYC\" converted to \"Washington\" 42 characters into a 21 node.", logger.getLog().trim());
 }

 /// 
 /// Maintains a log of every text replacement done by a find-and-replace operation
 /// and notes the original matched text's value.
 /// 
 private static class TextFindAndReplacementLogger implements IReplacingCallback {
     public int replacing(ReplacingArgs args) {
         mLog.append(MessageFormat.format("\"{0}\" converted to \"{1}\" {2} characters into a {3} node.", args.getMatch().group(0), args.getReplacement(), args.getMatchOffset(), args.getMatchNode().getNodeType()));

         args.setReplacement(MessageFormat.format("(Old value:\"{0}\") {1}", args.getMatch().group(0), args.getReplacement()));
         return ReplaceAction.REPLACE;
     }

     public String getLog() {
         return mLog.toString();
     }

     private final StringBuilder mLog = new StringBuilder();
 }
 
```

Mostra come applicare un carattere diverso al nuovo contenuto tramite FindReplaceOptions.

```

 public void convertNumbersToHexadecimal() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.getFont().setName("Arial");
     builder.writeln("Numbers that the find-and-replace operation will convert to hexadecimal and highlight:\n" +
             "123, 456, 789 and 17379.");

     // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
     FindReplaceOptions options = new FindReplaceOptions();

     // Set the "HighlightColor" property to a background color that we want to apply to the operation's resulting text.
     options.getApplyFont().setHighlightColor(Color.GRAY);

     NumberHexer numberHexer = new NumberHexer();
     options.setReplacingCallback(numberHexer);

     int replacementCount = doc.getRange().replace(Pattern.compile("[0-9]+"), "", options);

     System.out.println(numberHexer.getLog());

     Assert.assertEquals(4, replacementCount);
     Assert.assertEquals("Numbers that the find-and-replace operation will convert to hexadecimal and highlight:\r" +
             "0x123, 0x456, 0x789 and 0x17,379.", doc.getText().trim());
 }

 /// 
 /// Replaces numeric find-and-replacement matches with their hexadecimal equivalents.
 /// Maintains a log of every replacement.
 /// 
 private static class NumberHexer implements IReplacingCallback {
     public int replacing(ReplacingArgs args) {
         mCurrentReplacementNumber++;

         int number = Integer.parseInt(args.getMatch().group(0));

         args.setReplacement(MessageFormat.format("0x{0}", number));

         mLog.append(MessageFormat.format("Match #{0}", mCurrentReplacementNumber));
         mLog.append(MessageFormat.format("\tOriginal value:\t{0}", args.getMatch().group(0)));
         mLog.append(MessageFormat.format("\tReplacement:\t{0}", args.getReplacement()));
         mLog.append(MessageFormat.format("\tOffset in parent {0} node:\t{1}", args.getMatchNode().getNodeType(), args.getMatchOffset()));

         return ReplaceAction.REPLACE;
     }

     public String getLog() {
         return mLog.toString();
     }

     private int mCurrentReplacementNumber;
     private final StringBuilder mLog = new StringBuilder();
 }
 
```

**Returns:**
[IReplacingCallback](../../com.aspose.words/ireplacingcallback/) - The corresponding [IReplacingCallback](../../com.aspose.words/ireplacingcallback/) value.
### getSmartParagraphBreakReplacement() {#getSmartParagraphBreakReplacement}
```
public boolean getSmartParagraphBreakReplacement()
```


Ottiene o imposta un valore booleano che indica se è consentito sostituire l'interruzione di paragrafo quando non esiste un paragrafo fratello successivo.

Il valore predefinito è  false .

 **Remarks:** 

Questa opzione consente di sostituire l'interruzione di paragrafo quando non esiste un paragrafo fratello successivo a cui spostare tutti i nodi figlio, trovando qualsiasi (non necessariamente fratello) paragrafo successivo a quello che viene sostituito.

 **Examples:** 

Mostra come rimuovere un paragrafo da una cella di tabella con una tabella nidificata.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create table with paragraph and inner table in first cell.
 builder.startTable();
 builder.insertCell();
 builder.write("TEXT1");
 builder.startTable();
 builder.insertCell();
 builder.endTable();
 builder.endTable();
 builder.writeln();

 FindReplaceOptions options = new FindReplaceOptions();
 // When the following option is set to 'true', Aspose.Words will remove paragraph's text
 // completely with its paragraph mark. Otherwise, Aspose.Words will mimic Word and remove
 // only paragraph's text and leaves the paragraph mark intact (when a table follows the text).
 options.setSmartParagraphBreakReplacement(isSmartParagraphBreakReplacement);
 doc.getRange().replace("TEXT1&p", "", options);

 doc.save(getArtifactsDir() + "Table.RemoveParagraphTextAndMark.docx");
 
```

**Returns:**
boolean - Il valore booleano corrispondente.
### getUseLegacyOrder() {#getUseLegacyOrder}
```
public boolean getUseLegacyOrder()
```


True indica che la ricerca del testo viene eseguita in modo sequenziale dall'alto verso il basso considerando le caselle di testo. Il valore predefinito è false.

 **Examples:** 

Mostra come modificare l'ordine di ricerca dei nodi durante l'esecuzione di un'operazione di ricerca e sostituzione del testo.

```

 public void useLegacyOrder(boolean useLegacyOrder) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Insert three runs which we can search for using a regex pattern.
     // Place one of those runs inside a text box.
     builder.writeln("[tag 1]");
     Shape textBox = builder.insertShape(ShapeType.TEXT_BOX, 100.0, 50.0);
     builder.writeln("[tag 2]");
     builder.moveTo(textBox.getFirstParagraph());
     builder.write("[tag 3]");

     // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
     FindReplaceOptions options = new FindReplaceOptions();

     // Assign a custom callback to the "ReplacingCallback" property.
     TextReplacementTracker callback = new TextReplacementTracker();
     options.setReplacingCallback(callback);

     // If we set the "UseLegacyOrder" property to "true", the
     // find-and-replace operation will go through all the runs outside of a text box
     // before going through the ones inside a text box.
     // If we set the "UseLegacyOrder" property to "false", the
     // find-and-replace operation will go over all the runs in a range in sequential order.
     options.setUseLegacyOrder(useLegacyOrder);

     doc.getRange().replace("\[tag d*\]", "", options);
 }

 public static Object[][] useLegacyOrderDataProvider() {
     return new Object[][]
             {
                     {true},
                     {false},
             };
 }

 /// 
 /// Records the order of all matches that occur during a find-and-replace operation.
 /// 
 private static class TextReplacementTracker implements IReplacingCallback {
     public int replacing(ReplacingArgs e) {
         mMatches.add(e.getMatch().group(1));
         return ReplaceAction.REPLACE;
     }

     public ArrayList getMatches() {
         return mMatches;
     }

     private ArrayList mMatches;
 }
 
```

**Returns:**
boolean - Il valore booleano corrispondente.
### getUseSubstitutions() {#getUseSubstitutions}
```
public boolean getUseSubstitutions()
```


Restituisce un valore booleano che indica se riconoscere e utilizzare le sostituzioni nei modelli di sostituzione. Il valore predefinito è false.

 **Remarks:** 

Per i dettagli sugli elementi di sostituzione, fare riferimento a: https://docs.microsoft.com/en-us/dotnet/standard/base-types/substitutions-in-regular-expressions.

 **Examples:** 

Mostra come riconoscere e utilizzare le sostituzioni nei modelli di sostituzione.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("Jason gave money to Paul.");

 String regex = "([A-z]+) gave money to ([A-z]+)";

 FindReplaceOptions options = new FindReplaceOptions();
 options.setUseSubstitutions(true);

 // Using legacy mode does not support many advanced features, so we need to set it to 'false'.
 options.setLegacyMode(false);

 doc.getRange().replace(Pattern.compile(regex), "$2 took money from $1", options);

 Assert.assertEquals(doc.getText(), "Paul took money from Jason.\f");
 
```

Mostra come sostituire il testo con le sostituzioni.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("John sold a car to Paul.");
 builder.writeln("Jane sold a house to Joe.");

 // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
 FindReplaceOptions options = new FindReplaceOptions();

 // Set the "UseSubstitutions" property to "true" to get
 // the find-and-replace operation to recognize substitution elements.
 // Set the "UseSubstitutions" property to "false" to ignore substitution elements.
 options.setUseSubstitutions(useSubstitutions);

 doc.getRange().replace(Pattern.compile("([A-z]+) sold a ([A-z]+) to ([A-z]+)"), "$3 bought a $2 from $1", options);

 Assert.assertEquals(
         useSubstitutions
                 ? "Paul bought a car from John.\rJoe bought a house from Jane."
                 : "$3 bought a $2 from $1.\r$3 bought a $2 from $1.", doc.getText().trim());
 
```

**Returns:**
boolean - Un valore booleano che indica se riconoscere e utilizzare le sostituzioni nei modelli di sostituzione.
### setDirection(int value) {#setDirection-int}
```
public void setDirection(int value)
```


Seleziona la direzione per la sostituzione. Il valore predefinito è [FindReplaceDirection.FORWARD](../../com.aspose.words/findreplacedirection/\#FORWARD).

 **Examples:** 

Mostra come determinare in quale direzione un'operazione di ricerca e sostituzione attraversa il documento.

```

 public void direction(int findReplaceDirection) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Insert three runs which we can search for using a regex pattern.
     // Place one of those runs inside a text box.
     builder.writeln("Match 1.");
     builder.writeln("Match 2.");
     builder.writeln("Match 3.");
     builder.writeln("Match 4.");

     // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
     FindReplaceOptions options = new FindReplaceOptions();

     // Assign a custom callback to the "ReplacingCallback" property.
     TextReplacementRecorder callback = new TextReplacementRecorder();
     options.setReplacingCallback(callback);

     // Set the "Direction" property to "FindReplaceDirection.Backward" to get the find-and-replace
     // operation to start from the end of the range, and traverse back to the beginning.
     // Set the "Direction" property to "FindReplaceDirection.Forward" to get the find-and-replace
     // operation to start from the beginning of the range, and traverse to the end.
     options.setDirection(findReplaceDirection);

     doc.getRange().replace(Pattern.compile("Match \\d*"), "Replacement", options);

     Assert.assertEquals("Replacement.\r" +
             "Replacement.\r" +
             "Replacement.\r" +
             "Replacement.", doc.getText().trim());

     switch (findReplaceDirection) {
         case FindReplaceDirection.FORWARD:
             Assert.assertEquals(new String[]{"Match 1", "Match 2", "Match 3", "Match 4"}, callback.getMatches().toArray());
             break;
         case FindReplaceDirection.BACKWARD:
             Assert.assertEquals(new String[]{"Match 4", "Match 3", "Match 2", "Match 1"}, callback.getMatches().toArray());
             break;
     }
 }

 public static Object[][] directionDataProvider() {
     return new Object[][]
             {
                     {FindReplaceDirection.BACKWARD},
                     {FindReplaceDirection.FORWARD},
             };
 }

 /// 
 /// Records all matches that occur during a find-and-replace operation in the order that they take place.
 /// 
 private static class TextReplacementRecorder implements IReplacingCallback {
     public int replacing(ReplacingArgs e) {
         mMatches.add(e.getMatch().group(0));
         return ReplaceAction.REPLACE;
     }

     public ArrayList getMatches() {
         return mMatches;
     }
     private ArrayList mMatches = new ArrayList<>();
 }
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Il valore int corrispondente. Il valore deve essere una delle costanti di [FindReplaceDirection](../../com.aspose.words/findreplacedirection/). |

### setFindWholeWordsOnly(boolean value) {#setFindWholeWordsOnly-boolean}
```
public void setFindWholeWordsOnly(boolean value)
```


True indica che oldValue deve essere una parola isolata.

 **Examples:** 

Mostra come attivare/disattivare le operazioni di ricerca e sostituzione che riguardano solo parole isolate.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Jackson will meet you in Jacksonville.");

 // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
 FindReplaceOptions options = new FindReplaceOptions();

 // Set the "FindWholeWordsOnly" flag to "true" to replace the found text if it is not a part of another word.
 // Set the "FindWholeWordsOnly" flag to "false" to replace all text regardless of its surroundings.
 options.setFindWholeWordsOnly(findWholeWordsOnly);

 doc.getRange().replace("Jackson", "Louis", options);

 Assert.assertEquals(
         findWholeWordsOnly ? "Louis will meet you in Jacksonville." : "Louis will meet you in Louisville.",
         doc.getText().trim());
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setIgnoreDeleted(boolean value) {#setIgnoreDeleted-boolean}
```
public void setIgnoreDeleted(boolean value)
```


Imposta un valore booleano che indica se ignorare il testo all'interno delle revisioni di eliminazione. Il valore predefinito è false.

 **Examples:** 

Mostra come includere o ignorare il testo all'interno delle revisioni di eliminazione durante un'operazione di ricerca e sostituzione.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");
 builder.writeln("Hello again!");

 // Start tracking revisions and remove the second paragraph, which will create a delete revision.
 // That paragraph will persist in the document until we accept the delete revision.
 doc.startTrackRevisions("John Doe", new Date());
 doc.getFirstSection().getBody().getParagraphs().get(1).remove();
 doc.stopTrackRevisions();

 Assert.assertTrue(doc.getFirstSection().getBody().getParagraphs().get(1).isDeleteRevision());

 // We can use a "FindReplaceOptions" object to modify the find and replace process.
 FindReplaceOptions options = new FindReplaceOptions();

 // Set the "IgnoreDeleted" flag to "true" to get the find-and-replace
 // operation to ignore paragraphs that are delete revisions.
 // Set the "IgnoreDeleted" flag to "false" to get the find-and-replace
 // operation to also search for text inside delete revisions.
 options.setIgnoreDeleted(ignoreTextInsideDeleteRevisions);

 doc.getRange().replace("Hello", "Greetings", options);

 Assert.assertEquals(
         ignoreTextInsideDeleteRevisions
                 ? "Greetings world!\rHello again!"
                 : "Greetings world!\rGreetings again!", doc.getText().trim());
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Un valore booleano che indica se ignorare il testo all'interno delle revisioni di eliminazione. |

### setIgnoreFieldCodes(boolean value) {#setIgnoreFieldCodes-boolean}
```
public void setIgnoreFieldCodes(boolean value)
```


Imposta un valore booleano che indica se ignorare il testo all'interno dei codici di campo. Il valore predefinito è false.

 **Remarks:** 

Questa opzione influisce solo sui codici di campo (non ignora i nodi tra [NodeType.FIELD\_SEPARATOR](../../com.aspose.words/nodetype/\#FIELD-SEPARATOR) e [NodeType.FIELD\_END](../../com.aspose.words/nodetype/\#FIELD-END)).

Per ignorare l'intero campo, si prega di utilizzare l'opzione corrispondente [getIgnoreFields()](../../com.aspose.words/findreplaceoptions/\#getIgnoreFields) / [setIgnoreFields(boolean)](../../com.aspose.words/findreplaceoptions/\#setIgnoreFields-boolean).

 **Examples:** 

Mostra come ignorare il testo all'interno dei codici di campo.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.insertField("INCLUDETEXT", "Test IT!");

 FindReplaceOptions options = new FindReplaceOptions(); {options.setIgnoreFieldCodes(ignoreFieldCodes);}

 // Replace 'T' in document ignoring text inside field code or not.
 doc.getRange().replace(Pattern.compile("T"), "*", options);
 System.out.println(doc.getText());

 Assert.assertEquals(
         ignoreFieldCodes
                 ? "INCLUDETEXT*est I*!"
                 : "INCLUDE*EX**est I*!", doc.getText().trim());
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Un valore booleano che indica se ignorare il testo all'interno dei codici di campo. |

### setIgnoreFields(boolean value) {#setIgnoreFields-boolean}
```
public void setIgnoreFields(boolean value)
```


Imposta un valore booleano che indica se ignorare il testo all'interno dei campi. Il valore predefinito è false.

 **Remarks:** 

Questa opzione influisce sull'intero campo (tutti i nodi tra [NodeType.FIELD\_START](../../com.aspose.words/nodetype/\#FIELD-START) e [NodeType.FIELD\_END](../../com.aspose.words/nodetype/\#FIELD-END)).

Per ignorare solo i codici di campo, si prega di utilizzare l'opzione corrispondente [getIgnoreFieldCodes()](../../com.aspose.words/findreplaceoptions/\#getIgnoreFieldCodes) / [setIgnoreFieldCodes(boolean)](../../com.aspose.words/findreplaceoptions/\#setIgnoreFieldCodes-boolean).

 **Examples:** 

Mostra come ignorare il testo all'interno dei campi.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");
 builder.insertField("QUOTE", "Hello again!");

 // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
 FindReplaceOptions options = new FindReplaceOptions();

 // Set the "IgnoreFields" flag to "true" to get the find-and-replace
 // operation to ignore text inside fields.
 // Set the "IgnoreFields" flag to "false" to get the find-and-replace
 // operation to also search for text inside fields.
 options.setIgnoreFields(ignoreTextInsideFields);

 doc.getRange().replace("Hello", "Greetings", options);

 Assert.assertEquals(
         ignoreTextInsideFields
                 ? "Greetings world!\rQUOTEHello again!"
                 : "Greetings world!\rQUOTEGreetings again!", doc.getText().trim());
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Un valore booleano che indica se ignorare il testo all'interno dei campi. |

### setIgnoreFootnotes(boolean value) {#setIgnoreFootnotes-boolean}
```
public void setIgnoreFootnotes(boolean value)
```


Imposta un valore booleano che indica se ignorare le note a piè di pagina. Il valore predefinito è false.

 **Examples:** 

Mostra come ignorare le note a piè di pagina durante un'operazione di ricerca e sostituzione.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

 builder.insertParagraph();

 builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

 // Set the "IgnoreFootnotes" flag to "true" to get the find-and-replace
 // operation to ignore text inside footnotes.
 // Set the "IgnoreFootnotes" flag to "false" to get the find-and-replace
 // operation to also search for text inside footnotes.
 FindReplaceOptions options = new FindReplaceOptions();
 {
     options.setIgnoreFootnotes(isIgnoreFootnotes);
 }
 doc.getRange().replace("Lorem ipsum", "Replaced Lorem ipsum", options);
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Un valore booleano che indica se ignorare le note a piè di pagina. |

### setIgnoreInserted(boolean value) {#setIgnoreInserted-boolean}
```
public void setIgnoreInserted(boolean value)
```


Imposta un valore booleano che indica se ignorare il testo all'interno delle revisioni di inserimento. Il valore predefinito è false.

 **Examples:** 

Mostra come includere o ignorare il testo all'interno delle revisioni di inserimento durante un'operazione di ricerca e sostituzione.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");

 // Start tracking revisions and insert a paragraph. That paragraph will be an insert revision.
 doc.startTrackRevisions("John Doe", new Date());
 builder.writeln("Hello again!");
 doc.stopTrackRevisions();

 Assert.assertTrue(doc.getFirstSection().getBody().getParagraphs().get(1).isInsertRevision());

 // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
 FindReplaceOptions options = new FindReplaceOptions();

 // Set the "IgnoreInserted" flag to "true" to get the find-and-replace
 // operation to ignore paragraphs that are insert revisions.
 // Set the "IgnoreInserted" flag to "false" to get the find-and-replace
 // operation to also search for text inside insert revisions.
 options.setIgnoreInserted(ignoreTextInsideInsertRevisions);

 doc.getRange().replace("Hello", "Greetings", options);

 Assert.assertEquals(
         ignoreTextInsideInsertRevisions
                 ? "Greetings world!\rHello again!"
                 : "Greetings world!\rGreetings again!", doc.getText().trim());
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Un valore booleano che indica se ignorare il testo all'interno delle revisioni di inserimento. |

### setIgnoreOfficeMath(boolean value) {#setIgnoreOfficeMath-boolean}
```
public void setIgnoreOfficeMath(boolean value)
```


Imposta un valore booleano che indica se ignorare il testo all'interno di OfficeMath/>. Il valore predefinito è true.

 **Examples:** 

Mostra come trovare e sostituire il testo all'interno di OfficeMath.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 Assert.assertEquals("i+b-c\u2265iM+bM-cM", doc.getFirstSection().getBody().getFirstParagraph().getText().trim());

 FindReplaceOptions options = new FindReplaceOptions();
 options.setIgnoreOfficeMath(isIgnoreOfficeMath);
 doc.getRange().replace("b", "x", options);

 if (isIgnoreOfficeMath)
     Assert.assertEquals("i+b-c\u2265iM+bM-cM", doc.getFirstSection().getBody().getFirstParagraph().getText().trim());
 else
     Assert.assertEquals("i+x-c\u2265iM+xM-cM", doc.getFirstSection().getBody().getFirstParagraph().getText().trim());
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Un valore booleano che indica se ignorare il testo all'interno di OfficeMath/>. |

### setIgnoreShapes(boolean value) {#setIgnoreShapes-boolean}
```
public void setIgnoreShapes(boolean value)
```


Ottiene o imposta un valore booleano che indica se ignorare le forme all'interno di un testo.

Il valore predefinito è  false .

 **Examples:** 

Mostra come ignorare le forme durante la sostituzione del testo.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
 builder.insertShape(ShapeType.BALLOON, 200.0, 200.0);
 builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

 FindReplaceOptions findReplaceOptions = new FindReplaceOptions(); { findReplaceOptions.setIgnoreShapes(true); }
 builder.getDocument().getRange().replace("Lorem ipsum dolor sit amet, consectetur adipiscing elit.Lorem ipsum dolor sit amet, consectetur adipiscing elit.",
     "Lorem ipsum dolor sit amet, consectetur adipiscing elit.", findReplaceOptions);
 Assert.assertEquals("Lorem ipsum dolor sit amet, consectetur adipiscing elit.", builder.getDocument().getText().trim());
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setIgnoreStructuredDocumentTags(boolean value) {#setIgnoreStructuredDocumentTags-boolean}
```
public void setIgnoreStructuredDocumentTags(boolean value)
```


Imposta un valore booleano che indica se ignorare il contenuto di [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/). Il valore predefinito è false.

 **Remarks:** 

Quando questa opzione è impostata su true, il contenuto di [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) verrà trattato come testo semplice.

Altrimenti, [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) verrà elaborato come Story autonomo e il modello di sostituzione verrà cercato separatamente per ogni [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/), in modo che se il modello attraversa un [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/), la sostituzione non verrà eseguita per tale modello.

 **Examples:** 

Mostra come ignorare il contenuto dei tag durante la sostituzione.

```

 Document doc = new Document(getMyDir() + "Structured document tags.docx");

 // This paragraph contains SDT.
 Paragraph p = (Paragraph)doc.getFirstSection().getBody().getChild(NodeType.PARAGRAPH, 2, true);
 String textToSearch = p.toString(SaveFormat.TEXT).trim();

 FindReplaceOptions options = new FindReplaceOptions();
 options.setIgnoreStructuredDocumentTags(true);
 doc.getRange().replace(textToSearch, "replacement", options);

 doc.save(getArtifactsDir() + "StructuredDocumentTag.IgnoreStructuredDocumentTags.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | boolean | Un valore booleano che indica se ignorare il contenuto di [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/). |

### setLegacyMode(boolean value) {#setLegacyMode-boolean}
```
public void setLegacyMode(boolean value)
```


Imposta un valore booleano che indica che viene utilizzato il vecchio algoritmo di ricerca/sostituzione.

 **Remarks:** 

Utilizza questo flag se hai bisogno esattamente dello stesso comportamento di prima dell'introduzione della funzionalità avanzata di ricerca/sostituzione. Nota che il vecchio algoritmo non supporta funzionalità avanzate come la sostituzione con interruzioni, l'applicazione di formattazione e così via.

 **Examples:** 

Mostra come riconoscere e utilizzare le sostituzioni nei modelli di sostituzione.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("Jason gave money to Paul.");

 String regex = "([A-z]+) gave money to ([A-z]+)";

 FindReplaceOptions options = new FindReplaceOptions();
 options.setUseSubstitutions(true);

 // Using legacy mode does not support many advanced features, so we need to set it to 'false'.
 options.setLegacyMode(false);

 doc.getRange().replace(Pattern.compile(regex), "$2 took money from $1", options);

 Assert.assertEquals(doc.getText(), "Paul took money from Jason.\f");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Un valore booleano che indica che viene utilizzato il vecchio algoritmo di ricerca/sostituzione. |

### setMatchCase(boolean value) {#setMatchCase-boolean}
```
public void setMatchCase(boolean value)
```


True indica un confronto sensibile al maiuscolo/minuscolo, false indica un confronto insensibile al maiuscolo/minuscolo.

 **Examples:** 

Mostra come attivare/disattivare la distinzione tra maiuscole e minuscole durante un'operazione di ricerca e sostituzione.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Ruby bought a ruby necklace.");

 // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
 FindReplaceOptions options = new FindReplaceOptions();

 // Set the "MatchCase" flag to "true" to apply case sensitivity while finding strings to replace.
 // Set the "MatchCase" flag to "false" to ignore character case while searching for text to replace.
 options.setMatchCase(matchCase);

 doc.getRange().replace("Ruby", "Jade", options);

 Assert.assertEquals(matchCase ? "Jade bought a ruby necklace." : "Jade bought a Jade necklace.",
         doc.getText().trim());
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setReplacementFormat(int value) {#setReplacementFormat-int}
```
public void setReplacementFormat(int value)
```


Specifica il formato della sostituzione. Il valore predefinito è [ReplacementFormat.TEXT](../../com.aspose.words/replacementformat/\#TEXT).

 **Remarks:** 

Ha effetto solo quando viene utilizzato in [Replacer](../../com.aspose.words/replacer/)

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Il valore intero corrispondente. Il valore deve essere una delle costanti di [ReplacementFormat](../../com.aspose.words/replacementformat/). |

### setReplacingCallback(IReplacingCallback value) {#setReplacingCallback-com.aspose.words.IReplacingCallback}
```
public void setReplacingCallback(IReplacingCallback value)
```


Il metodo definito dall'utente che viene chiamato prima di ogni occorrenza di sostituzione.

 **Examples:** 

Mostra come sostituire tutte le occorrenze di un modello di espressione regolare con un'altra stringa, tenendo traccia di tutte queste sostituzioni.

```

 public void replaceWithCallback() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.writeln("Our new location in New York City is opening tomorrow. " +
             "Hope to see all our NYC-based customers at the opening!");

     // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
     FindReplaceOptions options = new FindReplaceOptions();

     // Set a callback that tracks any replacements that the "Replace" method will make.
     TextFindAndReplacementLogger logger = new TextFindAndReplacementLogger();
     options.setReplacingCallback(logger);

     doc.getRange().replace(Pattern.compile("New York City|NYC"), "Washington", options);

     Assert.assertEquals("Our new location in (Old value:\"New York City\") Washington is opening tomorrow. " +
             "Hope to see all our (Old value:\"NYC\") Washington-based customers at the opening!", doc.getText().trim());

     Assert.assertEquals("\"New York City\" converted to \"Washington\" 20 characters into a 21 node." +
             "\"NYC\" converted to \"Washington\" 42 characters into a 21 node.", logger.getLog().trim());
 }

 /// 
 /// Maintains a log of every text replacement done by a find-and-replace operation
 /// and notes the original matched text's value.
 /// 
 private static class TextFindAndReplacementLogger implements IReplacingCallback {
     public int replacing(ReplacingArgs args) {
         mLog.append(MessageFormat.format("\"{0}\" converted to \"{1}\" {2} characters into a {3} node.", args.getMatch().group(0), args.getReplacement(), args.getMatchOffset(), args.getMatchNode().getNodeType()));

         args.setReplacement(MessageFormat.format("(Old value:\"{0}\") {1}", args.getMatch().group(0), args.getReplacement()));
         return ReplaceAction.REPLACE;
     }

     public String getLog() {
         return mLog.toString();
     }

     private final StringBuilder mLog = new StringBuilder();
 }
 
```

Mostra come applicare un carattere diverso al nuovo contenuto tramite FindReplaceOptions.

```

 public void convertNumbersToHexadecimal() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.getFont().setName("Arial");
     builder.writeln("Numbers that the find-and-replace operation will convert to hexadecimal and highlight:\n" +
             "123, 456, 789 and 17379.");

     // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
     FindReplaceOptions options = new FindReplaceOptions();

     // Set the "HighlightColor" property to a background color that we want to apply to the operation's resulting text.
     options.getApplyFont().setHighlightColor(Color.GRAY);

     NumberHexer numberHexer = new NumberHexer();
     options.setReplacingCallback(numberHexer);

     int replacementCount = doc.getRange().replace(Pattern.compile("[0-9]+"), "", options);

     System.out.println(numberHexer.getLog());

     Assert.assertEquals(4, replacementCount);
     Assert.assertEquals("Numbers that the find-and-replace operation will convert to hexadecimal and highlight:\r" +
             "0x123, 0x456, 0x789 and 0x17,379.", doc.getText().trim());
 }

 /// 
 /// Replaces numeric find-and-replacement matches with their hexadecimal equivalents.
 /// Maintains a log of every replacement.
 /// 
 private static class NumberHexer implements IReplacingCallback {
     public int replacing(ReplacingArgs args) {
         mCurrentReplacementNumber++;

         int number = Integer.parseInt(args.getMatch().group(0));

         args.setReplacement(MessageFormat.format("0x{0}", number));

         mLog.append(MessageFormat.format("Match #{0}", mCurrentReplacementNumber));
         mLog.append(MessageFormat.format("\tOriginal value:\t{0}", args.getMatch().group(0)));
         mLog.append(MessageFormat.format("\tReplacement:\t{0}", args.getReplacement()));
         mLog.append(MessageFormat.format("\tOffset in parent {0} node:\t{1}", args.getMatchNode().getNodeType(), args.getMatchOffset()));

         return ReplaceAction.REPLACE;
     }

     public String getLog() {
         return mLog.toString();
     }

     private int mCurrentReplacementNumber;
     private final StringBuilder mLog = new StringBuilder();
 }
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | [IReplacingCallback](../../com.aspose.words/ireplacingcallback/) | Il valore corrispondente di [IReplacingCallback](../../com.aspose.words/ireplacingcallback/). |

### setSmartParagraphBreakReplacement(boolean value) {#setSmartParagraphBreakReplacement-boolean}
```
public void setSmartParagraphBreakReplacement(boolean value)
```


Ottiene o imposta un valore booleano che indica se è consentito sostituire l'interruzione di paragrafo quando non esiste un paragrafo fratello successivo.

Il valore predefinito è  false .

 **Remarks:** 

Questa opzione consente di sostituire l'interruzione di paragrafo quando non esiste un paragrafo fratello successivo a cui spostare tutti i nodi figlio, trovando qualsiasi (non necessariamente fratello) paragrafo successivo a quello che viene sostituito.

 **Examples:** 

Mostra come rimuovere un paragrafo da una cella di tabella con una tabella nidificata.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create table with paragraph and inner table in first cell.
 builder.startTable();
 builder.insertCell();
 builder.write("TEXT1");
 builder.startTable();
 builder.insertCell();
 builder.endTable();
 builder.endTable();
 builder.writeln();

 FindReplaceOptions options = new FindReplaceOptions();
 // When the following option is set to 'true', Aspose.Words will remove paragraph's text
 // completely with its paragraph mark. Otherwise, Aspose.Words will mimic Word and remove
 // only paragraph's text and leaves the paragraph mark intact (when a table follows the text).
 options.setSmartParagraphBreakReplacement(isSmartParagraphBreakReplacement);
 doc.getRange().replace("TEXT1&p", "", options);

 doc.save(getArtifactsDir() + "Table.RemoveParagraphTextAndMark.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setUseLegacyOrder(boolean value) {#setUseLegacyOrder-boolean}
```
public void setUseLegacyOrder(boolean value)
```


True indica che la ricerca del testo viene eseguita in modo sequenziale dall'alto verso il basso considerando le caselle di testo. Il valore predefinito è false.

 **Examples:** 

Mostra come modificare l'ordine di ricerca dei nodi durante l'esecuzione di un'operazione di ricerca e sostituzione del testo.

```

 public void useLegacyOrder(boolean useLegacyOrder) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Insert three runs which we can search for using a regex pattern.
     // Place one of those runs inside a text box.
     builder.writeln("[tag 1]");
     Shape textBox = builder.insertShape(ShapeType.TEXT_BOX, 100.0, 50.0);
     builder.writeln("[tag 2]");
     builder.moveTo(textBox.getFirstParagraph());
     builder.write("[tag 3]");

     // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
     FindReplaceOptions options = new FindReplaceOptions();

     // Assign a custom callback to the "ReplacingCallback" property.
     TextReplacementTracker callback = new TextReplacementTracker();
     options.setReplacingCallback(callback);

     // If we set the "UseLegacyOrder" property to "true", the
     // find-and-replace operation will go through all the runs outside of a text box
     // before going through the ones inside a text box.
     // If we set the "UseLegacyOrder" property to "false", the
     // find-and-replace operation will go over all the runs in a range in sequential order.
     options.setUseLegacyOrder(useLegacyOrder);

     doc.getRange().replace("\[tag d*\]", "", options);
 }

 public static Object[][] useLegacyOrderDataProvider() {
     return new Object[][]
             {
                     {true},
                     {false},
             };
 }

 /// 
 /// Records the order of all matches that occur during a find-and-replace operation.
 /// 
 private static class TextReplacementTracker implements IReplacingCallback {
     public int replacing(ReplacingArgs e) {
         mMatches.add(e.getMatch().group(1));
         return ReplaceAction.REPLACE;
     }

     public ArrayList getMatches() {
         return mMatches;
     }

     private ArrayList mMatches;
 }
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setUseSubstitutions(boolean value) {#setUseSubstitutions-boolean}
```
public void setUseSubstitutions(boolean value)
```


Imposta un valore booleano che indica se riconoscere e utilizzare le sostituzioni nei modelli di sostituzione. Il valore predefinito è false.

 **Remarks:** 

Per i dettagli sugli elementi di sostituzione, fare riferimento a: https://docs.microsoft.com/en-us/dotnet/standard/base-types/substitutions-in-regular-expressions.

 **Examples:** 

Mostra come riconoscere e utilizzare le sostituzioni nei modelli di sostituzione.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("Jason gave money to Paul.");

 String regex = "([A-z]+) gave money to ([A-z]+)";

 FindReplaceOptions options = new FindReplaceOptions();
 options.setUseSubstitutions(true);

 // Using legacy mode does not support many advanced features, so we need to set it to 'false'.
 options.setLegacyMode(false);

 doc.getRange().replace(Pattern.compile(regex), "$2 took money from $1", options);

 Assert.assertEquals(doc.getText(), "Paul took money from Jason.\f");
 
```

Mostra come sostituire il testo con le sostituzioni.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("John sold a car to Paul.");
 builder.writeln("Jane sold a house to Joe.");

 // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
 FindReplaceOptions options = new FindReplaceOptions();

 // Set the "UseSubstitutions" property to "true" to get
 // the find-and-replace operation to recognize substitution elements.
 // Set the "UseSubstitutions" property to "false" to ignore substitution elements.
 options.setUseSubstitutions(useSubstitutions);

 doc.getRange().replace(Pattern.compile("([A-z]+) sold a ([A-z]+) to ([A-z]+)"), "$3 bought a $2 from $1", options);

 Assert.assertEquals(
         useSubstitutions
                 ? "Paul bought a car from John.\rJoe bought a house from Jane."
                 : "$3 bought a $2 from $1.\r$3 bought a $2 from $1.", doc.getText().trim());
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Un valore booleano che indica se riconoscere e utilizzare le sostituzioni nei modelli di sostituzione. |

