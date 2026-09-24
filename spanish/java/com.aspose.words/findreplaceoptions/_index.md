---
title: "FindReplaceOptions"
linktitle: "FindReplaceOptions"
second_title: "Aspose.Words para Java"
description: "Especifica opciones para operaciones de buscar/reemplazar en Java."
type: docs
weight: 314
url: /es/java/com.aspose.words/findreplaceoptions/
---

**Inheritance:**
java.lang.Object
```
public class FindReplaceOptions
```

Especifica opciones para operaciones de buscar/reemplazar.

Para obtener más información, visite el artículo de documentación [ Find and Replace ][Find and Replace].

 **Examples:** 

Muestra cómo alternar la sensibilidad a mayúsculas y minúsculas al realizar una operación de buscar y reemplazar.

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

Muestra cómo alternar operaciones de buscar y reemplazar que solo afectan palabras independientes.

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
## Constructores

| Constructor | Descripción |
| --- | --- |
| [FindReplaceOptions()](#FindReplaceOptions) | Inicializa una nueva instancia de la clase FindReplaceOptions con la configuración predeterminada. |
| [FindReplaceOptions(int direction)](#FindReplaceOptions-int) | Inicializa una nueva instancia de esta clase. |
| [FindReplaceOptions(IReplacingCallback replacingCallback)](#FindReplaceOptions-com.aspose.words.IReplacingCallback) | Inicializa una nueva instancia de la clase FindReplaceOptions con la devolución de llamada de reemplazo especificada. |
| [FindReplaceOptions(int direction, IReplacingCallback replacingCallback)](#FindReplaceOptions-int-com.aspose.words.IReplacingCallback) | Inicializa una nueva instancia de esta clase. |
## Métodos

| Método | Descripción |
| --- | --- |
| [getApplyFont()](#getApplyFont) | Formato de texto aplicado al contenido nuevo. |
| [getApplyParagraphFormat()](#getApplyParagraphFormat) | Formato de párrafo aplicado al contenido nuevo. |
| [getDirection()](#getDirection) | Selecciona la dirección para reemplazar. |
| [getFindWholeWordsOnly()](#getFindWholeWordsOnly) | True indica que oldValue debe ser una palabra independiente. |
| [getIgnoreDeleted()](#getIgnoreDeleted) | Obtiene un valor booleano que indica si se debe ignorar el texto dentro de revisiones de eliminación. |
| [getIgnoreFieldCodes()](#getIgnoreFieldCodes) | Obtiene un valor booleano que indica si se debe ignorar el texto dentro de códigos de campo. |
| [getIgnoreFields()](#getIgnoreFields) | Obtiene un valor booleano que indica si se debe ignorar el texto dentro de campos. |
| [getIgnoreFootnotes()](#getIgnoreFootnotes) | Obtiene un valor booleano que indica si se debe ignorar las notas al pie. |
| [getIgnoreInserted()](#getIgnoreInserted) | Obtiene un valor booleano que indica si se debe ignorar el texto dentro de revisiones de inserción. |
| [getIgnoreOfficeMath()](#getIgnoreOfficeMath) | Obtiene un valor booleano que indica si se debe ignorar el texto dentro de OfficeMath/>. |
| [getIgnoreShapes()](#getIgnoreShapes) | Obtiene o establece un valor booleano que indica si se deben ignorar las formas dentro de un texto. |
| [getIgnoreStructuredDocumentTags()](#getIgnoreStructuredDocumentTags) | Obtiene un valor booleano que indica si se debe ignorar el contenido de [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/). |
| [getLegacyMode()](#getLegacyMode) | Obtiene un valor booleano que indica que se utiliza el algoritmo antiguo de buscar/reemplazar. |
| [getMatchCase()](#getMatchCase) | True indica una comparación sensible a mayúsculas y minúsculas, false indica una comparación que no distingue mayúsculas y minúsculas. |
| [getReplacementFormat()](#getReplacementFormat) | Especifica el formato del reemplazo. |
| [getReplacingCallback()](#getReplacingCallback) | El método definido por el usuario que se llama antes de cada aparición de reemplazo. |
| [getSmartParagraphBreakReplacement()](#getSmartParagraphBreakReplacement) | Obtiene o establece un valor booleano que indica si se permite reemplazar el salto de párrafo cuando no hay un párrafo hermano siguiente. |
| [getUseLegacyOrder()](#getUseLegacyOrder) | True indica que la búsqueda de texto se realiza secuencialmente de arriba a abajo considerando los cuadros de texto. |
| [getUseSubstitutions()](#getUseSubstitutions) | Obtiene un valor booleano que indica si se deben reconocer y usar sustituciones dentro de los patrones de reemplazo. |
| [setDirection(int value)](#setDirection-int) | Selecciona la dirección para reemplazar. |
| [setFindWholeWordsOnly(boolean value)](#setFindWholeWordsOnly-boolean) | True indica que oldValue debe ser una palabra independiente. |
| [setIgnoreDeleted(boolean value)](#setIgnoreDeleted-boolean) | Establece un valor booleano que indica si se debe ignorar el texto dentro de revisiones de eliminación. |
| [setIgnoreFieldCodes(boolean value)](#setIgnoreFieldCodes-boolean) | Establece un valor booleano que indica si se debe ignorar el texto dentro de códigos de campo. |
| [setIgnoreFields(boolean value)](#setIgnoreFields-boolean) | Establece un valor booleano que indica si se debe ignorar el texto dentro de campos. |
| [setIgnoreFootnotes(boolean value)](#setIgnoreFootnotes-boolean) | Establece un valor booleano que indica si se deben ignorar las notas al pie. |
| [setIgnoreInserted(boolean value)](#setIgnoreInserted-boolean) | Establece un valor booleano que indica si se debe ignorar el texto dentro de revisiones de inserción. |
| [setIgnoreOfficeMath(boolean value)](#setIgnoreOfficeMath-boolean) | Establece un valor booleano que indica si se debe ignorar el texto dentro de OfficeMath/>. |
| [setIgnoreShapes(boolean value)](#setIgnoreShapes-boolean) | Obtiene o establece un valor booleano que indica si se deben ignorar las formas dentro de un texto. |
| [setIgnoreStructuredDocumentTags(boolean value)](#setIgnoreStructuredDocumentTags-boolean) | Establece un valor booleano que indica si se debe ignorar el contenido de [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/). |
| [setLegacyMode(boolean value)](#setLegacyMode-boolean) | Establece un valor booleano que indica que se utiliza el algoritmo antiguo de buscar/reemplazar. |
| [setMatchCase(boolean value)](#setMatchCase-boolean) | True indica una comparación sensible a mayúsculas y minúsculas, false indica una comparación que no distingue mayúsculas y minúsculas. |
| [setReplacementFormat(int value)](#setReplacementFormat-int) | Especifica el formato del reemplazo. |
| [setReplacingCallback(IReplacingCallback value)](#setReplacingCallback-com.aspose.words.IReplacingCallback) | El método definido por el usuario que se llama antes de cada aparición de reemplazo. |
| [setSmartParagraphBreakReplacement(boolean value)](#setSmartParagraphBreakReplacement-boolean) | Obtiene o establece un valor booleano que indica si se permite reemplazar el salto de párrafo cuando no hay un párrafo hermano siguiente. |
| [setUseLegacyOrder(boolean value)](#setUseLegacyOrder-boolean) | True indica que la búsqueda de texto se realiza secuencialmente de arriba a abajo considerando los cuadros de texto. |
| [setUseSubstitutions(boolean value)](#setUseSubstitutions-boolean) | Establece un valor booleano que indica si se deben reconocer y usar sustituciones dentro de los patrones de reemplazo. |
### FindReplaceOptions() {#FindReplaceOptions}
```
public FindReplaceOptions()
```


Inicializa una nueva instancia de la clase FindReplaceOptions con la configuración predeterminada.

 **Examples:** 

Muestra cómo reconocer y usar sustituciones dentro de los patrones de reemplazo.

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


Inicializa una nueva instancia de esta clase.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| direction | int |  |

### FindReplaceOptions(IReplacingCallback replacingCallback) {#FindReplaceOptions-com.aspose.words.IReplacingCallback}
```
public FindReplaceOptions(IReplacingCallback replacingCallback)
```


Inicializa una nueva instancia de la clase FindReplaceOptions con la devolución de llamada de reemplazo especificada.

 **Examples:** 

Muestra cómo rastrear el orden en que una operación de reemplazo de texto recorre los nodos.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| replacingCallback | [IReplacingCallback](../../com.aspose.words/ireplacingcallback/) | La función de devolución de llamada a usar para reemplazar el texto encontrado. |

### FindReplaceOptions(int direction, IReplacingCallback replacingCallback) {#FindReplaceOptions-int-com.aspose.words.IReplacingCallback}
```
public FindReplaceOptions(int direction, IReplacingCallback replacingCallback)
```


Inicializa una nueva instancia de esta clase.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| direction | int |  |
| replacingCallback | [IReplacingCallback](../../com.aspose.words/ireplacingcallback/) |  |

### getApplyFont() {#getApplyFont}
```
public Font getApplyFont()
```


Formato de texto aplicado al contenido nuevo.

 **Examples:** 

Muestra cómo aplicar una fuente diferente al contenido nuevo mediante FindReplaceOptions.

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


Formato de párrafo aplicado al contenido nuevo.

 **Examples:** 

Muestra cómo agregar formato a los párrafos en los que una operación de buscar y reemplazar ha encontrado coincidencias.

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


Selecciona la dirección para el reemplazo. El valor predeterminado es [FindReplaceDirection.FORWARD](../../com.aspose.words/findreplacedirection/\#FORWARD).

 **Examples:** 

Muestra cómo determinar en qué dirección recorre el documento una operación de buscar y reemplazar.

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
int - El valor int correspondiente. El valor devuelto es una de las constantes [FindReplaceDirection](../../com.aspose.words/findreplacedirection/).
### getFindWholeWordsOnly() {#getFindWholeWordsOnly}
```
public boolean getFindWholeWordsOnly()
```


True indica que oldValue debe ser una palabra independiente.

 **Examples:** 

Muestra cómo alternar operaciones de buscar y reemplazar que solo afectan palabras independientes.

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
boolean - El valor  boolean  correspondiente.
### getIgnoreDeleted() {#getIgnoreDeleted}
```
public boolean getIgnoreDeleted()
```


Obtiene un valor booleano que indica si se debe ignorar el texto dentro de revisiones de eliminación. El valor predeterminado es false.

 **Examples:** 

Muestra cómo incluir o ignorar el texto dentro de revisiones de eliminación durante una operación de buscar y reemplazar.

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
boolean - Un valor booleano que indica si se debe ignorar el texto dentro de revisiones de eliminación.
### getIgnoreFieldCodes() {#getIgnoreFieldCodes}
```
public boolean getIgnoreFieldCodes()
```


Obtiene un valor booleano que indica si se debe ignorar el texto dentro de códigos de campo. El valor predeterminado es false.

 **Remarks:** 

Esta opción afecta solo a los códigos de campo (no ignora los nodos entre [NodeType.FIELD\_SEPARATOR](../../com.aspose.words/nodetype/\#FIELD-SEPARATOR) y [NodeType.FIELD\_END](../../com.aspose.words/nodetype/\#FIELD-END)).

Para ignorar todo el campo, utilice la opción correspondiente [getIgnoreFields()](../../com.aspose.words/findreplaceoptions/\#getIgnoreFields) / [setIgnoreFields(boolean)](../../com.aspose.words/findreplaceoptions/\#setIgnoreFields-boolean).

 **Examples:** 

Muestra cómo ignorar el texto dentro de códigos de campo.

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
boolean - Un valor booleano que indica si se debe ignorar el texto dentro de códigos de campo.
### getIgnoreFields() {#getIgnoreFields}
```
public boolean getIgnoreFields()
```


Obtiene un valor booleano que indica si se deben ignorar los campos. El valor predeterminado es false.

 **Remarks:** 

Esta opción afecta a todo el campo (todos los nodos entre [NodeType.FIELD\_START](../../com.aspose.words/nodetype/\#FIELD-START) y [NodeType.FIELD\_END](../../com.aspose.words/nodetype/\#FIELD-END)).

Para ignorar solo los códigos de campo, utilice la opción correspondiente [getIgnoreFieldCodes()](../../com.aspose.words/findreplaceoptions/\#getIgnoreFieldCodes) / [setIgnoreFieldCodes(boolean)](../../com.aspose.words/findreplaceoptions/\#setIgnoreFieldCodes-boolean).

 **Examples:** 

Muestra cómo ignorar el texto dentro de los campos.

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
boolean - Un valor booleano que indica si se debe ignorar el texto dentro de los campos.
### getIgnoreFootnotes() {#getIgnoreFootnotes}
```
public boolean getIgnoreFootnotes()
```


Obtiene un valor booleano que indica si se deben ignorar las notas al pie. El valor predeterminado es false.

 **Examples:** 

Muestra cómo ignorar las notas al pie durante una operación de buscar y reemplazar.

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
boolean - Un valor booleano que indica si se deben ignorar las notas al pie.
### getIgnoreInserted() {#getIgnoreInserted}
```
public boolean getIgnoreInserted()
```


Obtiene un valor booleano que indica si se debe ignorar el texto dentro de revisiones de inserción. El valor predeterminado es false.

 **Examples:** 

Muestra cómo incluir o ignorar el texto dentro de revisiones de inserción durante una operación de buscar y reemplazar.

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
boolean - Un valor booleano que indica si se debe ignorar el texto dentro de revisiones de inserción.
### getIgnoreOfficeMath() {#getIgnoreOfficeMath}
```
public boolean getIgnoreOfficeMath()
```


Obtiene un valor booleano que indica si se debe ignorar el texto dentro de OfficeMath/>. El valor predeterminado es true.

 **Examples:** 

Muestra cómo buscar y reemplazar texto dentro de OfficeMath.

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
boolean - Un valor booleano que indica si se debe ignorar el texto dentro de OfficeMath/>.
### getIgnoreShapes() {#getIgnoreShapes}
```
public boolean getIgnoreShapes()
```


Obtiene o establece un valor booleano que indica si se deben ignorar las formas dentro de un texto.

El valor predeterminado es  false .

 **Examples:** 

Muestra cómo ignorar formas al reemplazar texto.

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
boolean - El valor  boolean  correspondiente.
### getIgnoreStructuredDocumentTags() {#getIgnoreStructuredDocumentTags}
```
public boolean getIgnoreStructuredDocumentTags()
```


Obtiene un valor booleano que indica si se debe ignorar el contenido de [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/). El valor predeterminado es false.

 **Remarks:** 

Cuando esta opción se establece en true, el contenido de [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) se tratará como texto simple.

De lo contrario, [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) se procesará como una historia independiente y el patrón de reemplazo se buscará por separado para cada [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/), de modo que si el patrón cruza un [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/), entonces no se realizará el reemplazo para ese patrón.

 **Examples:** 

Muestra cómo ignorar el contenido de las etiquetas durante el reemplazo.

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
boolean - Un valor booleano que indica si se debe ignorar el contenido de [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/).
### getLegacyMode() {#getLegacyMode}
```
public boolean getLegacyMode()
```


Obtiene un valor booleano que indica que se utiliza el algoritmo antiguo de buscar/reemplazar.

 **Remarks:** 

Utilice esta bandera si necesita exactamente el mismo comportamiento que antes de que se introdujera la función avanzada de búsqueda/reemplazo. Tenga en cuenta que el algoritmo antiguo no admite funciones avanzadas como reemplazar con saltos, aplicar formato, etc.

 **Examples:** 

Muestra cómo reconocer y usar sustituciones dentro de los patrones de reemplazo.

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
boolean - Un valor booleano que indica que se utiliza el algoritmo antiguo de búsqueda/reemplazo.
### getMatchCase() {#getMatchCase}
```
public boolean getMatchCase()
```


True indica una comparación sensible a mayúsculas y minúsculas, false indica una comparación que no distingue mayúsculas y minúsculas.

 **Examples:** 

Muestra cómo alternar la sensibilidad a mayúsculas y minúsculas al realizar una operación de buscar y reemplazar.

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
boolean - El valor  boolean  correspondiente.
### getReplacementFormat() {#getReplacementFormat}
```
public int getReplacementFormat()
```


Especifica el formato del reemplazo. El valor predeterminado es [ReplacementFormat.TEXT](../../com.aspose.words/replacementformat/\#TEXT).

 **Remarks:** 

Tiene efecto solo al usar en [Replacer](../../com.aspose.words/replacer/)

**Returns:**
int - El valor int correspondiente. El valor devuelto es una de las constantes de [ReplacementFormat](../../com.aspose.words/replacementformat/).
### getReplacingCallback() {#getReplacingCallback}
```
public IReplacingCallback getReplacingCallback()
```


El método definido por el usuario que se llama antes de cada aparición de reemplazo.

 **Examples:** 

Muestra cómo reemplazar todas las ocurrencias de un patrón de expresión regular con otra cadena, mientras se rastrean todos esos reemplazos.

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

Muestra cómo aplicar una fuente diferente al contenido nuevo mediante FindReplaceOptions.

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


Obtiene o establece un valor booleano que indica si se permite reemplazar el salto de párrafo cuando no hay un párrafo hermano siguiente.

El valor predeterminado es  false .

 **Remarks:** 

Esta opción permite reemplazar el salto de párrafo cuando no hay un párrafo hermano siguiente al que se puedan mover todos los nodos hijos, encontrando cualquier párrafo siguiente (no necesariamente hermano) después del párrafo que se está reemplazando.

 **Examples:** 

Muestra cómo eliminar un párrafo de una celda de tabla con una tabla anidada.

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
boolean - El valor  boolean  correspondiente.
### getUseLegacyOrder() {#getUseLegacyOrder}
```
public boolean getUseLegacyOrder()
```


True indica que una búsqueda de texto se realiza secuencialmente de arriba a abajo considerando los cuadros de texto. El valor predeterminado es false.

 **Examples:** 

Muestra cómo cambiar el orden de búsqueda de nodos al realizar una operación de buscar y reemplazar texto.

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
boolean - El valor  boolean  correspondiente.
### getUseSubstitutions() {#getUseSubstitutions}
```
public boolean getUseSubstitutions()
```


Obtiene un valor booleano que indica si se deben reconocer y usar sustituciones dentro de los patrones de reemplazo. El valor predeterminado es false.

 **Remarks:** 

Para obtener detalles sobre los elementos de sustitución, consulte: https://docs.microsoft.com/en-us/dotnet/standard/base-types/substitutions-in-regular-expressions.

 **Examples:** 

Muestra cómo reconocer y usar sustituciones dentro de los patrones de reemplazo.

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

Muestra cómo reemplazar el texto con sustituciones.

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
boolean - Un valor booleano que indica si se deben reconocer y usar sustituciones dentro de los patrones de reemplazo.
### setDirection(int value) {#setDirection-int}
```
public void setDirection(int value)
```


Selecciona la dirección para el reemplazo. El valor predeterminado es [FindReplaceDirection.FORWARD](../../com.aspose.words/findreplacedirection/\#FORWARD).

 **Examples:** 

Muestra cómo determinar en qué dirección recorre el documento una operación de buscar y reemplazar.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El valor int correspondiente. El valor debe ser una de las constantes de [FindReplaceDirection](../../com.aspose.words/findreplacedirection/). |

### setFindWholeWordsOnly(boolean value) {#setFindWholeWordsOnly-boolean}
```
public void setFindWholeWordsOnly(boolean value)
```


True indica que oldValue debe ser una palabra independiente.

 **Examples:** 

Muestra cómo alternar operaciones de buscar y reemplazar que solo afectan palabras independientes.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setIgnoreDeleted(boolean value) {#setIgnoreDeleted-boolean}
```
public void setIgnoreDeleted(boolean value)
```


Establece un valor booleano que indica si se debe ignorar el texto dentro de revisiones de eliminación. El valor predeterminado es false.

 **Examples:** 

Muestra cómo incluir o ignorar el texto dentro de revisiones de eliminación durante una operación de buscar y reemplazar.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | Un valor booleano que indica si se debe ignorar el texto dentro de revisiones de eliminación. |

### setIgnoreFieldCodes(boolean value) {#setIgnoreFieldCodes-boolean}
```
public void setIgnoreFieldCodes(boolean value)
```


Establece un valor booleano que indica si se debe ignorar el texto dentro de códigos de campo. El valor predeterminado es false.

 **Remarks:** 

Esta opción afecta solo a los códigos de campo (no ignora los nodos entre [NodeType.FIELD\_SEPARATOR](../../com.aspose.words/nodetype/\#FIELD-SEPARATOR) y [NodeType.FIELD\_END](../../com.aspose.words/nodetype/\#FIELD-END)).

Para ignorar todo el campo, utilice la opción correspondiente [getIgnoreFields()](../../com.aspose.words/findreplaceoptions/\#getIgnoreFields) / [setIgnoreFields(boolean)](../../com.aspose.words/findreplaceoptions/\#setIgnoreFields-boolean).

 **Examples:** 

Muestra cómo ignorar el texto dentro de códigos de campo.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | Un valor booleano que indica si se debe ignorar el texto dentro de códigos de campo. |

### setIgnoreFields(boolean value) {#setIgnoreFields-boolean}
```
public void setIgnoreFields(boolean value)
```


Establece un valor booleano que indica si se debe ignorar el texto dentro de campos. El valor predeterminado es false.

 **Remarks:** 

Esta opción afecta a todo el campo (todos los nodos entre [NodeType.FIELD\_START](../../com.aspose.words/nodetype/\#FIELD-START) y [NodeType.FIELD\_END](../../com.aspose.words/nodetype/\#FIELD-END)).

Para ignorar solo los códigos de campo, utilice la opción correspondiente [getIgnoreFieldCodes()](../../com.aspose.words/findreplaceoptions/\#getIgnoreFieldCodes) / [setIgnoreFieldCodes(boolean)](../../com.aspose.words/findreplaceoptions/\#setIgnoreFieldCodes-boolean).

 **Examples:** 

Muestra cómo ignorar el texto dentro de los campos.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | Un valor booleano que indica si se debe ignorar el texto dentro de los campos. |

### setIgnoreFootnotes(boolean value) {#setIgnoreFootnotes-boolean}
```
public void setIgnoreFootnotes(boolean value)
```


Establece un valor booleano que indica si se deben ignorar las notas al pie. El valor predeterminado es false.

 **Examples:** 

Muestra cómo ignorar las notas al pie durante una operación de buscar y reemplazar.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | Un valor booleano que indica si se deben ignorar las notas al pie. |

### setIgnoreInserted(boolean value) {#setIgnoreInserted-boolean}
```
public void setIgnoreInserted(boolean value)
```


Establece un valor booleano que indica si se debe ignorar el texto dentro de las revisiones de inserción. El valor predeterminado es false.

 **Examples:** 

Muestra cómo incluir o ignorar el texto dentro de revisiones de inserción durante una operación de buscar y reemplazar.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | Un valor booleano que indica si se debe ignorar el texto dentro de las revisiones de inserción. |

### setIgnoreOfficeMath(boolean value) {#setIgnoreOfficeMath-boolean}
```
public void setIgnoreOfficeMath(boolean value)
```


Establece un valor booleano que indica si se debe ignorar el texto dentro de OfficeMath/>. El valor predeterminado es true.

 **Examples:** 

Muestra cómo buscar y reemplazar texto dentro de OfficeMath.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | Un valor booleano que indica si se debe ignorar el texto dentro de OfficeMath/>. |

### setIgnoreShapes(boolean value) {#setIgnoreShapes-boolean}
```
public void setIgnoreShapes(boolean value)
```


Obtiene o establece un valor booleano que indica si se deben ignorar las formas dentro de un texto.

El valor predeterminado es  false .

 **Examples:** 

Muestra cómo ignorar formas al reemplazar texto.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setIgnoreStructuredDocumentTags(boolean value) {#setIgnoreStructuredDocumentTags-boolean}
```
public void setIgnoreStructuredDocumentTags(boolean value)
```


Establece un valor booleano que indica si se debe ignorar el contenido de [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/). El valor predeterminado es false.

 **Remarks:** 

Cuando esta opción se establece en true, el contenido de [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) se tratará como texto simple.

De lo contrario, [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) se procesará como una historia independiente y el patrón de reemplazo se buscará por separado para cada [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/), de modo que si el patrón cruza un [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/), entonces no se realizará el reemplazo para ese patrón.

 **Examples:** 

Muestra cómo ignorar el contenido de las etiquetas durante el reemplazo.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | boolean | Un valor booleano que indica si se debe ignorar el contenido de [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/). |

### setLegacyMode(boolean value) {#setLegacyMode-boolean}
```
public void setLegacyMode(boolean value)
```


Establece un valor booleano que indica que se utiliza el algoritmo antiguo de buscar/reemplazar.

 **Remarks:** 

Utilice esta bandera si necesita exactamente el mismo comportamiento que antes de que se introdujera la función avanzada de búsqueda/reemplazo. Tenga en cuenta que el algoritmo antiguo no admite funciones avanzadas como reemplazar con saltos, aplicar formato, etc.

 **Examples:** 

Muestra cómo reconocer y usar sustituciones dentro de los patrones de reemplazo.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | Un valor booleano que indica que se utiliza el algoritmo antiguo de buscar/reemplazar. |

### setMatchCase(boolean value) {#setMatchCase-boolean}
```
public void setMatchCase(boolean value)
```


True indica una comparación sensible a mayúsculas y minúsculas, false indica una comparación que no distingue mayúsculas y minúsculas.

 **Examples:** 

Muestra cómo alternar la sensibilidad a mayúsculas y minúsculas al realizar una operación de buscar y reemplazar.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setReplacementFormat(int value) {#setReplacementFormat-int}
```
public void setReplacementFormat(int value)
```


Especifica el formato del reemplazo. El valor predeterminado es [ReplacementFormat.TEXT](../../com.aspose.words/replacementformat/\#TEXT).

 **Remarks:** 

Tiene efecto solo al usar en [Replacer](../../com.aspose.words/replacer/)

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El valor int correspondiente. El valor debe ser una de las constantes de [ReplacementFormat](../../com.aspose.words/replacementformat/). |

### setReplacingCallback(IReplacingCallback value) {#setReplacingCallback-com.aspose.words.IReplacingCallback}
```
public void setReplacingCallback(IReplacingCallback value)
```


El método definido por el usuario que se llama antes de cada aparición de reemplazo.

 **Examples:** 

Muestra cómo reemplazar todas las ocurrencias de un patrón de expresión regular con otra cadena, mientras se rastrean todos esos reemplazos.

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

Muestra cómo aplicar una fuente diferente al contenido nuevo mediante FindReplaceOptions.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | [IReplacingCallback](../../com.aspose.words/ireplacingcallback/) | El valor correspondiente de [IReplacingCallback](../../com.aspose.words/ireplacingcallback/). |

### setSmartParagraphBreakReplacement(boolean value) {#setSmartParagraphBreakReplacement-boolean}
```
public void setSmartParagraphBreakReplacement(boolean value)
```


Obtiene o establece un valor booleano que indica si se permite reemplazar el salto de párrafo cuando no hay un párrafo hermano siguiente.

El valor predeterminado es  false .

 **Remarks:** 

Esta opción permite reemplazar el salto de párrafo cuando no hay un párrafo hermano siguiente al que se puedan mover todos los nodos hijos, encontrando cualquier párrafo siguiente (no necesariamente hermano) después del párrafo que se está reemplazando.

 **Examples:** 

Muestra cómo eliminar un párrafo de una celda de tabla con una tabla anidada.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setUseLegacyOrder(boolean value) {#setUseLegacyOrder-boolean}
```
public void setUseLegacyOrder(boolean value)
```


True indica que una búsqueda de texto se realiza secuencialmente de arriba a abajo considerando los cuadros de texto. El valor predeterminado es false.

 **Examples:** 

Muestra cómo cambiar el orden de búsqueda de nodos al realizar una operación de buscar y reemplazar texto.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setUseSubstitutions(boolean value) {#setUseSubstitutions-boolean}
```
public void setUseSubstitutions(boolean value)
```


Establece un valor booleano que indica si se deben reconocer y usar sustituciones dentro de los patrones de reemplazo. El valor predeterminado es false.

 **Remarks:** 

Para obtener detalles sobre los elementos de sustitución, consulte: https://docs.microsoft.com/en-us/dotnet/standard/base-types/substitutions-in-regular-expressions.

 **Examples:** 

Muestra cómo reconocer y usar sustituciones dentro de los patrones de reemplazo.

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

Muestra cómo reemplazar el texto con sustituciones.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | Un valor booleano que indica si se deben reconocer y usar sustituciones dentro de los patrones de reemplazo. |

