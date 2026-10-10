---
title: "ReplacingArgs"
linktitle: "ReplacingArgs"
second_title: "Aspose.Words für Java"
description: "Stellt Daten für eine benutzerdefinierte Ersetzungsoperation in Java bereit."
type: docs
weight: 569
url: /de/java/com.aspose.words/replacingargs/
---

**Inheritance:**
java.lang.Object
```
public class ReplacingArgs
```

Stellt Daten für einen benutzerdefinierten Ersetzungsvorgang bereit.

Um mehr zu erfahren, besuchen Sie den [ Find and Replace ][Find and Replace] Dokumentationsartikel.

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

Zeigt, wie der gesamte Inhalt eines Dokuments als Ersatz für eine Übereinstimmung in einer Suchen‑und‑Ersetzen‑Operation eingefügt wird.

```

 public void insertDocumentAtReplace() throws Exception {
     Document mainDoc = new Document(getMyDir() + "Document insertion destination.docx");

     // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
     FindReplaceOptions options = new FindReplaceOptions();
     options.setReplacingCallback(new InsertDocumentAtReplaceHandler());

     mainDoc.getRange().replace(Pattern.compile("\[MY_DOCUMENT\]"), "", options);
     mainDoc.save(getArtifactsDir() + "InsertDocument.InsertDocumentAtReplace.docx");

 }

 private static class InsertDocumentAtReplaceHandler implements IReplacingCallback {
     public int replacing(ReplacingArgs args) throws Exception {
         Document subDoc = new Document(getMyDir() + "Document.docx");

         // Insert a document after the paragraph containing the matched text.
         Paragraph para = (Paragraph) args.getMatchNode().getParentNode();
         insertDocument(para, subDoc);

         // Remove the paragraph with the matched text.
         para.remove();

         return ReplaceAction.SKIP;
     }
 }

 /// 
 /// Inserts all the nodes of another document after a paragraph or table.
 /// 
 private static void insertDocument(Node insertionDestination, Document docToInsert) {
     if (((insertionDestination.getNodeType()) == (NodeType.PARAGRAPH)) || ((insertionDestination.getNodeType()) == (NodeType.TABLE))) {
         CompositeNode dstStory = insertionDestination.getParentNode();

         NodeImporter importer =
                 new NodeImporter(docToInsert, insertionDestination.getDocument(), ImportFormatMode.KEEP_SOURCE_FORMATTING);

         for (Section srcSection : docToInsert.getSections())
             for (Node srcNode : srcSection.getBody()) {
                 // Skip the node if it is the last empty paragraph in a section.
                 if (((srcNode.getNodeType()) == (NodeType.PARAGRAPH))) {
                     Paragraph para = (Paragraph) srcNode;
                     if (para.isEndOfSection() && !para.hasChildNodes())
                         continue;
                 }

                 Node newNode = importer.importNode(srcNode, true);

                 dstStory.insertAfter(newNode, insertionDestination);
                 insertionDestination = newNode;
             }
     } else {
         throw new IllegalArgumentException("The destination node must be either a paragraph or table.");
     }
 }
 
```


