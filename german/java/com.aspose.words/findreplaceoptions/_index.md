---
title: "FindReplaceOptions"
linktitle: "FindReplaceOptions"
second_title: "Aspose.Words für Java"
description: "Gibt Optionen für Find/Replace‑Operationen in Java an."
type: docs
weight: 314
url: /de/java/com.aspose.words/findreplaceoptions/
---

**Inheritance:**
java.lang.Object
```
public class FindReplaceOptions
```

Gibt Optionen für Suchen/Ersetzen-Operationen an.

Um mehr zu erfahren, besuchen Sie den [ Find and Replace ][Find and Replace] Dokumentationsartikel.

 **Examples:** 

Zeigt, wie man die Groß-/Kleinschreibung bei einer Find‑and‑Replace‑Operation umschaltet.

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

Zeigt, wie man eigenständige Wort‑nur‑Find‑and‑Replace‑Operationen umschaltet.

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
## Konstruktoren

| Konstruktor | Beschreibung |
| --- | --- |
| [FindReplaceOptions()](#FindReplaceOptions) | Initialisiert eine neue Instanz der FindReplaceOptions‑Klasse mit Standardeinstellungen. |
| [FindReplaceOptions(int direction)](#FindReplaceOptions-int) | Initialisiert eine neue Instanz dieser Klasse. |
| [FindReplaceOptions(IReplacingCallback replacingCallback)](#FindReplaceOptions-com.aspose.words.IReplacingCallback) | Initialisiert eine neue Instanz der FindReplaceOptions‑Klasse mit dem angegebenen Ersetzungs‑Callback. |
| [FindReplaceOptions(int direction, IReplacingCallback replacingCallback)](#FindReplaceOptions-int-com.aspose.words.IReplacingCallback) | Initialisiert eine neue Instanz dieser Klasse. |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getApplyFont()](#getApplyFont) | Textformatierung, die auf neuen Inhalt angewendet wird. |
| [getApplyParagraphFormat()](#getApplyParagraphFormat) | Absatzformatierung, die auf neuen Inhalt angewendet wird. |
| [getDirection()](#getDirection) | Wählt die Richtung für das Ersetzen aus. |
| [getFindWholeWordsOnly()](#getFindWholeWordsOnly) | True gibt an, dass oldValue ein eigenständiges Wort sein muss. |
| [getIgnoreDeleted()](#getIgnoreDeleted) | Liefert einen booleschen Wert, der angibt, ob Text innerhalb von Löschrevisionen ignoriert werden soll. |
| [getIgnoreFieldCodes()](#getIgnoreFieldCodes) | Liefert einen booleschen Wert, der angibt, ob Text innerhalb von Feldcodes ignoriert werden soll. |
| [getIgnoreFields()](#getIgnoreFields) | Liefert einen booleschen Wert, der angibt, ob Text innerhalb von Feldern ignoriert werden soll. |
| [getIgnoreFootnotes()](#getIgnoreFootnotes) | Liefert einen booleschen Wert, der angibt, ob Fußnoten ignoriert werden sollen. |
| [getIgnoreInserted()](#getIgnoreInserted) | Liefert einen booleschen Wert, der angibt, ob Text innerhalb von Einfüge-Revisionen ignoriert werden soll. |
| [getIgnoreOfficeMath()](#getIgnoreOfficeMath) | Liefert einen booleschen Wert, der angibt, ob Text innerhalb von OfficeMath/> ignoriert werden soll. |
| [getIgnoreShapes()](#getIgnoreShapes) | Liefert oder setzt einen booleschen Wert, der angibt, ob Formen innerhalb eines Textes ignoriert werden sollen. |
| [getIgnoreStructuredDocumentTags()](#getIgnoreStructuredDocumentTags) | Liefert einen booleschen Wert, der angibt, ob der Inhalt von [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) ignoriert werden soll. |
| [getLegacyMode()](#getLegacyMode) | Liefert einen booleschen Wert, der angibt, dass der alte Such‑/Ersetzungsalgorithmus verwendet wird. |
| [getMatchCase()](#getMatchCase) | True gibt einen fallabhängigen Vergleich an, false einen fallunabhängigen Vergleich. |
| [getReplacementFormat()](#getReplacementFormat) | Gibt das Format der Ersetzung an. |
| [getReplacingCallback()](#getReplacingCallback) | Die benutzerdefinierte Methode, die vor jedem Ersetzungsereignis aufgerufen wird. |
| [getSmartParagraphBreakReplacement()](#getSmartParagraphBreakReplacement) | Liefert oder setzt einen booleschen Wert, der angibt, ob ein Absatzumbruch ersetzt werden darf, wenn kein nachfolgender Geschwisterabsatz vorhanden ist. |
| [getUseLegacyOrder()](#getUseLegacyOrder) | True gibt an, dass eine Textsuche sequenziell von oben nach unten unter Berücksichtigung von Textfeldern durchgeführt wird. |
| [getUseSubstitutions()](#getUseSubstitutions) | Liefert einen booleschen Wert, der angibt, ob Ersetzungen innerhalb von Ersetzungsmustern erkannt und verwendet werden sollen. |
| [setDirection(int value)](#setDirection-int) | Wählt die Richtung für das Ersetzen aus. |
| [setFindWholeWordsOnly(boolean value)](#setFindWholeWordsOnly-boolean) | True gibt an, dass oldValue ein eigenständiges Wort sein muss. |
| [setIgnoreDeleted(boolean value)](#setIgnoreDeleted-boolean) | Setzt einen booleschen Wert, der angibt, ob Text innerhalb von Löschrevisionen ignoriert werden soll. |
| [setIgnoreFieldCodes(boolean value)](#setIgnoreFieldCodes-boolean) | Setzt einen booleschen Wert, der angibt, ob Text innerhalb von Feldcodes ignoriert werden soll. |
| [setIgnoreFields(boolean value)](#setIgnoreFields-boolean) | Setzt einen booleschen Wert, der angibt, ob Text innerhalb von Feldern ignoriert werden soll. |
| [setIgnoreFootnotes(boolean value)](#setIgnoreFootnotes-boolean) | Setzt einen booleschen Wert, der angibt, ob Fußnoten ignoriert werden sollen. |
| [setIgnoreInserted(boolean value)](#setIgnoreInserted-boolean) | Setzt einen booleschen Wert, der angibt, ob Text innerhalb von Einfüge‑Revisionen ignoriert werden soll. |
| [setIgnoreOfficeMath(boolean value)](#setIgnoreOfficeMath-boolean) | Setzt einen booleschen Wert, der angibt, ob Text innerhalb von OfficeMath/> ignoriert werden soll. |
| [setIgnoreShapes(boolean value)](#setIgnoreShapes-boolean) | Liefert oder setzt einen booleschen Wert, der angibt, ob Formen innerhalb eines Textes ignoriert werden sollen. |
| [setIgnoreStructuredDocumentTags(boolean value)](#setIgnoreStructuredDocumentTags-boolean) | Setzt einen booleschen Wert, der angibt, ob der Inhalt von [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) ignoriert werden soll. |
| [setLegacyMode(boolean value)](#setLegacyMode-boolean) | Setzt einen booleschen Wert, der angibt, dass der alte Such‑/Ersetzungsalgorithmus verwendet wird. |
| [setMatchCase(boolean value)](#setMatchCase-boolean) | True gibt einen fallabhängigen Vergleich an, false einen fallunabhängigen Vergleich. |
| [setReplacementFormat(int value)](#setReplacementFormat-int) | Gibt das Format der Ersetzung an. |
| [setReplacingCallback(IReplacingCallback value)](#setReplacingCallback-com.aspose.words.IReplacingCallback) | Die benutzerdefinierte Methode, die vor jedem Ersetzungsereignis aufgerufen wird. |
| [setSmartParagraphBreakReplacement(boolean value)](#setSmartParagraphBreakReplacement-boolean) | Liefert oder setzt einen booleschen Wert, der angibt, ob ein Absatzumbruch ersetzt werden darf, wenn kein nachfolgender Geschwisterabsatz vorhanden ist. |
| [setUseLegacyOrder(boolean value)](#setUseLegacyOrder-boolean) | True gibt an, dass eine Textsuche sequenziell von oben nach unten unter Berücksichtigung von Textfeldern durchgeführt wird. |
| [setUseSubstitutions(boolean value)](#setUseSubstitutions-boolean) | Legt einen booleschen Wert fest, der angibt, ob Substitutionen innerhalb von Ersetzungsmustern erkannt und verwendet werden sollen. |
### FindReplaceOptions() {#FindReplaceOptions}
```
public FindReplaceOptions()
```


Initialisiert eine neue Instanz der FindReplaceOptions‑Klasse mit Standardeinstellungen.

 **Examples:** 

Zeigt, wie Substitutionen innerhalb von Ersetzungsmustern erkannt und verwendet werden.

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


Initialisiert eine neue Instanz dieser Klasse.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| direction | int |  |

### FindReplaceOptions(IReplacingCallback replacingCallback) {#FindReplaceOptions-com.aspose.words.IReplacingCallback}
```
public FindReplaceOptions(IReplacingCallback replacingCallback)
```


Initialisiert eine neue Instanz der FindReplaceOptions‑Klasse mit dem angegebenen Ersetzungs‑Callback.

 **Examples:** 

Zeigt, wie die Reihenfolge verfolgt wird, in der ein Textaustauschvorgang Knoten durchläuft.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| replacingCallback | [IReplacingCallback](../../com.aspose.words/ireplacingcallback/) | Der Rückruf, der zum Ersetzen des gefundenen Textes verwendet wird. |

### FindReplaceOptions(int direction, IReplacingCallback replacingCallback) {#FindReplaceOptions-int-com.aspose.words.IReplacingCallback}
```
public FindReplaceOptions(int direction, IReplacingCallback replacingCallback)
```


Initialisiert eine neue Instanz dieser Klasse.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| direction | int |  |
| replacingCallback | [IReplacingCallback](../../com.aspose.words/ireplacingcallback/) |  |

### getApplyFont() {#getApplyFont}
```
public Font getApplyFont()
```


Textformatierung, die auf neuen Inhalt angewendet wird.

 **Examples:** 

Zeigt, wie über FindReplaceOptions eine andere Schriftart auf neuen Inhalt angewendet wird.

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


Absatzformatierung, die auf neuen Inhalt angewendet wird.

 **Examples:** 

Zeigt, wie Formatierungen zu Absätzen hinzugefügt werden, in denen ein Suchen‑und‑Ersetzen‑Vorgang Treffer gefunden hat.

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


Wählt die Richtung für das Ersetzen aus. Der Standardwert ist [FindReplaceDirection.FORWARD](../../com.aspose.words/findreplacedirection/\#FORWARD).

 **Examples:** 

Zeigt, wie ermittelt wird, in welcher Richtung ein Suchen‑und‑Ersetzen‑Vorgang das Dokument durchläuft.

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
int - Der entsprechende int‑Wert. Der zurückgegebene Wert ist einer der Konstanten von [FindReplaceDirection](../../com.aspose.words/findreplacedirection/).
### getFindWholeWordsOnly() {#getFindWholeWordsOnly}
```
public boolean getFindWholeWordsOnly()
```


True gibt an, dass oldValue ein eigenständiges Wort sein muss.

 **Examples:** 

Zeigt, wie man eigenständige Wort‑nur‑Find‑and‑Replace‑Operationen umschaltet.

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
boolean - Der entsprechende  boolean  Wert.
### getIgnoreDeleted() {#getIgnoreDeleted}
```
public boolean getIgnoreDeleted()
```


Liefert einen booleschen Wert, der angibt, ob Text innerhalb von Löschrevisionen ignoriert werden soll. Der Standardwert ist false.

 **Examples:** 

Zeigt, wie Text innerhalb von Löschrevisionen während eines Suchen‑und‑Ersetzen‑Vorgangs einbezogen oder ignoriert werden kann.

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
boolean - Ein boolescher Wert, der angibt, ob Text innerhalb von Löschrevisionen ignoriert werden soll.
### getIgnoreFieldCodes() {#getIgnoreFieldCodes}
```
public boolean getIgnoreFieldCodes()
```


Liefert einen booleschen Wert, der angibt, ob Text innerhalb von Feldcodes ignoriert werden soll. Der Standardwert ist false.

 **Remarks:** 

Diese Option wirkt sich nur auf Feldcodes aus (sie ignoriert keine Knoten zwischen [NodeType.FIELD\_SEPARATOR](../../com.aspose.words/nodetype/\#FIELD-SEPARATOR) und [NodeType.FIELD\_END](../../com.aspose.words/nodetype/\#FIELD-END)).

Um das gesamte Feld zu ignorieren, verwenden Sie bitte die entsprechende Option [getIgnoreFields()](../../com.aspose.words/findreplaceoptions/\#getIgnoreFields) / [setIgnoreFields(boolean)](../../com.aspose.words/findreplaceoptions/\#setIgnoreFields-boolean).

 **Examples:** 

Zeigt, wie Text innerhalb von Feldcodes ignoriert wird.

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
boolean - Ein boolescher Wert, der angibt, ob Text innerhalb von Feldcodes ignoriert werden soll.
### getIgnoreFields() {#getIgnoreFields}
```
public boolean getIgnoreFields()
```


Liefert einen booleschen Wert, der angibt, ob Text innerhalb von Feldern ignoriert werden soll. Der Standardwert ist false.

 **Remarks:** 

Diese Option wirkt sich auf das gesamte Feld aus (alle Knoten zwischen [NodeType.FIELD\_START](../../com.aspose.words/nodetype/\#FIELD-START) und [NodeType.FIELD\_END](../../com.aspose.words/nodetype/\#FIELD-END)).

Um nur Feldcodes zu ignorieren, verwenden Sie bitte die entsprechende Option [getIgnoreFieldCodes()](../../com.aspose.words/findreplaceoptions/\#getIgnoreFieldCodes) / [setIgnoreFieldCodes(boolean)](../../com.aspose.words/findreplaceoptions/\#setIgnoreFieldCodes-boolean).

 **Examples:** 

Zeigt, wie Text innerhalb von Feldern ignoriert wird.

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
boolean - Ein boolescher Wert, der angibt, ob Text innerhalb von Feldern ignoriert werden soll.
### getIgnoreFootnotes() {#getIgnoreFootnotes}
```
public boolean getIgnoreFootnotes()
```


Liefert einen booleschen Wert, der angibt, ob Fußnoten ignoriert werden sollen. Der Standardwert ist false.

 **Examples:** 

Zeigt, wie Fußnoten während eines Suchen‑und‑Ersetzen‑Vorgangs ignoriert werden.

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
boolean - Ein boolescher Wert, der angibt, ob Fußnoten ignoriert werden sollen.
### getIgnoreInserted() {#getIgnoreInserted}
```
public boolean getIgnoreInserted()
```


Liefert einen booleschen Wert, der angibt, ob Text innerhalb von Einfüge‑Revisionen ignoriert werden soll. Der Standardwert ist false.

 **Examples:** 

Zeigt, wie man Text innerhalb von Einfüge‑Revisionen während einer Suchen‑und‑Ersetzen‑Operation einbezieht oder ignoriert.

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
boolean - Ein boolescher Wert, der angibt, ob Text innerhalb von Einfüge‑Revisionen ignoriert werden soll.
### getIgnoreOfficeMath() {#getIgnoreOfficeMath}
```
public boolean getIgnoreOfficeMath()
```


Ermittelt einen booleschen Wert, der angibt, ob Text innerhalb von OfficeMath/> ignoriert werden soll. Der Standardwert ist  true .

 **Examples:** 

Zeigt, wie man Text innerhalb von OfficeMath findet und ersetzt.

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
boolean - Ein boolescher Wert, der angibt, ob Text innerhalb von OfficeMath/> ignoriert werden soll.
### getIgnoreShapes() {#getIgnoreShapes}
```
public boolean getIgnoreShapes()
```


Liefert oder setzt einen booleschen Wert, der angibt, ob Formen innerhalb eines Textes ignoriert werden sollen.

Der Standardwert ist  false .

 **Examples:** 

Zeigt, wie man Formen beim Ersetzen von Text ignoriert.

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
boolean - Der entsprechende  boolean  Wert.
### getIgnoreStructuredDocumentTags() {#getIgnoreStructuredDocumentTags}
```
public boolean getIgnoreStructuredDocumentTags()
```


Ermittelt einen booleschen Wert, der angibt, ob der Inhalt von [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) ignoriert werden soll. Der Standardwert ist  false .

 **Remarks:** 

Wenn diese Option auf true gesetzt ist, wird der Inhalt von [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) als einfacher Text behandelt.

Andernfalls wird [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) als eigenständige Story verarbeitet und das Ersetzungsmuster wird für jedes [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) separat gesucht, sodass, wenn das Muster ein [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) überschreitet, die Ersetzung für ein solches Muster nicht durchgeführt wird.

 **Examples:** 

Zeigt, wie man den Inhalt von Tags bei der Ersetzung ignoriert.

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
boolean - Ein boolescher Wert, der angibt, ob der Inhalt von [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) ignoriert werden soll.
### getLegacyMode() {#getLegacyMode}
```
public boolean getLegacyMode()
```


Liefert einen booleschen Wert, der angibt, dass der alte Such‑/Ersetzungsalgorithmus verwendet wird.

 **Remarks:** 

Verwenden Sie dieses Flag, wenn Sie exakt das gleiche Verhalten benötigen wie vor der Einführung der erweiterten Suchen‑/Ersetzen‑Funktion. Beachten Sie, dass der alte Algorithmus erweiterte Funktionen wie Ersetzen mit Zeilenumbrüchen, Formatierung anwenden usw. nicht unterstützt.

 **Examples:** 

Zeigt, wie Substitutionen innerhalb von Ersetzungsmustern erkannt und verwendet werden.

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
boolean - Ein boolescher Wert, der angibt, dass der alte Suchen‑/Ersetzen‑Algorithmus verwendet wird.
### getMatchCase() {#getMatchCase}
```
public boolean getMatchCase()
```


True gibt einen fallabhängigen Vergleich an, false einen fallunabhängigen Vergleich.

 **Examples:** 

Zeigt, wie man die Groß-/Kleinschreibung bei einer Find‑and‑Replace‑Operation umschaltet.

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
boolean - Der entsprechende  boolean  Wert.
### getReplacementFormat() {#getReplacementFormat}
```
public int getReplacementFormat()
```


Gibt das Format der Ersetzung an. Standard ist [ReplacementFormat.TEXT](../../com.aspose.words/replacementformat/\#TEXT).

 **Remarks:** 

Hat nur Wirkung, wenn es in [Replacer](../../com.aspose.words/replacer/) verwendet wird.

**Returns:**
int - Der entsprechende int‑Wert. Der zurückgegebene Wert ist einer der Konstanten von [ReplacementFormat](../../com.aspose.words/replacementformat/).
### getReplacingCallback() {#getReplacingCallback}
```
public IReplacingCallback getReplacingCallback()
```


Die benutzerdefinierte Methode, die vor jedem Ersetzungsereignis aufgerufen wird.

 **Examples:** 

Zeigt, wie man alle Vorkommen eines regulären Ausdrucksmusters durch einen anderen String ersetzt und dabei alle solchen Ersetzungen nachverfolgt.

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

Zeigt, wie über FindReplaceOptions eine andere Schriftart auf neuen Inhalt angewendet wird.

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


Liefert oder setzt einen booleschen Wert, der angibt, ob ein Absatzumbruch ersetzt werden darf, wenn kein nachfolgender Geschwisterabsatz vorhanden ist.

Der Standardwert ist  false .

 **Remarks:** 

Diese Option ermöglicht das Ersetzen eines Absatzumbruchs, wenn kein nachfolgender Geschwisterabsatz existiert, zu dem alle Kindknoten verschoben werden können, indem ein beliebiger (nicht notwendigerweise Geschwister‑)Absatz nach dem zu ersetzenden Absatz gefunden wird.

 **Examples:** 

Zeigt, wie man einen Absatz aus einer Tabellenzelle mit einer verschachtelten Tabelle entfernt.

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
boolean - Der entsprechende  boolean  Wert.
### getUseLegacyOrder() {#getUseLegacyOrder}
```
public boolean getUseLegacyOrder()
```


True zeigt an, dass eine Textsuche sequenziell von oben nach unten unter Berücksichtigung der Textfelder durchgeführt wird. Der Standardwert ist  false .

 **Examples:** 

Zeigt, wie man die Suchreihenfolge von Knoten bei einer Suchen‑und‑Ersetzen‑Textoperation ändert.

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
boolean - Der entsprechende  boolean  Wert.
### getUseSubstitutions() {#getUseSubstitutions}
```
public boolean getUseSubstitutions()
```


Ermittelt einen booleschen Wert, der angibt, ob Substitutionen innerhalb von Ersetzungsmustern erkannt und verwendet werden sollen. Der Standardwert ist  false .

 **Remarks:** 

Weitere Details zu Substitutionselementen finden Sie unter: https://docs.microsoft.com/en-us/dotnet/standard/base-types/substitutions-in-regular-expressions.

 **Examples:** 

Zeigt, wie Substitutionen innerhalb von Ersetzungsmustern erkannt und verwendet werden.

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

Zeigt, wie man den Text mit Substitutionen ersetzt.

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
boolean - Ein boolescher Wert, der angibt, ob Ersetzungen innerhalb von Ersetzungsmustern erkannt und verwendet werden sollen.
### setDirection(int value) {#setDirection-int}
```
public void setDirection(int value)
```


Wählt die Richtung für das Ersetzen aus. Der Standardwert ist [FindReplaceDirection.FORWARD](../../com.aspose.words/findreplacedirection/\#FORWARD).

 **Examples:** 

Zeigt, wie ermittelt wird, in welcher Richtung ein Suchen‑und‑Ersetzen‑Vorgang das Dokument durchläuft.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Der entsprechende  int  Wert. Der Wert muss einer der [FindReplaceDirection](../../com.aspose.words/findreplacedirection/) Konstanten sein. |

### setFindWholeWordsOnly(boolean value) {#setFindWholeWordsOnly-boolean}
```
public void setFindWholeWordsOnly(boolean value)
```


True gibt an, dass oldValue ein eigenständiges Wort sein muss.

 **Examples:** 

Zeigt, wie man eigenständige Wort‑nur‑Find‑and‑Replace‑Operationen umschaltet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setIgnoreDeleted(boolean value) {#setIgnoreDeleted-boolean}
```
public void setIgnoreDeleted(boolean value)
```


Setzt einen booleschen Wert, der angibt, ob Text innerhalb von Löschrevisionen ignoriert werden soll. Der Standardwert ist  false .

 **Examples:** 

Zeigt, wie Text innerhalb von Löschrevisionen während eines Suchen‑und‑Ersetzen‑Vorgangs einbezogen oder ignoriert werden kann.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Ein boolescher Wert, der angibt, ob Text innerhalb von Löschrevisionen ignoriert werden soll. |

### setIgnoreFieldCodes(boolean value) {#setIgnoreFieldCodes-boolean}
```
public void setIgnoreFieldCodes(boolean value)
```


Setzt einen booleschen Wert, der angibt, ob Text innerhalb von Feldcodes ignoriert werden soll. Der Standardwert ist  false .

 **Remarks:** 

Diese Option wirkt sich nur auf Feldcodes aus (sie ignoriert keine Knoten zwischen [NodeType.FIELD\_SEPARATOR](../../com.aspose.words/nodetype/\#FIELD-SEPARATOR) und [NodeType.FIELD\_END](../../com.aspose.words/nodetype/\#FIELD-END)).

Um das gesamte Feld zu ignorieren, verwenden Sie bitte die entsprechende Option [getIgnoreFields()](../../com.aspose.words/findreplaceoptions/\#getIgnoreFields) / [setIgnoreFields(boolean)](../../com.aspose.words/findreplaceoptions/\#setIgnoreFields-boolean).

 **Examples:** 

Zeigt, wie Text innerhalb von Feldcodes ignoriert wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Ein boolescher Wert, der angibt, ob Text innerhalb von Feldcodes ignoriert werden soll. |

### setIgnoreFields(boolean value) {#setIgnoreFields-boolean}
```
public void setIgnoreFields(boolean value)
```


Setzt einen booleschen Wert, der angibt, ob Text innerhalb von Feldern ignoriert werden soll. Der Standardwert ist  false .

 **Remarks:** 

Diese Option wirkt sich auf das gesamte Feld aus (alle Knoten zwischen [NodeType.FIELD\_START](../../com.aspose.words/nodetype/\#FIELD-START) und [NodeType.FIELD\_END](../../com.aspose.words/nodetype/\#FIELD-END)).

Um nur Feldcodes zu ignorieren, verwenden Sie bitte die entsprechende Option [getIgnoreFieldCodes()](../../com.aspose.words/findreplaceoptions/\#getIgnoreFieldCodes) / [setIgnoreFieldCodes(boolean)](../../com.aspose.words/findreplaceoptions/\#setIgnoreFieldCodes-boolean).

 **Examples:** 

Zeigt, wie Text innerhalb von Feldern ignoriert wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Ein boolescher Wert, der angibt, ob Text innerhalb von Feldern ignoriert werden soll. |

### setIgnoreFootnotes(boolean value) {#setIgnoreFootnotes-boolean}
```
public void setIgnoreFootnotes(boolean value)
```


Setzt einen booleschen Wert, der angibt, ob Fußnoten ignoriert werden sollen. Der Standardwert ist  false .

 **Examples:** 

Zeigt, wie Fußnoten während eines Suchen‑und‑Ersetzen‑Vorgangs ignoriert werden.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Ein boolescher Wert, der angibt, ob Fußnoten ignoriert werden sollen. |

### setIgnoreInserted(boolean value) {#setIgnoreInserted-boolean}
```
public void setIgnoreInserted(boolean value)
```


Setzt einen booleschen Wert, der angibt, ob Text innerhalb von Einfüge‑Revisionen ignoriert werden soll. Der Standardwert ist  false .

 **Examples:** 

Zeigt, wie man Text innerhalb von Einfüge‑Revisionen während einer Suchen‑und‑Ersetzen‑Operation einbezieht oder ignoriert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Ein boolescher Wert, der angibt, ob Text innerhalb von Einfüge‑Revisionen ignoriert werden soll. |

### setIgnoreOfficeMath(boolean value) {#setIgnoreOfficeMath-boolean}
```
public void setIgnoreOfficeMath(boolean value)
```


Setzt einen booleschen Wert, der angibt, ob Text innerhalb von OfficeMath/> ignoriert werden soll. Der Standardwert ist  true .

 **Examples:** 

Zeigt, wie man Text innerhalb von OfficeMath findet und ersetzt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Ein boolescher Wert, der angibt, ob Text innerhalb von OfficeMath/> ignoriert werden soll. |

### setIgnoreShapes(boolean value) {#setIgnoreShapes-boolean}
```
public void setIgnoreShapes(boolean value)
```


Liefert oder setzt einen booleschen Wert, der angibt, ob Formen innerhalb eines Textes ignoriert werden sollen.

Der Standardwert ist  false .

 **Examples:** 

Zeigt, wie man Formen beim Ersetzen von Text ignoriert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setIgnoreStructuredDocumentTags(boolean value) {#setIgnoreStructuredDocumentTags-boolean}
```
public void setIgnoreStructuredDocumentTags(boolean value)
```


Setzt einen booleschen Wert, der angibt, ob der Inhalt von [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) ignoriert werden soll. Der Standardwert ist  false .

 **Remarks:** 

Wenn diese Option auf true gesetzt ist, wird der Inhalt von [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) als einfacher Text behandelt.

Andernfalls wird [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) als eigenständige Story verarbeitet und das Ersetzungsmuster wird für jedes [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) separat gesucht, sodass, wenn das Muster ein [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) überschreitet, die Ersetzung für ein solches Muster nicht durchgeführt wird.

 **Examples:** 

Zeigt, wie man den Inhalt von Tags bei der Ersetzung ignoriert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | boolean | Ein boolescher Wert, der angibt, ob der Inhalt von [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) ignoriert werden soll. |

### setLegacyMode(boolean value) {#setLegacyMode-boolean}
```
public void setLegacyMode(boolean value)
```


Setzt einen booleschen Wert, der angibt, dass der alte Such‑/Ersetzungsalgorithmus verwendet wird.

 **Remarks:** 

Verwenden Sie dieses Flag, wenn Sie exakt das gleiche Verhalten benötigen wie vor der Einführung der erweiterten Suchen‑/Ersetzen‑Funktion. Beachten Sie, dass der alte Algorithmus erweiterte Funktionen wie Ersetzen mit Zeilenumbrüchen, Formatierung anwenden usw. nicht unterstützt.

 **Examples:** 

Zeigt, wie Substitutionen innerhalb von Ersetzungsmustern erkannt und verwendet werden.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Ein boolescher Wert, der angibt, dass der alte Such‑/Ersetzungsalgorithmus verwendet wird. |

### setMatchCase(boolean value) {#setMatchCase-boolean}
```
public void setMatchCase(boolean value)
```


True gibt einen fallabhängigen Vergleich an, false einen fallunabhängigen Vergleich.

 **Examples:** 

Zeigt, wie man die Groß-/Kleinschreibung bei einer Find‑and‑Replace‑Operation umschaltet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setReplacementFormat(int value) {#setReplacementFormat-int}
```
public void setReplacementFormat(int value)
```


Gibt das Format der Ersetzung an. Standard ist [ReplacementFormat.TEXT](../../com.aspose.words/replacementformat/\#TEXT).

 **Remarks:** 

Hat nur Wirkung, wenn es in [Replacer](../../com.aspose.words/replacer/) verwendet wird.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Der entsprechende  int  Wert. Der Wert muss einer der [ReplacementFormat](../../com.aspose.words/replacementformat/) Konstanten sein. |

### setReplacingCallback(IReplacingCallback value) {#setReplacingCallback-com.aspose.words.IReplacingCallback}
```
public void setReplacingCallback(IReplacingCallback value)
```


Die benutzerdefinierte Methode, die vor jedem Ersetzungsereignis aufgerufen wird.

 **Examples:** 

Zeigt, wie man alle Vorkommen eines regulären Ausdrucksmusters durch einen anderen String ersetzt und dabei alle solchen Ersetzungen nachverfolgt.

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

Zeigt, wie über FindReplaceOptions eine andere Schriftart auf neuen Inhalt angewendet wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | [IReplacingCallback](../../com.aspose.words/ireplacingcallback/) | Der entsprechende [IReplacingCallback](../../com.aspose.words/ireplacingcallback/) Wert. |

### setSmartParagraphBreakReplacement(boolean value) {#setSmartParagraphBreakReplacement-boolean}
```
public void setSmartParagraphBreakReplacement(boolean value)
```


Liefert oder setzt einen booleschen Wert, der angibt, ob ein Absatzumbruch ersetzt werden darf, wenn kein nachfolgender Geschwisterabsatz vorhanden ist.

Der Standardwert ist  false .

 **Remarks:** 

Diese Option ermöglicht das Ersetzen eines Absatzumbruchs, wenn kein nachfolgender Geschwisterabsatz existiert, zu dem alle Kindknoten verschoben werden können, indem ein beliebiger (nicht notwendigerweise Geschwister‑)Absatz nach dem zu ersetzenden Absatz gefunden wird.

 **Examples:** 

Zeigt, wie man einen Absatz aus einer Tabellenzelle mit einer verschachtelten Tabelle entfernt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setUseLegacyOrder(boolean value) {#setUseLegacyOrder-boolean}
```
public void setUseLegacyOrder(boolean value)
```


True zeigt an, dass eine Textsuche sequenziell von oben nach unten unter Berücksichtigung der Textfelder durchgeführt wird. Der Standardwert ist  false .

 **Examples:** 

Zeigt, wie man die Suchreihenfolge von Knoten bei einer Suchen‑und‑Ersetzen‑Textoperation ändert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setUseSubstitutions(boolean value) {#setUseSubstitutions-boolean}
```
public void setUseSubstitutions(boolean value)
```


Setzt einen booleschen Wert, der angibt, ob Ersetzungen innerhalb von Ersetzungsmustern erkannt und verwendet werden sollen. Der Standardwert ist  false .

 **Remarks:** 

Weitere Details zu Substitutionselementen finden Sie unter: https://docs.microsoft.com/en-us/dotnet/standard/base-types/substitutions-in-regular-expressions.

 **Examples:** 

Zeigt, wie Substitutionen innerhalb von Ersetzungsmustern erkannt und verwendet werden.

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

Zeigt, wie man den Text mit Substitutionen ersetzt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Ein boolescher Wert, der angibt, ob Ersetzungen innerhalb von Ersetzungsmustern erkannt und verwendet werden sollen. |

