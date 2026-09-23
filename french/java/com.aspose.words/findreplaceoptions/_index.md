---
title: "FindReplaceOptions"
linktitle: "FindReplaceOptions"
second_title: "Aspose.Words pour Java"
description: "Spécifie les options pour les opérations de recherche/remplacement en Java."
type: docs
weight: 314
url: /fr/java/com.aspose.words/findreplaceoptions/
---

**Inheritance:**
java.lang.Object
```
public class FindReplaceOptions
```

Spécifie les options pour les opérations de recherche/remplacement.

Pour en savoir plus, consultez l'article de documentation [ Find and Replace ][Find and Replace].

 **Examples:** 

Montre comment activer/désactiver la sensibilité à la casse lors d'une opération de recherche-remplacement.

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

Montre comment activer/désactiver les opérations de recherche-remplacement uniquement sur des mots isolés.

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
## Constructors

| Constructor | Description |
| --- | --- |
| [FindReplaceOptions()](#FindReplaceOptions) | Initialise une nouvelle instance de la classe FindReplaceOptions avec les paramètres par défaut. |
| [FindReplaceOptions(int direction)](#FindReplaceOptions-int) | Initialise une nouvelle instance de cette classe. |
| [FindReplaceOptions(IReplacingCallback replacingCallback)](#FindReplaceOptions-com.aspose.words.IReplacingCallback) | Initialise une nouvelle instance de la classe FindReplaceOptions avec le rappel de remplacement spécifié. |
| [FindReplaceOptions(int direction, IReplacingCallback replacingCallback)](#FindReplaceOptions-int-com.aspose.words.IReplacingCallback) | Initialise une nouvelle instance de cette classe. |
## Méthodes

| Méthode | Description |
| --- | --- |
| [getApplyFont()](#getApplyFont) | Mise en forme du texte appliquée au nouveau contenu. |
| [getApplyParagraphFormat()](#getApplyParagraphFormat) | Mise en forme du paragraphe appliquée au nouveau contenu. |
| [getDirection()](#getDirection) | Sélectionne la direction du remplacement. |
| [getFindWholeWordsOnly()](#getFindWholeWordsOnly) | True indique que oldValue doit être un mot isolé. |
| [getIgnoreDeleted()](#getIgnoreDeleted) | Obtient une valeur booléenne indiquant s'il faut ignorer le texte à l'intérieur des révisions de suppression. |
| [getIgnoreFieldCodes()](#getIgnoreFieldCodes) | Obtient une valeur booléenne indiquant s'il faut ignorer le texte à l'intérieur des codes de champ. |
| [getIgnoreFields()](#getIgnoreFields) | Obtient une valeur booléenne indiquant s'il faut ignorer le texte à l'intérieur des champs. |
| [getIgnoreFootnotes()](#getIgnoreFootnotes) | Obtient une valeur booléenne indiquant s'il faut ignorer les notes de bas de page. |
| [getIgnoreInserted()](#getIgnoreInserted) | Obtient une valeur booléenne indiquant s'il faut ignorer le texte à l'intérieur des révisions d'insertion. |
| [getIgnoreOfficeMath()](#getIgnoreOfficeMath) | Obtient une valeur booléenne indiquant s'il faut ignorer le texte à l'intérieur d'OfficeMath/>. |
| [getIgnoreShapes()](#getIgnoreShapes) | Obtient ou définit une valeur booléenne indiquant s'il faut ignorer les formes dans un texte. |
| [getIgnoreStructuredDocumentTags()](#getIgnoreStructuredDocumentTags) | Obtient une valeur booléenne indiquant s'il faut ignorer le contenu de [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/). |
| [getLegacyMode()](#getLegacyMode) | Obtient une valeur booléenne indiquant que l'ancien algorithme de recherche/remplacement est utilisé. |
| [getMatchCase()](#getMatchCase) | True indique une comparaison sensible à la casse, false indique une comparaison insensible à la casse. |
| [getReplacementFormat()](#getReplacementFormat) | Spécifie le format du remplacement. |
| [getReplacingCallback()](#getReplacingCallback) | La méthode définie par l'utilisateur qui est appelée avant chaque occurrence de remplacement. |
| [getSmartParagraphBreakReplacement()](#getSmartParagraphBreakReplacement) | Obtient ou définit une valeur booléenne indiquant s'il est permis de remplacer le saut de paragraphe lorsqu'il n'y a pas de paragraphe frère suivant. |
| [getUseLegacyOrder()](#getUseLegacyOrder) | True indique qu'une recherche de texte est effectuée séquentiellement de haut en bas en tenant compte des zones de texte. |
| [getUseSubstitutions()](#getUseSubstitutions) | Obtient une valeur booléenne indiquant s'il faut reconnaître et utiliser les substitutions dans les modèles de remplacement. |
| [setDirection(int value)](#setDirection-int) | Sélectionne la direction du remplacement. |
| [setFindWholeWordsOnly(boolean value)](#setFindWholeWordsOnly-boolean) | True indique que oldValue doit être un mot isolé. |
| [setIgnoreDeleted(boolean value)](#setIgnoreDeleted-boolean) | Définit une valeur booléenne indiquant s'il faut ignorer le texte à l'intérieur des révisions de suppression. |
| [setIgnoreFieldCodes(boolean value)](#setIgnoreFieldCodes-boolean) | Définit une valeur booléenne indiquant s'il faut ignorer le texte à l'intérieur des codes de champ. |
| [setIgnoreFields(boolean value)](#setIgnoreFields-boolean) | Définit une valeur booléenne indiquant s'il faut ignorer le texte à l'intérieur des champs. |
| [setIgnoreFootnotes(boolean value)](#setIgnoreFootnotes-boolean) | Définit une valeur booléenne indiquant s'il faut ignorer les notes de bas de page. |
| [setIgnoreInserted(boolean value)](#setIgnoreInserted-boolean) | Définit une valeur booléenne indiquant s'il faut ignorer le texte à l'intérieur des révisions d'insertion. |
| [setIgnoreOfficeMath(boolean value)](#setIgnoreOfficeMath-boolean) | Définit une valeur booléenne indiquant s'il faut ignorer le texte à l'intérieur d'OfficeMath/>. |
| [setIgnoreShapes(boolean value)](#setIgnoreShapes-boolean) | Obtient ou définit une valeur booléenne indiquant s'il faut ignorer les formes dans un texte. |
| [setIgnoreStructuredDocumentTags(boolean value)](#setIgnoreStructuredDocumentTags-boolean) | Définit une valeur booléenne indiquant s'il faut ignorer le contenu de [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/). |
| [setLegacyMode(boolean value)](#setLegacyMode-boolean) | Définit une valeur booléenne indiquant que l'ancien algorithme de recherche/remplacement est utilisé. |
| [setMatchCase(boolean value)](#setMatchCase-boolean) | True indique une comparaison sensible à la casse, false indique une comparaison insensible à la casse. |
| [setReplacementFormat(int value)](#setReplacementFormat-int) | Spécifie le format du remplacement. |
| [setReplacingCallback(IReplacingCallback value)](#setReplacingCallback-com.aspose.words.IReplacingCallback) | La méthode définie par l'utilisateur qui est appelée avant chaque occurrence de remplacement. |
| [setSmartParagraphBreakReplacement(boolean value)](#setSmartParagraphBreakReplacement-boolean) | Obtient ou définit une valeur booléenne indiquant s'il est permis de remplacer le saut de paragraphe lorsqu'il n'y a pas de paragraphe frère suivant. |
| [setUseLegacyOrder(boolean value)](#setUseLegacyOrder-boolean) | True indique qu'une recherche de texte est effectuée séquentiellement de haut en bas en tenant compte des zones de texte. |
| [setUseSubstitutions(boolean value)](#setUseSubstitutions-boolean) | Définit une valeur booléenne indiquant s'il faut reconnaître et utiliser les substitutions dans les modèles de remplacement. |
### FindReplaceOptions() {#FindReplaceOptions}
```
public FindReplaceOptions()
```


Initialise une nouvelle instance de la classe FindReplaceOptions avec les paramètres par défaut.

 **Examples:** 

Montre comment reconnaître et utiliser les substitutions dans les modèles de remplacement.

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


Initialise une nouvelle instance de cette classe.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| direction | int |  |

### FindReplaceOptions(IReplacingCallback replacingCallback) {#FindReplaceOptions-com.aspose.words.IReplacingCallback}
```
public FindReplaceOptions(IReplacingCallback replacingCallback)
```


Initialise une nouvelle instance de la classe FindReplaceOptions avec le rappel de remplacement spécifié.

 **Examples:** 

Montre comment suivre l'ordre dans lequel une opération de remplacement de texte parcourt les nœuds.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| replacingCallback | [IReplacingCallback](../../com.aspose.words/ireplacingcallback/) | Le rappel à utiliser pour remplacer le texte trouvé. |

### FindReplaceOptions(int direction, IReplacingCallback replacingCallback) {#FindReplaceOptions-int-com.aspose.words.IReplacingCallback}
```
public FindReplaceOptions(int direction, IReplacingCallback replacingCallback)
```


Initialise une nouvelle instance de cette classe.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| direction | int |  |
| replacingCallback | [IReplacingCallback](../../com.aspose.words/ireplacingcallback/) |  |

### getApplyFont() {#getApplyFont}
```
public Font getApplyFont()
```


Mise en forme du texte appliquée au nouveau contenu.

 **Examples:** 

Montre comment appliquer une police différente au nouveau contenu via FindReplaceOptions.

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


Mise en forme du paragraphe appliquée au nouveau contenu.

 **Examples:** 

Montre comment ajouter du formatage aux paragraphes dans lesquels une opération de recherche-remplacement a trouvé des correspondances.

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


Sélectionne la direction du remplacement. La valeur par défaut est [FindReplaceDirection.FORWARD](../../com.aspose.words/findreplacedirection/\#FORWARD).

 **Examples:** 

Montre comment déterminer dans quelle direction une opération de recherche‑remplacement parcourt le document.

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
int - La valeur int correspondante. La valeur retournée est l'une des constantes [FindReplaceDirection](../../com.aspose.words/findreplacedirection/).
### getFindWholeWordsOnly() {#getFindWholeWordsOnly}
```
public boolean getFindWholeWordsOnly()
```


True indique que oldValue doit être un mot isolé.

 **Examples:** 

Montre comment activer/désactiver les opérations de recherche-remplacement uniquement sur des mots isolés.

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
boolean - La valeur  boolean  correspondante.
### getIgnoreDeleted() {#getIgnoreDeleted}
```
public boolean getIgnoreDeleted()
```


Obtient une valeur booléenne indiquant s'il faut ignorer le texte à l'intérieur des révisions de suppression. La valeur par défaut est false.

 **Examples:** 

Montre comment inclure ou ignorer le texte à l'intérieur des révisions de suppression lors d'une opération de recherche‑remplacement.

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
boolean - Une valeur booléenne indiquant s'il faut ignorer le texte à l'intérieur des révisions de suppression.
### getIgnoreFieldCodes() {#getIgnoreFieldCodes}
```
public boolean getIgnoreFieldCodes()
```


Obtient une valeur booléenne indiquant s'il faut ignorer le texte à l'intérieur des codes de champ. La valeur par défaut est false.

 **Remarks:** 

Cette option affecte uniquement les codes de champ (elle n'ignore pas les nœuds entre [NodeType.FIELD\_SEPARATOR](../../com.aspose.words/nodetype/\#FIELD-SEPARATOR) et [NodeType.FIELD\_END](../../com.aspose.words/nodetype/\#FIELD-END)).

Pour ignorer le champ entier, veuillez utiliser l'option correspondante [getIgnoreFields()](../../com.aspose.words/findreplaceoptions/\#getIgnoreFields) / [setIgnoreFields(boolean)](../../com.aspose.words/findreplaceoptions/\#setIgnoreFields-boolean).

 **Examples:** 

Montre comment ignorer le texte à l'intérieur des codes de champ.

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
boolean - Une valeur booléenne indiquant s'il faut ignorer le texte à l'intérieur des codes de champ.
### getIgnoreFields() {#getIgnoreFields}
```
public boolean getIgnoreFields()
```


Obtient une valeur booléenne indiquant s'il faut ignorer le texte à l'intérieur des champs. La valeur par défaut est false.

 **Remarks:** 

Cette option affecte le champ entier (tous les nœuds entre [NodeType.FIELD\_START](../../com.aspose.words/nodetype/\#FIELD-START) et [NodeType.FIELD\_END](../../com.aspose.words/nodetype/\#FIELD-END)).

Pour ignorer uniquement les codes de champ, veuillez utiliser l'option correspondante [getIgnoreFieldCodes()](../../com.aspose.words/findreplaceoptions/\#getIgnoreFieldCodes) / [setIgnoreFieldCodes(boolean)](../../com.aspose.words/findreplaceoptions/\#setIgnoreFieldCodes-boolean).

 **Examples:** 

Montre comment ignorer le texte à l'intérieur des champs.

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
boolean - Une valeur booléenne indiquant s'il faut ignorer le texte à l'intérieur des champs.
### getIgnoreFootnotes() {#getIgnoreFootnotes}
```
public boolean getIgnoreFootnotes()
```


Obtient une valeur booléenne indiquant s'il faut ignorer les notes de bas de page. La valeur par défaut est false.

 **Examples:** 

Montre comment ignorer les notes de bas de page lors d'une opération de recherche‑remplacement.

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
boolean - Une valeur booléenne indiquant s'il faut ignorer les notes de bas de page.
### getIgnoreInserted() {#getIgnoreInserted}
```
public boolean getIgnoreInserted()
```


Obtient une valeur booléenne indiquant s'il faut ignorer le texte à l'intérieur des révisions d'insertion. La valeur par défaut est false.

 **Examples:** 

Montre comment inclure ou ignorer le texte à l'intérieur des révisions d'insertion lors d'une opération de recherche‑remplacement.

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
boolean - Une valeur booléenne indiquant s'il faut ignorer le texte à l'intérieur des révisions d'insertion.
### getIgnoreOfficeMath() {#getIgnoreOfficeMath}
```
public boolean getIgnoreOfficeMath()
```


Obtient une valeur booléenne indiquant s'il faut ignorer le texte à l'intérieur d'OfficeMath/>. La valeur par défaut est true.

 **Examples:** 

Montre comment rechercher et remplacer du texte à l'intérieur d'OfficeMath.

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
boolean - Une valeur booléenne indiquant s'il faut ignorer le texte à l'intérieur d'OfficeMath/>.
### getIgnoreShapes() {#getIgnoreShapes}
```
public boolean getIgnoreShapes()
```


Obtient ou définit une valeur booléenne indiquant s'il faut ignorer les formes dans un texte.

La valeur par défaut est false.

 **Examples:** 

Montre comment ignorer les formes lors du remplacement du texte.

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
boolean - La valeur  boolean  correspondante.
### getIgnoreStructuredDocumentTags() {#getIgnoreStructuredDocumentTags}
```
public boolean getIgnoreStructuredDocumentTags()
```


Obtient une valeur booléenne indiquant s'il faut ignorer le contenu de [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/). La valeur par défaut est false.

 **Remarks:** 

Lorsque cette option est définie sur true, le contenu de [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) sera traité comme un texte simple.

Sinon, [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) sera traité comme une Story autonome et le modèle de remplacement sera recherché séparément pour chaque [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/), de sorte que si le modèle traverse un [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/), le remplacement ne sera pas effectué pour ce modèle.

 **Examples:** 

Montre comment ignorer le contenu des balises lors du remplacement.

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
booléen - Une valeur booléenne indiquant s'il faut ignorer le contenu de [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/).
### getLegacyMode() {#getLegacyMode}
```
public boolean getLegacyMode()
```


Obtient une valeur booléenne indiquant que l'ancien algorithme de recherche/remplacement est utilisé.

 **Remarks:** 

Utilisez ce drapeau si vous avez besoin exactement du même comportement qu'avant l'introduction de la fonction avancée de recherche/remplacement. Notez que l'ancien algorithme ne prend pas en charge les fonctionnalités avancées telles que le remplacement avec des sauts, l'application de formatage, etc.

 **Examples:** 

Montre comment reconnaître et utiliser les substitutions dans les modèles de remplacement.

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
booléen - Une valeur booléenne indiquant que l'ancien algorithme de recherche/remplacement est utilisé.
### getMatchCase() {#getMatchCase}
```
public boolean getMatchCase()
```


True indique une comparaison sensible à la casse, false indique une comparaison insensible à la casse.

 **Examples:** 

Montre comment activer/désactiver la sensibilité à la casse lors d'une opération de recherche-remplacement.

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
boolean - La valeur  boolean  correspondante.
### getReplacementFormat() {#getReplacementFormat}
```
public int getReplacementFormat()
```


Spécifie le format du remplacement. La valeur par défaut est [ReplacementFormat.TEXT](../../com.aspose.words/replacementformat/\#TEXT).

 **Remarks:** 

N'a d'effet que lors de l'utilisation dans [Replacer](../../com.aspose.words/replacer/)

**Returns:**
int - La valeur int correspondante. La valeur retournée est l'une des constantes [ReplacementFormat](../../com.aspose.words/replacementformat/).
### getReplacingCallback() {#getReplacingCallback}
```
public IReplacingCallback getReplacingCallback()
```


La méthode définie par l'utilisateur qui est appelée avant chaque occurrence de remplacement.

 **Examples:** 

Montre comment remplacer toutes les occurrences d'un modèle d'expression régulière par une autre chaîne, tout en suivant tous ces remplacements.

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

Montre comment appliquer une police différente au nouveau contenu via FindReplaceOptions.

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


Obtient ou définit une valeur booléenne indiquant s'il est permis de remplacer le saut de paragraphe lorsqu'il n'y a pas de paragraphe frère suivant.

La valeur par défaut est false.

 **Remarks:** 

Cette option permet de remplacer un saut de paragraphe lorsqu'il n'existe aucun paragraphe frère suivant auquel tous les nœuds enfants peuvent être déplacés, en trouvant tout paragraphe suivant (pas nécessairement frère) après le paragraphe à remplacer.

 **Examples:** 

Montre comment supprimer un paragraphe d'une cellule de tableau contenant un tableau imbriqué.

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
boolean - La valeur  boolean  correspondante.
### getUseLegacyOrder() {#getUseLegacyOrder}
```
public boolean getUseLegacyOrder()
```


True indique qu'une recherche de texte est effectuée séquentiellement de haut en bas en tenant compte des zones de texte. La valeur par défaut est false.

 **Examples:** 

Montre comment modifier l'ordre de recherche des nœuds lors d'une opération de recherche et remplacement de texte.

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
boolean - La valeur  boolean  correspondante.
### getUseSubstitutions() {#getUseSubstitutions}
```
public boolean getUseSubstitutions()
```


Obtient une valeur booléenne indiquant s'il faut reconnaître et utiliser les substitutions dans les modèles de remplacement. La valeur par défaut est false.

 **Remarks:** 

Pour les détails sur les éléments de substitution, veuillez vous référer à : https://docs.microsoft.com/en-us/dotnet/standard/base-types/substitutions-in-regular-expressions.

 **Examples:** 

Montre comment reconnaître et utiliser les substitutions dans les modèles de remplacement.

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

Montre comment remplacer le texte avec des substitutions.

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
booléen - Une valeur booléenne indiquant s'il faut reconnaître et utiliser les substitutions dans les modèles de remplacement.
### setDirection(int value) {#setDirection-int}
```
public void setDirection(int value)
```


Sélectionne la direction du remplacement. La valeur par défaut est [FindReplaceDirection.FORWARD](../../com.aspose.words/findreplacedirection/\#FORWARD).

 **Examples:** 

Montre comment déterminer dans quelle direction une opération de recherche‑remplacement parcourt le document.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | La valeur int correspondante. La valeur doit être l'une des constantes [FindReplaceDirection](../../com.aspose.words/findreplacedirection/). |

### setFindWholeWordsOnly(boolean value) {#setFindWholeWordsOnly-boolean}
```
public void setFindWholeWordsOnly(boolean value)
```


True indique que oldValue doit être un mot isolé.

 **Examples:** 

Montre comment activer/désactiver les opérations de recherche-remplacement uniquement sur des mots isolés.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | La valeur  boolean  correspondante. |

### setIgnoreDeleted(boolean value) {#setIgnoreDeleted-boolean}
```
public void setIgnoreDeleted(boolean value)
```


Définit une valeur booléenne indiquant s'il faut ignorer le texte à l'intérieur des révisions de suppression. La valeur par défaut est false.

 **Examples:** 

Montre comment inclure ou ignorer le texte à l'intérieur des révisions de suppression lors d'une opération de recherche‑remplacement.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | Une valeur booléenne indiquant s'il faut ignorer le texte à l'intérieur des révisions de suppression. |

### setIgnoreFieldCodes(boolean value) {#setIgnoreFieldCodes-boolean}
```
public void setIgnoreFieldCodes(boolean value)
```


Définit une valeur booléenne indiquant s'il faut ignorer le texte à l'intérieur des codes de champ. La valeur par défaut est false.

 **Remarks:** 

Cette option affecte uniquement les codes de champ (elle n'ignore pas les nœuds entre [NodeType.FIELD\_SEPARATOR](../../com.aspose.words/nodetype/\#FIELD-SEPARATOR) et [NodeType.FIELD\_END](../../com.aspose.words/nodetype/\#FIELD-END)).

Pour ignorer le champ entier, veuillez utiliser l'option correspondante [getIgnoreFields()](../../com.aspose.words/findreplaceoptions/\#getIgnoreFields) / [setIgnoreFields(boolean)](../../com.aspose.words/findreplaceoptions/\#setIgnoreFields-boolean).

 **Examples:** 

Montre comment ignorer le texte à l'intérieur des codes de champ.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | Une valeur booléenne indiquant s'il faut ignorer le texte à l'intérieur des codes de champ. |

### setIgnoreFields(boolean value) {#setIgnoreFields-boolean}
```
public void setIgnoreFields(boolean value)
```


Définit une valeur booléenne indiquant s'il faut ignorer le texte à l'intérieur des champs. La valeur par défaut est false.

 **Remarks:** 

Cette option affecte le champ entier (tous les nœuds entre [NodeType.FIELD\_START](../../com.aspose.words/nodetype/\#FIELD-START) et [NodeType.FIELD\_END](../../com.aspose.words/nodetype/\#FIELD-END)).

Pour ignorer uniquement les codes de champ, veuillez utiliser l'option correspondante [getIgnoreFieldCodes()](../../com.aspose.words/findreplaceoptions/\#getIgnoreFieldCodes) / [setIgnoreFieldCodes(boolean)](../../com.aspose.words/findreplaceoptions/\#setIgnoreFieldCodes-boolean).

 **Examples:** 

Montre comment ignorer le texte à l'intérieur des champs.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | Une valeur booléenne indiquant s'il faut ignorer le texte à l'intérieur des champs. |

### setIgnoreFootnotes(boolean value) {#setIgnoreFootnotes-boolean}
```
public void setIgnoreFootnotes(boolean value)
```


Définit une valeur booléenne indiquant s'il faut ignorer les notes de bas de page. La valeur par défaut est  false .

 **Examples:** 

Montre comment ignorer les notes de bas de page lors d'une opération de recherche‑remplacement.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | Une valeur booléenne indiquant s'il faut ignorer les notes de bas de page. |

### setIgnoreInserted(boolean value) {#setIgnoreInserted-boolean}
```
public void setIgnoreInserted(boolean value)
```


Définit une valeur booléenne indiquant s'il faut ignorer le texte dans les révisions d'insertion. La valeur par défaut est  false .

 **Examples:** 

Montre comment inclure ou ignorer le texte à l'intérieur des révisions d'insertion lors d'une opération de recherche‑remplacement.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | Une valeur booléenne indiquant s'il faut ignorer le texte dans les révisions d'insertion. |

### setIgnoreOfficeMath(boolean value) {#setIgnoreOfficeMath-boolean}
```
public void setIgnoreOfficeMath(boolean value)
```


Définit une valeur booléenne indiquant s'il faut ignorer le texte à l'intérieur de OfficeMath/>. La valeur par défaut est  true .

 **Examples:** 

Montre comment rechercher et remplacer du texte à l'intérieur d'OfficeMath.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | Une valeur booléenne indiquant s'il faut ignorer le texte à l'intérieur de OfficeMath/>. |

### setIgnoreShapes(boolean value) {#setIgnoreShapes-boolean}
```
public void setIgnoreShapes(boolean value)
```


Obtient ou définit une valeur booléenne indiquant s'il faut ignorer les formes dans un texte.

La valeur par défaut est false.

 **Examples:** 

Montre comment ignorer les formes lors du remplacement du texte.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | La valeur  boolean  correspondante. |

### setIgnoreStructuredDocumentTags(boolean value) {#setIgnoreStructuredDocumentTags-boolean}
```
public void setIgnoreStructuredDocumentTags(boolean value)
```


Définit une valeur booléenne indiquant s'il faut ignorer le contenu de [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/). La valeur par défaut est  false .

 **Remarks:** 

Lorsque cette option est définie sur true, le contenu de [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) sera traité comme un texte simple.

Sinon, [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) sera traité comme une Story autonome et le modèle de remplacement sera recherché séparément pour chaque [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/), de sorte que si le modèle traverse un [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/), le remplacement ne sera pas effectué pour ce modèle.

 **Examples:** 

Montre comment ignorer le contenu des balises lors du remplacement.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| value | boolean | Une valeur booléenne indiquant s'il faut ignorer le contenu de [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/). |

### setLegacyMode(boolean value) {#setLegacyMode-boolean}
```
public void setLegacyMode(boolean value)
```


Définit une valeur booléenne indiquant que l'ancien algorithme de recherche/remplacement est utilisé.

 **Remarks:** 

Utilisez ce drapeau si vous avez besoin exactement du même comportement qu'avant l'introduction de la fonction avancée de recherche/remplacement. Notez que l'ancien algorithme ne prend pas en charge les fonctionnalités avancées telles que le remplacement avec des sauts, l'application de formatage, etc.

 **Examples:** 

Montre comment reconnaître et utiliser les substitutions dans les modèles de remplacement.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | Une valeur booléenne indiquant que l'ancien algorithme de recherche/remplacement est utilisé. |

### setMatchCase(boolean value) {#setMatchCase-boolean}
```
public void setMatchCase(boolean value)
```


True indique une comparaison sensible à la casse, false indique une comparaison insensible à la casse.

 **Examples:** 

Montre comment activer/désactiver la sensibilité à la casse lors d'une opération de recherche-remplacement.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | La valeur  boolean  correspondante. |

### setReplacementFormat(int value) {#setReplacementFormat-int}
```
public void setReplacementFormat(int value)
```


Spécifie le format du remplacement. La valeur par défaut est [ReplacementFormat.TEXT](../../com.aspose.words/replacementformat/\#TEXT).

 **Remarks:** 

N'a d'effet que lors de l'utilisation dans [Replacer](../../com.aspose.words/replacer/)

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | La valeur  int  correspondante. La valeur doit être l'une des constantes [ReplacementFormat](../../com.aspose.words/replacementformat/). |

### setReplacingCallback(IReplacingCallback value) {#setReplacingCallback-com.aspose.words.IReplacingCallback}
```
public void setReplacingCallback(IReplacingCallback value)
```


La méthode définie par l'utilisateur qui est appelée avant chaque occurrence de remplacement.

 **Examples:** 

Montre comment remplacer toutes les occurrences d'un modèle d'expression régulière par une autre chaîne, tout en suivant tous ces remplacements.

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

Montre comment appliquer une police différente au nouveau contenu via FindReplaceOptions.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| value | [IReplacingCallback](../../com.aspose.words/ireplacingcallback/) | La valeur [IReplacingCallback](../../com.aspose.words/ireplacingcallback/) correspondante. |

### setSmartParagraphBreakReplacement(boolean value) {#setSmartParagraphBreakReplacement-boolean}
```
public void setSmartParagraphBreakReplacement(boolean value)
```


Obtient ou définit une valeur booléenne indiquant s'il est permis de remplacer le saut de paragraphe lorsqu'il n'y a pas de paragraphe frère suivant.

La valeur par défaut est false.

 **Remarks:** 

Cette option permet de remplacer un saut de paragraphe lorsqu'il n'existe aucun paragraphe frère suivant auquel tous les nœuds enfants peuvent être déplacés, en trouvant tout paragraphe suivant (pas nécessairement frère) après le paragraphe à remplacer.

 **Examples:** 

Montre comment supprimer un paragraphe d'une cellule de tableau contenant un tableau imbriqué.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | La valeur  boolean  correspondante. |

### setUseLegacyOrder(boolean value) {#setUseLegacyOrder-boolean}
```
public void setUseLegacyOrder(boolean value)
```


True indique qu'une recherche de texte est effectuée séquentiellement de haut en bas en tenant compte des zones de texte. La valeur par défaut est false.

 **Examples:** 

Montre comment modifier l'ordre de recherche des nœuds lors d'une opération de recherche et remplacement de texte.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | La valeur  boolean  correspondante. |

### setUseSubstitutions(boolean value) {#setUseSubstitutions-boolean}
```
public void setUseSubstitutions(boolean value)
```


Définit une valeur booléenne indiquant s'il faut reconnaître et utiliser les substitutions dans les modèles de remplacement. La valeur par défaut est  false .

 **Remarks:** 

Pour les détails sur les éléments de substitution, veuillez vous référer à : https://docs.microsoft.com/en-us/dotnet/standard/base-types/substitutions-in-regular-expressions.

 **Examples:** 

Montre comment reconnaître et utiliser les substitutions dans les modèles de remplacement.

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

Montre comment remplacer le texte avec des substitutions.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | Une valeur booléenne indiquant s'il faut reconnaître et utiliser les substitutions dans les modèles de remplacement. |