[Find and Replace]: https://docs.aspose.com/words/java/find-and-replace/
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getGroupIndex()](#getGroupIndex) | Identifiziert, nach Index, eine erfasste Gruppe in der [getMatch()](../../com.aspose.words/replacingargs/\#getMatch), die durch die Zeichenkette aus [getReplacement()](../../com.aspose.words/replacingargs/\#getReplacement) / [setReplacement(java.lang.String)](../../com.aspose.words/replacingargs/\#setReplacement-java.lang.String) ersetzt werden soll. |
| [getMatch()](#getMatch) | Der java.util.regex.Matcher, der aus einem einzelnen regulären Ausdrucks-Match während einer **Replace** resultiert. |
| [getMatchEndNode()](#getMatchEndNode) | Liefert den Knoten, der das Ende der Übereinstimmung enthält. |
| [getMatchNode()](#getMatchNode) | Liefert den Knoten, der den Anfang der Übereinstimmung enthält. |
| [getMatchOffset()](#getMatchOffset) | Liefert die nullbasierte Startposition der Übereinstimmung ab dem Beginn des Knotens, der den Anfang der Übereinstimmung enthält. |
| [getReplacement()](#getReplacement) | Liefert die Ersetzungszeichenfolge. |
| [setGroupIndex(int value)](#setGroupIndex-int) | Identifiziert, nach Index, eine erfasste Gruppe in der [getMatch()](../../com.aspose.words/replacingargs/\#getMatch), die durch die Zeichenkette aus [getReplacement()](../../com.aspose.words/replacingargs/\#getReplacement) / [setReplacement(java.lang.String)](../../com.aspose.words/replacingargs/\#setReplacement-java.lang.String) ersetzt werden soll. |
| [setReplacement(String value)](#setReplacement-java.lang.String) | Setzt die Ersetzungszeichenfolge. |
### getGroupIndex() {#getGroupIndex}
```
public int getGroupIndex()
```


Identifiziert, nach Index, eine erfasste Gruppe in der [getMatch()](../../com.aspose.words/replacingargs/\#getMatch), die durch die Zeichenkette aus [getReplacement()](../../com.aspose.words/replacingargs/\#getReplacement) / [setReplacement(java.lang.String)](../../com.aspose.words/replacingargs/\#setReplacement-java.lang.String) ersetzt werden soll.

 **Remarks:** 

Standardwert ist 0.

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
int - Der entsprechende int-Wert.
### getMatch() {#getMatch}
```
public Matcher getMatch()
```


Der java.util.regex.Matcher, der aus einem einzelnen regulären Ausdrucks-Match während einer **Replace** resultiert.

 **Remarks:** 

Matcher.start() liefert die nullbasierte Startposition der Übereinstimmung ab dem Beginn des Such‑ und Ersetzungsbereichs.

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
java.util.regex.Matcher – Der entsprechende java.util.regex.Matcher‑Wert.
### getMatchEndNode() {#getMatchEndNode}
```
public Node getMatchEndNode()
```


Liefert den Knoten, der das Ende der Übereinstimmung enthält.

 **Examples:** 

Zeigt, wie man den Endknoten der Übereinstimmung erhält.

```
{@code
```

**Returns:**
[Node](../../com.aspose.words/node/) - The node that contains the end of the match.
### getMatchNode() {#getMatchNode}
```
public Node getMatchNode()
```


Liefert den Knoten, der den Anfang der Übereinstimmung enthält.

 **Examples:** 

Zeigt, wie der gesamte Inhalt eines Dokuments als Ersatz für eine Übereinstimmung in einer Suchen‑und‑Ersetzen‑Operation eingefügt wird.

```

 public void insertDocumentAtReplace() throws Exception {
     Document mainDoc = new Document(getMyDir() + "Document insertion destination.docx");

     // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
     FindReplaceOptions options = new FindReplaceOptions();
     options.setReplacingCallback(new InsertDocumentAtReplaceHandler());

     mainDoc.getRange().replace(Pattern.compile("\[MY_DOCUMENT\]"), "", options);
     mainDoc.save(getArtifactsDir() + "InsertDocument.InsertDocumentAtReplace.docx");

 }

 private static class InsertDocumentAtReplaceHandler implements IReplacingCallback {
     public int replacing(ReplacingArgs args) throws Exception {
         Document subDoc = new Document(getMyDir() + "Document.docx");

         // Insert a document after the paragraph containing the matched text.
         Paragraph para = (Paragraph) args.getMatchNode().getParentNode();
         insertDocument(para, subDoc);

         // Remove the paragraph with the matched text.
         para.remove();

         return ReplaceAction.SKIP;
     }
 }

 /// 
 /// Inserts all the nodes of another document after a paragraph or table.
 /// 
 private static void insertDocument(Node insertionDestination, Document docToInsert) {
     if (((insertionDestination.getNodeType()) == (NodeType.PARAGRAPH)) || ((insertionDestination.getNodeType()) == (NodeType.TABLE))) {
         CompositeNode dstStory = insertionDestination.getParentNode();

         NodeImporter importer =
                 new NodeImporter(docToInsert, insertionDestination.getDocument(), ImportFormatMode.KEEP_SOURCE_FORMATTING);

         for (Section srcSection : docToInsert.getSections())
             for (Node srcNode : srcSection.getBody()) {
                 // Skip the node if it is the last empty paragraph in a section.
                 if (((srcNode.getNodeType()) == (NodeType.PARAGRAPH))) {
                     Paragraph para = (Paragraph) srcNode;
                     if (para.isEndOfSection() && !para.hasChildNodes())
                         continue;
                 }

                 Node newNode = importer.importNode(srcNode, true);

                 dstStory.insertAfter(newNode, insertionDestination);
                 insertionDestination = newNode;
             }
     } else {
         throw new IllegalArgumentException("The destination node must be either a paragraph or table.");
     }
 }
 
```

**Returns:**
[Node](../../com.aspose.words/node/) - The node that contains the beginning of the match.
### getMatchOffset() {#getMatchOffset}
```
public int getMatchOffset()
```


Liefert die nullbasierte Startposition der Übereinstimmung ab dem Beginn des Knotens, der den Anfang der Übereinstimmung enthält.

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
int – Die nullbasierte Startposition der Übereinstimmung ab dem Beginn des Knotens, der den Anfang der Übereinstimmung enthält.
### getReplacement() {#getReplacement}
```
public String getReplacement()
```


Liefert die Ersetzungszeichenfolge.

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

**Returns:**
java.lang.String – Die Ersetzungszeichenfolge.
### setGroupIndex(int value) {#setGroupIndex-int}
```
public void setGroupIndex(int value)
```


Identifiziert, nach Index, eine erfasste Gruppe in der [getMatch()](../../com.aspose.words/replacingargs/\#getMatch), die durch die Zeichenkette aus [getReplacement()](../../com.aspose.words/replacingargs/\#getReplacement) / [setReplacement(java.lang.String)](../../com.aspose.words/replacingargs/\#setReplacement-java.lang.String) ersetzt werden soll.

 **Remarks:** 

Standardwert ist 0.

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

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int | Der entsprechende  int  Wert. |

### setReplacement(String value) {#setReplacement-java.lang.String}
```
public void setReplacement(String value)
```


Setzt die Ersetzungszeichenfolge.

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

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Die Ersetzungszeichenfolge. |

