---
title: "CompareOptions"
linktitle: "CompareOptions"
second_title: "Aspose.Words für Java"
description: "Ermöglicht die Auswahl zusätzlicher Optionen für den Dokumentvergleichsvorgang in Java."
type: docs
weight: 113
url: /de/java/com.aspose.words/compareoptions/
---

**Inheritance:**
java.lang.Object
```
public class CompareOptions
```

Ermöglicht die Auswahl zusätzlicher Optionen für den Dokumentvergleichsvorgang.

Weitere Informationen finden Sie im Dokumentationsartikel [ Compare Documents ][Compare Documents].

 **Examples:** 

Zeigt, wie bestimmte Arten von Dokumentelementen beim Vergleich gefiltert werden können.

```

 // Create the original document and populate it with various kinds of elements.
 Document docOriginal = new Document();
 DocumentBuilder builder = new DocumentBuilder(docOriginal);

 // Paragraph text referenced with an endnote:
 builder.writeln("Hello world! This is the first paragraph.");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Original endnote text.");

 // Table:
 builder.startTable();
 builder.insertCell();
 builder.write("Original cell 1 text");
 builder.insertCell();
 builder.write("Original cell 2 text");
 builder.endTable();

 // Textbox:
 Shape textBox = builder.insertShape(ShapeType.TEXT_BOX, 150.0, 20.0);
 builder.moveTo(textBox.getFirstParagraph());
 builder.write("Original textbox contents");

 // DATE field:
 builder.moveTo(docOriginal.getFirstSection().getBody().appendParagraph(""));
 builder.insertField(" DATE ");

 // Comment:
 Comment newComment = new Comment(docOriginal, "John Doe", "J.D.", new Date());
 newComment.setText("Original comment.");
 builder.getCurrentParagraph().appendChild(newComment);

 // Header:
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.writeln("Original header contents.");

 // Create a clone of our document and perform a quick edit on each of the cloned document's elements.
 Document docEdited = (Document)docOriginal.deepClone(true);
 Paragraph firstParagraph = docEdited.getFirstSection().getBody().getFirstParagraph();

 firstParagraph.getRuns().get(0).setText("hello world! this is the first paragraph, after editing.");
 firstParagraph.getParagraphFormat().setStyle(docEdited.getStyles().getByStyleIdentifier(StyleIdentifier.HEADING_1));
 ((Footnote)docEdited.getChild(NodeType.FOOTNOTE, 0, true)).getFirstParagraph().getRuns().get(1).setText("Edited endnote text.");
 ((Table)docEdited.getChild(NodeType.TABLE, 0, true)).getFirstRow().getCells().get(1).getFirstParagraph().getRuns().get(0).setText("Edited Cell 2 contents");
 ((Shape)docEdited.getChild(NodeType.SHAPE, 0, true)).getFirstParagraph().getRuns().get(0).setText("Edited textbox contents");
 ((FieldDate)docEdited.getRange().getFields().get(0)).setUseLunarCalendar(true);
 ((Comment)docEdited.getChild(NodeType.COMMENT, 0, true)).getFirstParagraph().getRuns().get(0).setText("Edited comment.");
 docEdited.getFirstSection().getHeadersFooters().getByHeaderFooterType(HeaderFooterType.HEADER_PRIMARY).getFirstParagraph().getRuns().get(0).setText("Edited header contents.");

 // Comparing documents creates a revision for every edit in the edited document.
 // A CompareOptions object has a series of flags that can suppress revisions
 // on each respective type of element, effectively ignoring their change.
 CompareOptions compareOptions = new CompareOptions();
 compareOptions.setCompareMoves(false);
 compareOptions.setIgnoreFormatting(false);
 compareOptions.setIgnoreCaseChanges(false);
 compareOptions.setIgnoreComments(false);
 compareOptions.setIgnoreTables(false);
 compareOptions.setIgnoreFields(false);
 compareOptions.setIgnoreFootnotes(false);
 compareOptions.setIgnoreTextboxes(false);
 compareOptions.setIgnoreHeadersAndFooters(false);
 compareOptions.setTarget(ComparisonTargetType.NEW);

 docOriginal.compare(docEdited, "John Doe", new Date(), compareOptions);
 docOriginal.save(getArtifactsDir() + "Revision.CompareOptions.docx");
 
```


[Compare Documents]: https://docs.aspose.com/words/java/compare-documents/
## Konstruktoren

| Konstruktor | Beschreibung |
| --- | --- |
| [CompareOptions()](#CompareOptions) | Initialisiert eine neue Instanz dieser Klasse. |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getAdvancedOptions()](#getAdvancedOptions) | Gibt erweiterte Vergleichsoptionen an, die dabei helfen können, präzisere Vergleichsergebnisse zu erzeugen. |
| [getCompareMoves()](#getCompareMoves) | Gibt an, ob Unterschiede zwischen den beiden Dokumenten verglichen werden sollen. |
| [getGranularity()](#getGranularity) | Gibt an, ob Änderungen Zeichenweise oder Wortweise nachverfolgt werden. |
| [getIgnoreCaseChanges()](#getIgnoreCaseChanges) | True gibt an, dass der Dokumentvergleich nicht zwischen Groß- und Kleinschreibung unterscheidet. |
| [getIgnoreComments()](#getIgnoreComments) | Gibt an, ob Unterschiede in Kommentaren verglichen werden sollen. |
| [getIgnoreDmlUniqueId()](#getIgnoreDmlUniqueId) | Gibt an, ob Unterschiede in der eindeutigen DrawingML‑ID ignoriert werden sollen. |
| [getIgnoreFields()](#getIgnoreFields) | Gibt an, ob Unterschiede in Feldern verglichen werden sollen. |
| [getIgnoreFootnotes()](#getIgnoreFootnotes) | Gibt an, ob Unterschiede in Fußnoten und Endnoten verglichen werden sollen. |
| [getIgnoreFormatting()](#getIgnoreFormatting) | True gibt an, dass die Formatierung ignoriert wird. |
| [getIgnoreHeadersAndFooters()](#getIgnoreHeadersAndFooters) | True gibt an, dass der Inhalt von Kopf‑ und Fußzeilen ignoriert wird. |
| [getIgnoreTables()](#getIgnoreTables) | Gibt an, ob Unterschiede in den in Tabellen enthaltenen Daten verglichen werden sollen. |
| [getIgnoreTextboxes()](#getIgnoreTextboxes) | Gibt an, ob Unterschiede in den in Textfeldern enthaltenen Daten verglichen werden sollen. |
| [getTarget()](#getTarget) | Gibt an, welches Dokument während des Vergleichs als Ziel verwendet werden soll. |
| [setCompareMoves(boolean value)](#setCompareMoves-boolean) | Gibt an, ob Unterschiede zwischen den beiden Dokumenten verglichen werden sollen. |
| [setGranularity(int value)](#setGranularity-int) | Gibt an, ob Änderungen Zeichenweise oder Wortweise nachverfolgt werden. |
| [setIgnoreCaseChanges(boolean value)](#setIgnoreCaseChanges-boolean) | True gibt an, dass der Dokumentvergleich nicht zwischen Groß- und Kleinschreibung unterscheidet. |
| [setIgnoreComments(boolean value)](#setIgnoreComments-boolean) | Gibt an, ob Unterschiede in Kommentaren verglichen werden sollen. |
| [setIgnoreDmlUniqueId(boolean value)](#setIgnoreDmlUniqueId-boolean) | Gibt an, ob Unterschiede in der eindeutigen DrawingML‑ID ignoriert werden sollen. |
| [setIgnoreFields(boolean value)](#setIgnoreFields-boolean) | Gibt an, ob Unterschiede in Feldern verglichen werden sollen. |
| [setIgnoreFootnotes(boolean value)](#setIgnoreFootnotes-boolean) | Gibt an, ob Unterschiede in Fußnoten und Endnoten verglichen werden sollen. |
| [setIgnoreFormatting(boolean value)](#setIgnoreFormatting-boolean) | True gibt an, dass die Formatierung ignoriert wird. |
| [setIgnoreHeadersAndFooters(boolean value)](#setIgnoreHeadersAndFooters-boolean) | True gibt an, dass der Inhalt von Kopf‑ und Fußzeilen ignoriert wird. |
| [setIgnoreTables(boolean value)](#setIgnoreTables-boolean) | Gibt an, ob Unterschiede in den in Tabellen enthaltenen Daten verglichen werden sollen. |
| [setIgnoreTextboxes(boolean value)](#setIgnoreTextboxes-boolean) | Gibt an, ob Unterschiede in den in Textfeldern enthaltenen Daten verglichen werden sollen. |
| [setTarget(int value)](#setTarget-int) | Gibt an, welches Dokument während des Vergleichs als Ziel verwendet werden soll. |
### CompareOptions() {#CompareOptions}
```
public CompareOptions()
```


Initialisiert eine neue Instanz dieser Klasse.

### getAdvancedOptions() {#getAdvancedOptions}
```
public AdvancedCompareOptions getAdvancedOptions()
```


Gibt erweiterte Vergleichsoptionen an, die dabei helfen können, präzisere Vergleichsergebnisse zu erzeugen.

 **Examples:** 

Zeigt, wie man Dokumente vergleicht, wobei die eindeutige DML‑ID ignoriert wird.

```

 Document docA = new Document(getMyDir() + "DML unique ID original.docx");
 Document docB = new Document(getMyDir() + "DML unique ID compare.docx");

 // By default, Aspose.Words do not ignore DML's unique ID, and the revisions count was 2.
 // If we are ignoring DML's unique ID, and revisions count were 0.
 CompareOptions compareOptions = new CompareOptions();
 compareOptions.getAdvancedOptions().setIgnoreDmlUniqueId(isIgnoreDmlUniqueId);

 docA.compare(docB, "Aspose.Words", new Date(), compareOptions);

 Assert.assertEquals(isIgnoreDmlUniqueId ? 1 : 3, docA.getRevisions().getCount());
 
```

**Returns:**
[AdvancedCompareOptions](../../com.aspose.words/advancedcompareoptions/) - The corresponding [AdvancedCompareOptions](../../com.aspose.words/advancedcompareoptions/) value.
### getCompareMoves() {#getCompareMoves}
```
public boolean getCompareMoves()
```


Gibt an, ob Unterschiede zwischen den beiden Dokumenten verglichen werden sollen.

 **Remarks:** 

Standardmäßig werden Verschiebungsrevisionen nicht erzeugt.

 **Examples:** 

Zeigt, wie bestimmte Arten von Dokumentelementen beim Vergleich gefiltert werden können.

```

 // Create the original document and populate it with various kinds of elements.
 Document docOriginal = new Document();
 DocumentBuilder builder = new DocumentBuilder(docOriginal);

 // Paragraph text referenced with an endnote:
 builder.writeln("Hello world! This is the first paragraph.");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Original endnote text.");

 // Table:
 builder.startTable();
 builder.insertCell();
 builder.write("Original cell 1 text");
 builder.insertCell();
 builder.write("Original cell 2 text");
 builder.endTable();

 // Textbox:
 Shape textBox = builder.insertShape(ShapeType.TEXT_BOX, 150.0, 20.0);
 builder.moveTo(textBox.getFirstParagraph());
 builder.write("Original textbox contents");

 // DATE field:
 builder.moveTo(docOriginal.getFirstSection().getBody().appendParagraph(""));
 builder.insertField(" DATE ");

 // Comment:
 Comment newComment = new Comment(docOriginal, "John Doe", "J.D.", new Date());
 newComment.setText("Original comment.");
 builder.getCurrentParagraph().appendChild(newComment);

 // Header:
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.writeln("Original header contents.");

 // Create a clone of our document and perform a quick edit on each of the cloned document's elements.
 Document docEdited = (Document)docOriginal.deepClone(true);
 Paragraph firstParagraph = docEdited.getFirstSection().getBody().getFirstParagraph();

 firstParagraph.getRuns().get(0).setText("hello world! this is the first paragraph, after editing.");
 firstParagraph.getParagraphFormat().setStyle(docEdited.getStyles().getByStyleIdentifier(StyleIdentifier.HEADING_1));
 ((Footnote)docEdited.getChild(NodeType.FOOTNOTE, 0, true)).getFirstParagraph().getRuns().get(1).setText("Edited endnote text.");
 ((Table)docEdited.getChild(NodeType.TABLE, 0, true)).getFirstRow().getCells().get(1).getFirstParagraph().getRuns().get(0).setText("Edited Cell 2 contents");
 ((Shape)docEdited.getChild(NodeType.SHAPE, 0, true)).getFirstParagraph().getRuns().get(0).setText("Edited textbox contents");
 ((FieldDate)docEdited.getRange().getFields().get(0)).setUseLunarCalendar(true);
 ((Comment)docEdited.getChild(NodeType.COMMENT, 0, true)).getFirstParagraph().getRuns().get(0).setText("Edited comment.");
 docEdited.getFirstSection().getHeadersFooters().getByHeaderFooterType(HeaderFooterType.HEADER_PRIMARY).getFirstParagraph().getRuns().get(0).setText("Edited header contents.");

 // Comparing documents creates a revision for every edit in the edited document.
 // A CompareOptions object has a series of flags that can suppress revisions
 // on each respective type of element, effectively ignoring their change.
 CompareOptions compareOptions = new CompareOptions();
 compareOptions.setCompareMoves(false);
 compareOptions.setIgnoreFormatting(false);
 compareOptions.setIgnoreCaseChanges(false);
 compareOptions.setIgnoreComments(false);
 compareOptions.setIgnoreTables(false);
 compareOptions.setIgnoreFields(false);
 compareOptions.setIgnoreFootnotes(false);
 compareOptions.setIgnoreTextboxes(false);
 compareOptions.setIgnoreHeadersAndFooters(false);
 compareOptions.setTarget(ComparisonTargetType.NEW);

 docOriginal.compare(docEdited, "John Doe", new Date(), compareOptions);
 docOriginal.save(getArtifactsDir() + "Revision.CompareOptions.docx");
 
```

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### getGranularity() {#getGranularity}
```
public int getGranularity()
```


Gibt an, ob Änderungen Zeichenweise oder Wortweise nachverfolgt werden.

 **Remarks:** 

Standardwert ist [Granularity.WORD\_LEVEL](../../com.aspose.words/granularity/\#WORD-LEVEL).

 **Examples:** 

Zeigt, wie man eine Granularität beim Vergleich von Dokumenten angibt.

```

 Document docA = new Document();
 DocumentBuilder builderA = new DocumentBuilder(docA);
 builderA.writeln("Alpha Lorem ipsum dolor sit amet, consectetur adipiscing elit");

 Document docB = new Document();
 DocumentBuilder builderB = new DocumentBuilder(docB);
 builderB.writeln("Lorems ipsum dolor sit amet consectetur - \"adipiscing\" elit");

 // Specify whether changes are tracking
 // by character ('Granularity.CharLevel'), or by word ('Granularity.WordLevel').
 CompareOptions compareOptions = new CompareOptions();
 compareOptions.setGranularity(granularity);

 docA.compare(docB, "author", new Date(), compareOptions);

 // The first document's collection of revision groups contains all the differences between documents.
 RevisionGroupCollection groups = docA.getRevisions().getGroups();
 Assert.assertEquals(5, groups.getCount());
 
```

**Returns:**
int - Der entsprechende  int  Wert. Der zurückgegebene Wert ist einer der [Granularity](../../com.aspose.words/granularity/) Konstanten.
### getIgnoreCaseChanges() {#getIgnoreCaseChanges}
```
public boolean getIgnoreCaseChanges()
```


True gibt an, dass der Dokumentvergleich nicht zwischen Groß- und Kleinschreibung unterscheidet.

 **Remarks:** 

Standardmäßig ist der Vergleich groß‑ und kleinschreibungssensitiv.

 **Examples:** 

Zeigt, wie bestimmte Arten von Dokumentelementen beim Vergleich gefiltert werden können.

```

 // Create the original document and populate it with various kinds of elements.
 Document docOriginal = new Document();
 DocumentBuilder builder = new DocumentBuilder(docOriginal);

 // Paragraph text referenced with an endnote:
 builder.writeln("Hello world! This is the first paragraph.");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Original endnote text.");

 // Table:
 builder.startTable();
 builder.insertCell();
 builder.write("Original cell 1 text");
 builder.insertCell();
 builder.write("Original cell 2 text");
 builder.endTable();

 // Textbox:
 Shape textBox = builder.insertShape(ShapeType.TEXT_BOX, 150.0, 20.0);
 builder.moveTo(textBox.getFirstParagraph());
 builder.write("Original textbox contents");

 // DATE field:
 builder.moveTo(docOriginal.getFirstSection().getBody().appendParagraph(""));
 builder.insertField(" DATE ");

 // Comment:
 Comment newComment = new Comment(docOriginal, "John Doe", "J.D.", new Date());
 newComment.setText("Original comment.");
 builder.getCurrentParagraph().appendChild(newComment);

 // Header:
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.writeln("Original header contents.");

 // Create a clone of our document and perform a quick edit on each of the cloned document's elements.
 Document docEdited = (Document)docOriginal.deepClone(true);
 Paragraph firstParagraph = docEdited.getFirstSection().getBody().getFirstParagraph();

 firstParagraph.getRuns().get(0).setText("hello world! this is the first paragraph, after editing.");
 firstParagraph.getParagraphFormat().setStyle(docEdited.getStyles().getByStyleIdentifier(StyleIdentifier.HEADING_1));
 ((Footnote)docEdited.getChild(NodeType.FOOTNOTE, 0, true)).getFirstParagraph().getRuns().get(1).setText("Edited endnote text.");
 ((Table)docEdited.getChild(NodeType.TABLE, 0, true)).getFirstRow().getCells().get(1).getFirstParagraph().getRuns().get(0).setText("Edited Cell 2 contents");
 ((Shape)docEdited.getChild(NodeType.SHAPE, 0, true)).getFirstParagraph().getRuns().get(0).setText("Edited textbox contents");
 ((FieldDate)docEdited.getRange().getFields().get(0)).setUseLunarCalendar(true);
 ((Comment)docEdited.getChild(NodeType.COMMENT, 0, true)).getFirstParagraph().getRuns().get(0).setText("Edited comment.");
 docEdited.getFirstSection().getHeadersFooters().getByHeaderFooterType(HeaderFooterType.HEADER_PRIMARY).getFirstParagraph().getRuns().get(0).setText("Edited header contents.");

 // Comparing documents creates a revision for every edit in the edited document.
 // A CompareOptions object has a series of flags that can suppress revisions
 // on each respective type of element, effectively ignoring their change.
 CompareOptions compareOptions = new CompareOptions();
 compareOptions.setCompareMoves(false);
 compareOptions.setIgnoreFormatting(false);
 compareOptions.setIgnoreCaseChanges(false);
 compareOptions.setIgnoreComments(false);
 compareOptions.setIgnoreTables(false);
 compareOptions.setIgnoreFields(false);
 compareOptions.setIgnoreFootnotes(false);
 compareOptions.setIgnoreTextboxes(false);
 compareOptions.setIgnoreHeadersAndFooters(false);
 compareOptions.setTarget(ComparisonTargetType.NEW);

 docOriginal.compare(docEdited, "John Doe", new Date(), compareOptions);
 docOriginal.save(getArtifactsDir() + "Revision.CompareOptions.docx");
 
```

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### getIgnoreComments() {#getIgnoreComments}
```
public boolean getIgnoreComments()
```


Gibt an, ob Unterschiede in Kommentaren verglichen werden sollen.

 **Remarks:** 

Standardmäßig werden Kommentare nicht ignoriert.

 **Examples:** 

Zeigt, wie bestimmte Arten von Dokumentelementen beim Vergleich gefiltert werden können.

```

 // Create the original document and populate it with various kinds of elements.
 Document docOriginal = new Document();
 DocumentBuilder builder = new DocumentBuilder(docOriginal);

 // Paragraph text referenced with an endnote:
 builder.writeln("Hello world! This is the first paragraph.");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Original endnote text.");

 // Table:
 builder.startTable();
 builder.insertCell();
 builder.write("Original cell 1 text");
 builder.insertCell();
 builder.write("Original cell 2 text");
 builder.endTable();

 // Textbox:
 Shape textBox = builder.insertShape(ShapeType.TEXT_BOX, 150.0, 20.0);
 builder.moveTo(textBox.getFirstParagraph());
 builder.write("Original textbox contents");

 // DATE field:
 builder.moveTo(docOriginal.getFirstSection().getBody().appendParagraph(""));
 builder.insertField(" DATE ");

 // Comment:
 Comment newComment = new Comment(docOriginal, "John Doe", "J.D.", new Date());
 newComment.setText("Original comment.");
 builder.getCurrentParagraph().appendChild(newComment);

 // Header:
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.writeln("Original header contents.");

 // Create a clone of our document and perform a quick edit on each of the cloned document's elements.
 Document docEdited = (Document)docOriginal.deepClone(true);
 Paragraph firstParagraph = docEdited.getFirstSection().getBody().getFirstParagraph();

 firstParagraph.getRuns().get(0).setText("hello world! this is the first paragraph, after editing.");
 firstParagraph.getParagraphFormat().setStyle(docEdited.getStyles().getByStyleIdentifier(StyleIdentifier.HEADING_1));
 ((Footnote)docEdited.getChild(NodeType.FOOTNOTE, 0, true)).getFirstParagraph().getRuns().get(1).setText("Edited endnote text.");
 ((Table)docEdited.getChild(NodeType.TABLE, 0, true)).getFirstRow().getCells().get(1).getFirstParagraph().getRuns().get(0).setText("Edited Cell 2 contents");
 ((Shape)docEdited.getChild(NodeType.SHAPE, 0, true)).getFirstParagraph().getRuns().get(0).setText("Edited textbox contents");
 ((FieldDate)docEdited.getRange().getFields().get(0)).setUseLunarCalendar(true);
 ((Comment)docEdited.getChild(NodeType.COMMENT, 0, true)).getFirstParagraph().getRuns().get(0).setText("Edited comment.");
 docEdited.getFirstSection().getHeadersFooters().getByHeaderFooterType(HeaderFooterType.HEADER_PRIMARY).getFirstParagraph().getRuns().get(0).setText("Edited header contents.");

 // Comparing documents creates a revision for every edit in the edited document.
 // A CompareOptions object has a series of flags that can suppress revisions
 // on each respective type of element, effectively ignoring their change.
 CompareOptions compareOptions = new CompareOptions();
 compareOptions.setCompareMoves(false);
 compareOptions.setIgnoreFormatting(false);
 compareOptions.setIgnoreCaseChanges(false);
 compareOptions.setIgnoreComments(false);
 compareOptions.setIgnoreTables(false);
 compareOptions.setIgnoreFields(false);
 compareOptions.setIgnoreFootnotes(false);
 compareOptions.setIgnoreTextboxes(false);
 compareOptions.setIgnoreHeadersAndFooters(false);
 compareOptions.setTarget(ComparisonTargetType.NEW);

 docOriginal.compare(docEdited, "John Doe", new Date(), compareOptions);
 docOriginal.save(getArtifactsDir() + "Revision.CompareOptions.docx");
 
```

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### getIgnoreDmlUniqueId() {#getIgnoreDmlUniqueId}
```
public boolean getIgnoreDmlUniqueId()
```


Gibt an, ob Unterschiede in der eindeutigen DrawingML‑ID ignoriert werden sollen.

 **Remarks:** 

Standardwert ist false.

 **Examples:** 

Zeigt, wie man Dokumente vergleicht, wobei die eindeutige DML‑ID ignoriert wird.

```

 Document docA = new Document(getMyDir() + "DML unique ID original.docx");
 Document docB = new Document(getMyDir() + "DML unique ID compare.docx");

 // By default, Aspose.Words do not ignore DML's unique ID, and the revisions count was 2.
 // If we are ignoring DML's unique ID, and revisions count were 0.
 CompareOptions compareOptions = new CompareOptions();
 compareOptions.getAdvancedOptions().setIgnoreDmlUniqueId(isIgnoreDmlUniqueId);

 docA.compare(docB, "Aspose.Words", new Date(), compareOptions);

 Assert.assertEquals(isIgnoreDmlUniqueId ? 1 : 3, docA.getRevisions().getCount());
 
```

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### getIgnoreFields() {#getIgnoreFields}
```
public boolean getIgnoreFields()
```


Gibt an, ob Unterschiede in Feldern verglichen werden sollen.

 **Remarks:** 

Standardmäßig werden Felder nicht ignoriert.

 **Examples:** 

Zeigt, wie bestimmte Arten von Dokumentelementen beim Vergleich gefiltert werden können.

```

 // Create the original document and populate it with various kinds of elements.
 Document docOriginal = new Document();
 DocumentBuilder builder = new DocumentBuilder(docOriginal);

 // Paragraph text referenced with an endnote:
 builder.writeln("Hello world! This is the first paragraph.");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Original endnote text.");

 // Table:
 builder.startTable();
 builder.insertCell();
 builder.write("Original cell 1 text");
 builder.insertCell();
 builder.write("Original cell 2 text");
 builder.endTable();

 // Textbox:
 Shape textBox = builder.insertShape(ShapeType.TEXT_BOX, 150.0, 20.0);
 builder.moveTo(textBox.getFirstParagraph());
 builder.write("Original textbox contents");

 // DATE field:
 builder.moveTo(docOriginal.getFirstSection().getBody().appendParagraph(""));
 builder.insertField(" DATE ");

 // Comment:
 Comment newComment = new Comment(docOriginal, "John Doe", "J.D.", new Date());
 newComment.setText("Original comment.");
 builder.getCurrentParagraph().appendChild(newComment);

 // Header:
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.writeln("Original header contents.");

 // Create a clone of our document and perform a quick edit on each of the cloned document's elements.
 Document docEdited = (Document)docOriginal.deepClone(true);
 Paragraph firstParagraph = docEdited.getFirstSection().getBody().getFirstParagraph();

 firstParagraph.getRuns().get(0).setText("hello world! this is the first paragraph, after editing.");
 firstParagraph.getParagraphFormat().setStyle(docEdited.getStyles().getByStyleIdentifier(StyleIdentifier.HEADING_1));
 ((Footnote)docEdited.getChild(NodeType.FOOTNOTE, 0, true)).getFirstParagraph().getRuns().get(1).setText("Edited endnote text.");
 ((Table)docEdited.getChild(NodeType.TABLE, 0, true)).getFirstRow().getCells().get(1).getFirstParagraph().getRuns().get(0).setText("Edited Cell 2 contents");
 ((Shape)docEdited.getChild(NodeType.SHAPE, 0, true)).getFirstParagraph().getRuns().get(0).setText("Edited textbox contents");
 ((FieldDate)docEdited.getRange().getFields().get(0)).setUseLunarCalendar(true);
 ((Comment)docEdited.getChild(NodeType.COMMENT, 0, true)).getFirstParagraph().getRuns().get(0).setText("Edited comment.");
 docEdited.getFirstSection().getHeadersFooters().getByHeaderFooterType(HeaderFooterType.HEADER_PRIMARY).getFirstParagraph().getRuns().get(0).setText("Edited header contents.");

 // Comparing documents creates a revision for every edit in the edited document.
 // A CompareOptions object has a series of flags that can suppress revisions
 // on each respective type of element, effectively ignoring their change.
 CompareOptions compareOptions = new CompareOptions();
 compareOptions.setCompareMoves(false);
 compareOptions.setIgnoreFormatting(false);
 compareOptions.setIgnoreCaseChanges(false);
 compareOptions.setIgnoreComments(false);
 compareOptions.setIgnoreTables(false);
 compareOptions.setIgnoreFields(false);
 compareOptions.setIgnoreFootnotes(false);
 compareOptions.setIgnoreTextboxes(false);
 compareOptions.setIgnoreHeadersAndFooters(false);
 compareOptions.setTarget(ComparisonTargetType.NEW);

 docOriginal.compare(docEdited, "John Doe", new Date(), compareOptions);
 docOriginal.save(getArtifactsDir() + "Revision.CompareOptions.docx");
 
```

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### getIgnoreFootnotes() {#getIgnoreFootnotes}
```
public boolean getIgnoreFootnotes()
```


Gibt an, ob Unterschiede in Fußnoten und Endnoten verglichen werden sollen.

 **Remarks:** 

Standardmäßig werden Fußnoten nicht ignoriert.

 **Examples:** 

Zeigt, wie bestimmte Arten von Dokumentelementen beim Vergleich gefiltert werden können.

```

 // Create the original document and populate it with various kinds of elements.
 Document docOriginal = new Document();
 DocumentBuilder builder = new DocumentBuilder(docOriginal);

 // Paragraph text referenced with an endnote:
 builder.writeln("Hello world! This is the first paragraph.");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Original endnote text.");

 // Table:
 builder.startTable();
 builder.insertCell();
 builder.write("Original cell 1 text");
 builder.insertCell();
 builder.write("Original cell 2 text");
 builder.endTable();

 // Textbox:
 Shape textBox = builder.insertShape(ShapeType.TEXT_BOX, 150.0, 20.0);
 builder.moveTo(textBox.getFirstParagraph());
 builder.write("Original textbox contents");

 // DATE field:
 builder.moveTo(docOriginal.getFirstSection().getBody().appendParagraph(""));
 builder.insertField(" DATE ");

 // Comment:
 Comment newComment = new Comment(docOriginal, "John Doe", "J.D.", new Date());
 newComment.setText("Original comment.");
 builder.getCurrentParagraph().appendChild(newComment);

 // Header:
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.writeln("Original header contents.");

 // Create a clone of our document and perform a quick edit on each of the cloned document's elements.
 Document docEdited = (Document)docOriginal.deepClone(true);
 Paragraph firstParagraph = docEdited.getFirstSection().getBody().getFirstParagraph();

 firstParagraph.getRuns().get(0).setText("hello world! this is the first paragraph, after editing.");
 firstParagraph.getParagraphFormat().setStyle(docEdited.getStyles().getByStyleIdentifier(StyleIdentifier.HEADING_1));
 ((Footnote)docEdited.getChild(NodeType.FOOTNOTE, 0, true)).getFirstParagraph().getRuns().get(1).setText("Edited endnote text.");
 ((Table)docEdited.getChild(NodeType.TABLE, 0, true)).getFirstRow().getCells().get(1).getFirstParagraph().getRuns().get(0).setText("Edited Cell 2 contents");
 ((Shape)docEdited.getChild(NodeType.SHAPE, 0, true)).getFirstParagraph().getRuns().get(0).setText("Edited textbox contents");
 ((FieldDate)docEdited.getRange().getFields().get(0)).setUseLunarCalendar(true);
 ((Comment)docEdited.getChild(NodeType.COMMENT, 0, true)).getFirstParagraph().getRuns().get(0).setText("Edited comment.");
 docEdited.getFirstSection().getHeadersFooters().getByHeaderFooterType(HeaderFooterType.HEADER_PRIMARY).getFirstParagraph().getRuns().get(0).setText("Edited header contents.");

 // Comparing documents creates a revision for every edit in the edited document.
 // A CompareOptions object has a series of flags that can suppress revisions
 // on each respective type of element, effectively ignoring their change.
 CompareOptions compareOptions = new CompareOptions();
 compareOptions.setCompareMoves(false);
 compareOptions.setIgnoreFormatting(false);
 compareOptions.setIgnoreCaseChanges(false);
 compareOptions.setIgnoreComments(false);
 compareOptions.setIgnoreTables(false);
 compareOptions.setIgnoreFields(false);
 compareOptions.setIgnoreFootnotes(false);
 compareOptions.setIgnoreTextboxes(false);
 compareOptions.setIgnoreHeadersAndFooters(false);
 compareOptions.setTarget(ComparisonTargetType.NEW);

 docOriginal.compare(docEdited, "John Doe", new Date(), compareOptions);
 docOriginal.save(getArtifactsDir() + "Revision.CompareOptions.docx");
 
```

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### getIgnoreFormatting() {#getIgnoreFormatting}
```
public boolean getIgnoreFormatting()
```


True gibt an, dass die Formatierung ignoriert wird.

 **Remarks:** 

Standardmäßig wird die Dokumentformatierung nicht ignoriert.

 **Examples:** 

Zeigt, wie bestimmte Arten von Dokumentelementen beim Vergleich gefiltert werden können.

```

 // Create the original document and populate it with various kinds of elements.
 Document docOriginal = new Document();
 DocumentBuilder builder = new DocumentBuilder(docOriginal);

 // Paragraph text referenced with an endnote:
 builder.writeln("Hello world! This is the first paragraph.");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Original endnote text.");

 // Table:
 builder.startTable();
 builder.insertCell();
 builder.write("Original cell 1 text");
 builder.insertCell();
 builder.write("Original cell 2 text");
 builder.endTable();

 // Textbox:
 Shape textBox = builder.insertShape(ShapeType.TEXT_BOX, 150.0, 20.0);
 builder.moveTo(textBox.getFirstParagraph());
 builder.write("Original textbox contents");

 // DATE field:
 builder.moveTo(docOriginal.getFirstSection().getBody().appendParagraph(""));
 builder.insertField(" DATE ");

 // Comment:
 Comment newComment = new Comment(docOriginal, "John Doe", "J.D.", new Date());
 newComment.setText("Original comment.");
 builder.getCurrentParagraph().appendChild(newComment);

 // Header:
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.writeln("Original header contents.");

 // Create a clone of our document and perform a quick edit on each of the cloned document's elements.
 Document docEdited = (Document)docOriginal.deepClone(true);
 Paragraph firstParagraph = docEdited.getFirstSection().getBody().getFirstParagraph();

 firstParagraph.getRuns().get(0).setText("hello world! this is the first paragraph, after editing.");
 firstParagraph.getParagraphFormat().setStyle(docEdited.getStyles().getByStyleIdentifier(StyleIdentifier.HEADING_1));
 ((Footnote)docEdited.getChild(NodeType.FOOTNOTE, 0, true)).getFirstParagraph().getRuns().get(1).setText("Edited endnote text.");
 ((Table)docEdited.getChild(NodeType.TABLE, 0, true)).getFirstRow().getCells().get(1).getFirstParagraph().getRuns().get(0).setText("Edited Cell 2 contents");
 ((Shape)docEdited.getChild(NodeType.SHAPE, 0, true)).getFirstParagraph().getRuns().get(0).setText("Edited textbox contents");
 ((FieldDate)docEdited.getRange().getFields().get(0)).setUseLunarCalendar(true);
 ((Comment)docEdited.getChild(NodeType.COMMENT, 0, true)).getFirstParagraph().getRuns().get(0).setText("Edited comment.");
 docEdited.getFirstSection().getHeadersFooters().getByHeaderFooterType(HeaderFooterType.HEADER_PRIMARY).getFirstParagraph().getRuns().get(0).setText("Edited header contents.");

 // Comparing documents creates a revision for every edit in the edited document.
 // A CompareOptions object has a series of flags that can suppress revisions
 // on each respective type of element, effectively ignoring their change.
 CompareOptions compareOptions = new CompareOptions();
 compareOptions.setCompareMoves(false);
 compareOptions.setIgnoreFormatting(false);
 compareOptions.setIgnoreCaseChanges(false);
 compareOptions.setIgnoreComments(false);
 compareOptions.setIgnoreTables(false);
 compareOptions.setIgnoreFields(false);
 compareOptions.setIgnoreFootnotes(false);
 compareOptions.setIgnoreTextboxes(false);
 compareOptions.setIgnoreHeadersAndFooters(false);
 compareOptions.setTarget(ComparisonTargetType.NEW);

 docOriginal.compare(docEdited, "John Doe", new Date(), compareOptions);
 docOriginal.save(getArtifactsDir() + "Revision.CompareOptions.docx");
 
```

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### getIgnoreHeadersAndFooters() {#getIgnoreHeadersAndFooters}
```
public boolean getIgnoreHeadersAndFooters()
```


True gibt an, dass der Inhalt von Kopf‑ und Fußzeilen ignoriert wird.

 **Remarks:** 

Standardmäßig werden Kopf‑ und Fußzeilen nicht ignoriert.

 **Examples:** 

Zeigt, wie bestimmte Arten von Dokumentelementen beim Vergleich gefiltert werden können.

```

 // Create the original document and populate it with various kinds of elements.
 Document docOriginal = new Document();
 DocumentBuilder builder = new DocumentBuilder(docOriginal);

 // Paragraph text referenced with an endnote:
 builder.writeln("Hello world! This is the first paragraph.");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Original endnote text.");

 // Table:
 builder.startTable();
 builder.insertCell();
 builder.write("Original cell 1 text");
 builder.insertCell();
 builder.write("Original cell 2 text");
 builder.endTable();

 // Textbox:
 Shape textBox = builder.insertShape(ShapeType.TEXT_BOX, 150.0, 20.0);
 builder.moveTo(textBox.getFirstParagraph());
 builder.write("Original textbox contents");

 // DATE field:
 builder.moveTo(docOriginal.getFirstSection().getBody().appendParagraph(""));
 builder.insertField(" DATE ");

 // Comment:
 Comment newComment = new Comment(docOriginal, "John Doe", "J.D.", new Date());
 newComment.setText("Original comment.");
 builder.getCurrentParagraph().appendChild(newComment);

 // Header:
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.writeln("Original header contents.");

 // Create a clone of our document and perform a quick edit on each of the cloned document's elements.
 Document docEdited = (Document)docOriginal.deepClone(true);
 Paragraph firstParagraph = docEdited.getFirstSection().getBody().getFirstParagraph();

 firstParagraph.getRuns().get(0).setText("hello world! this is the first paragraph, after editing.");
 firstParagraph.getParagraphFormat().setStyle(docEdited.getStyles().getByStyleIdentifier(StyleIdentifier.HEADING_1));
 ((Footnote)docEdited.getChild(NodeType.FOOTNOTE, 0, true)).getFirstParagraph().getRuns().get(1).setText("Edited endnote text.");
 ((Table)docEdited.getChild(NodeType.TABLE, 0, true)).getFirstRow().getCells().get(1).getFirstParagraph().getRuns().get(0).setText("Edited Cell 2 contents");
 ((Shape)docEdited.getChild(NodeType.SHAPE, 0, true)).getFirstParagraph().getRuns().get(0).setText("Edited textbox contents");
 ((FieldDate)docEdited.getRange().getFields().get(0)).setUseLunarCalendar(true);
 ((Comment)docEdited.getChild(NodeType.COMMENT, 0, true)).getFirstParagraph().getRuns().get(0).setText("Edited comment.");
 docEdited.getFirstSection().getHeadersFooters().getByHeaderFooterType(HeaderFooterType.HEADER_PRIMARY).getFirstParagraph().getRuns().get(0).setText("Edited header contents.");

 // Comparing documents creates a revision for every edit in the edited document.
 // A CompareOptions object has a series of flags that can suppress revisions
 // on each respective type of element, effectively ignoring their change.
 CompareOptions compareOptions = new CompareOptions();
 compareOptions.setCompareMoves(false);
 compareOptions.setIgnoreFormatting(false);
 compareOptions.setIgnoreCaseChanges(false);
 compareOptions.setIgnoreComments(false);
 compareOptions.setIgnoreTables(false);
 compareOptions.setIgnoreFields(false);
 compareOptions.setIgnoreFootnotes(false);
 compareOptions.setIgnoreTextboxes(false);
 compareOptions.setIgnoreHeadersAndFooters(false);
 compareOptions.setTarget(ComparisonTargetType.NEW);

 docOriginal.compare(docEdited, "John Doe", new Date(), compareOptions);
 docOriginal.save(getArtifactsDir() + "Revision.CompareOptions.docx");
 
```

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### getIgnoreTables() {#getIgnoreTables}
```
public boolean getIgnoreTables()
```


Gibt an, ob Unterschiede in den in Tabellen enthaltenen Daten verglichen werden sollen.

 **Remarks:** 

Standardmäßig werden Tabellen nicht ignoriert.

 **Examples:** 

Zeigt, wie bestimmte Arten von Dokumentelementen beim Vergleich gefiltert werden können.

```

 // Create the original document and populate it with various kinds of elements.
 Document docOriginal = new Document();
 DocumentBuilder builder = new DocumentBuilder(docOriginal);

 // Paragraph text referenced with an endnote:
 builder.writeln("Hello world! This is the first paragraph.");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Original endnote text.");

 // Table:
 builder.startTable();
 builder.insertCell();
 builder.write("Original cell 1 text");
 builder.insertCell();
 builder.write("Original cell 2 text");
 builder.endTable();

 // Textbox:
 Shape textBox = builder.insertShape(ShapeType.TEXT_BOX, 150.0, 20.0);
 builder.moveTo(textBox.getFirstParagraph());
 builder.write("Original textbox contents");

 // DATE field:
 builder.moveTo(docOriginal.getFirstSection().getBody().appendParagraph(""));
 builder.insertField(" DATE ");

 // Comment:
 Comment newComment = new Comment(docOriginal, "John Doe", "J.D.", new Date());
 newComment.setText("Original comment.");
 builder.getCurrentParagraph().appendChild(newComment);

 // Header:
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.writeln("Original header contents.");

 // Create a clone of our document and perform a quick edit on each of the cloned document's elements.
 Document docEdited = (Document)docOriginal.deepClone(true);
 Paragraph firstParagraph = docEdited.getFirstSection().getBody().getFirstParagraph();

 firstParagraph.getRuns().get(0).setText("hello world! this is the first paragraph, after editing.");
 firstParagraph.getParagraphFormat().setStyle(docEdited.getStyles().getByStyleIdentifier(StyleIdentifier.HEADING_1));
 ((Footnote)docEdited.getChild(NodeType.FOOTNOTE, 0, true)).getFirstParagraph().getRuns().get(1).setText("Edited endnote text.");
 ((Table)docEdited.getChild(NodeType.TABLE, 0, true)).getFirstRow().getCells().get(1).getFirstParagraph().getRuns().get(0).setText("Edited Cell 2 contents");
 ((Shape)docEdited.getChild(NodeType.SHAPE, 0, true)).getFirstParagraph().getRuns().get(0).setText("Edited textbox contents");
 ((FieldDate)docEdited.getRange().getFields().get(0)).setUseLunarCalendar(true);
 ((Comment)docEdited.getChild(NodeType.COMMENT, 0, true)).getFirstParagraph().getRuns().get(0).setText("Edited comment.");
 docEdited.getFirstSection().getHeadersFooters().getByHeaderFooterType(HeaderFooterType.HEADER_PRIMARY).getFirstParagraph().getRuns().get(0).setText("Edited header contents.");

 // Comparing documents creates a revision for every edit in the edited document.
 // A CompareOptions object has a series of flags that can suppress revisions
 // on each respective type of element, effectively ignoring their change.
 CompareOptions compareOptions = new CompareOptions();
 compareOptions.setCompareMoves(false);
 compareOptions.setIgnoreFormatting(false);
 compareOptions.setIgnoreCaseChanges(false);
 compareOptions.setIgnoreComments(false);
 compareOptions.setIgnoreTables(false);
 compareOptions.setIgnoreFields(false);
 compareOptions.setIgnoreFootnotes(false);
 compareOptions.setIgnoreTextboxes(false);
 compareOptions.setIgnoreHeadersAndFooters(false);
 compareOptions.setTarget(ComparisonTargetType.NEW);

 docOriginal.compare(docEdited, "John Doe", new Date(), compareOptions);
 docOriginal.save(getArtifactsDir() + "Revision.CompareOptions.docx");
 
```

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### getIgnoreTextboxes() {#getIgnoreTextboxes}
```
public boolean getIgnoreTextboxes()
```


Gibt an, ob Unterschiede in den in Textfeldern enthaltenen Daten verglichen werden sollen.

 **Remarks:** 

Standardmäßig werden Textfelder nicht ignoriert.

 **Examples:** 

Zeigt, wie bestimmte Arten von Dokumentelementen beim Vergleich gefiltert werden können.

```

 // Create the original document and populate it with various kinds of elements.
 Document docOriginal = new Document();
 DocumentBuilder builder = new DocumentBuilder(docOriginal);

 // Paragraph text referenced with an endnote:
 builder.writeln("Hello world! This is the first paragraph.");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Original endnote text.");

 // Table:
 builder.startTable();
 builder.insertCell();
 builder.write("Original cell 1 text");
 builder.insertCell();
 builder.write("Original cell 2 text");
 builder.endTable();

 // Textbox:
 Shape textBox = builder.insertShape(ShapeType.TEXT_BOX, 150.0, 20.0);
 builder.moveTo(textBox.getFirstParagraph());
 builder.write("Original textbox contents");

 // DATE field:
 builder.moveTo(docOriginal.getFirstSection().getBody().appendParagraph(""));
 builder.insertField(" DATE ");

 // Comment:
 Comment newComment = new Comment(docOriginal, "John Doe", "J.D.", new Date());
 newComment.setText("Original comment.");
 builder.getCurrentParagraph().appendChild(newComment);

 // Header:
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.writeln("Original header contents.");

 // Create a clone of our document and perform a quick edit on each of the cloned document's elements.
 Document docEdited = (Document)docOriginal.deepClone(true);
 Paragraph firstParagraph = docEdited.getFirstSection().getBody().getFirstParagraph();

 firstParagraph.getRuns().get(0).setText("hello world! this is the first paragraph, after editing.");
 firstParagraph.getParagraphFormat().setStyle(docEdited.getStyles().getByStyleIdentifier(StyleIdentifier.HEADING_1));
 ((Footnote)docEdited.getChild(NodeType.FOOTNOTE, 0, true)).getFirstParagraph().getRuns().get(1).setText("Edited endnote text.");
 ((Table)docEdited.getChild(NodeType.TABLE, 0, true)).getFirstRow().getCells().get(1).getFirstParagraph().getRuns().get(0).setText("Edited Cell 2 contents");
 ((Shape)docEdited.getChild(NodeType.SHAPE, 0, true)).getFirstParagraph().getRuns().get(0).setText("Edited textbox contents");
 ((FieldDate)docEdited.getRange().getFields().get(0)).setUseLunarCalendar(true);
 ((Comment)docEdited.getChild(NodeType.COMMENT, 0, true)).getFirstParagraph().getRuns().get(0).setText("Edited comment.");
 docEdited.getFirstSection().getHeadersFooters().getByHeaderFooterType(HeaderFooterType.HEADER_PRIMARY).getFirstParagraph().getRuns().get(0).setText("Edited header contents.");

 // Comparing documents creates a revision for every edit in the edited document.
 // A CompareOptions object has a series of flags that can suppress revisions
 // on each respective type of element, effectively ignoring their change.
 CompareOptions compareOptions = new CompareOptions();
 compareOptions.setCompareMoves(false);
 compareOptions.setIgnoreFormatting(false);
 compareOptions.setIgnoreCaseChanges(false);
 compareOptions.setIgnoreComments(false);
 compareOptions.setIgnoreTables(false);
 compareOptions.setIgnoreFields(false);
 compareOptions.setIgnoreFootnotes(false);
 compareOptions.setIgnoreTextboxes(false);
 compareOptions.setIgnoreHeadersAndFooters(false);
 compareOptions.setTarget(ComparisonTargetType.NEW);

 docOriginal.compare(docEdited, "John Doe", new Date(), compareOptions);
 docOriginal.save(getArtifactsDir() + "Revision.CompareOptions.docx");
 
```

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### getTarget() {#getTarget}
```
public int getTarget()
```


Gibt an, welches Dokument während des Vergleichs als Ziel verwendet werden soll.

 **Examples:** 

Zeigt, wie bestimmte Arten von Dokumentelementen beim Vergleich gefiltert werden können.

```

 // Create the original document and populate it with various kinds of elements.
 Document docOriginal = new Document();
 DocumentBuilder builder = new DocumentBuilder(docOriginal);

 // Paragraph text referenced with an endnote:
 builder.writeln("Hello world! This is the first paragraph.");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Original endnote text.");

 // Table:
 builder.startTable();
 builder.insertCell();
 builder.write("Original cell 1 text");
 builder.insertCell();
 builder.write("Original cell 2 text");
 builder.endTable();

 // Textbox:
 Shape textBox = builder.insertShape(ShapeType.TEXT_BOX, 150.0, 20.0);
 builder.moveTo(textBox.getFirstParagraph());
 builder.write("Original textbox contents");

 // DATE field:
 builder.moveTo(docOriginal.getFirstSection().getBody().appendParagraph(""));
 builder.insertField(" DATE ");

 // Comment:
 Comment newComment = new Comment(docOriginal, "John Doe", "J.D.", new Date());
 newComment.setText("Original comment.");
 builder.getCurrentParagraph().appendChild(newComment);

 // Header:
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.writeln("Original header contents.");

 // Create a clone of our document and perform a quick edit on each of the cloned document's elements.
 Document docEdited = (Document)docOriginal.deepClone(true);
 Paragraph firstParagraph = docEdited.getFirstSection().getBody().getFirstParagraph();

 firstParagraph.getRuns().get(0).setText("hello world! this is the first paragraph, after editing.");
 firstParagraph.getParagraphFormat().setStyle(docEdited.getStyles().getByStyleIdentifier(StyleIdentifier.HEADING_1));
 ((Footnote)docEdited.getChild(NodeType.FOOTNOTE, 0, true)).getFirstParagraph().getRuns().get(1).setText("Edited endnote text.");
 ((Table)docEdited.getChild(NodeType.TABLE, 0, true)).getFirstRow().getCells().get(1).getFirstParagraph().getRuns().get(0).setText("Edited Cell 2 contents");
 ((Shape)docEdited.getChild(NodeType.SHAPE, 0, true)).getFirstParagraph().getRuns().get(0).setText("Edited textbox contents");
 ((FieldDate)docEdited.getRange().getFields().get(0)).setUseLunarCalendar(true);
 ((Comment)docEdited.getChild(NodeType.COMMENT, 0, true)).getFirstParagraph().getRuns().get(0).setText("Edited comment.");
 docEdited.getFirstSection().getHeadersFooters().getByHeaderFooterType(HeaderFooterType.HEADER_PRIMARY).getFirstParagraph().getRuns().get(0).setText("Edited header contents.");

 // Comparing documents creates a revision for every edit in the edited document.
 // A CompareOptions object has a series of flags that can suppress revisions
 // on each respective type of element, effectively ignoring their change.
 CompareOptions compareOptions = new CompareOptions();
 compareOptions.setCompareMoves(false);
 compareOptions.setIgnoreFormatting(false);
 compareOptions.setIgnoreCaseChanges(false);
 compareOptions.setIgnoreComments(false);
 compareOptions.setIgnoreTables(false);
 compareOptions.setIgnoreFields(false);
 compareOptions.setIgnoreFootnotes(false);
 compareOptions.setIgnoreTextboxes(false);
 compareOptions.setIgnoreHeadersAndFooters(false);
 compareOptions.setTarget(ComparisonTargetType.NEW);

 docOriginal.compare(docEdited, "John Doe", new Date(), compareOptions);
 docOriginal.save(getArtifactsDir() + "Revision.CompareOptions.docx");
 
```

**Returns:**
int - Der entsprechende  int  Wert. Der zurückgegebene Wert ist einer der [ComparisonTargetType](../../com.aspose.words/comparisontargettype/) Konstanten.
### setCompareMoves(boolean value) {#setCompareMoves-boolean}
```
public void setCompareMoves(boolean value)
```


Gibt an, ob Unterschiede zwischen den beiden Dokumenten verglichen werden sollen.

 **Remarks:** 

Standardmäßig werden Verschiebungsrevisionen nicht erzeugt.

 **Examples:** 

Zeigt, wie bestimmte Arten von Dokumentelementen beim Vergleich gefiltert werden können.

```

 // Create the original document and populate it with various kinds of elements.
 Document docOriginal = new Document();
 DocumentBuilder builder = new DocumentBuilder(docOriginal);

 // Paragraph text referenced with an endnote:
 builder.writeln("Hello world! This is the first paragraph.");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Original endnote text.");

 // Table:
 builder.startTable();
 builder.insertCell();
 builder.write("Original cell 1 text");
 builder.insertCell();
 builder.write("Original cell 2 text");
 builder.endTable();

 // Textbox:
 Shape textBox = builder.insertShape(ShapeType.TEXT_BOX, 150.0, 20.0);
 builder.moveTo(textBox.getFirstParagraph());
 builder.write("Original textbox contents");

 // DATE field:
 builder.moveTo(docOriginal.getFirstSection().getBody().appendParagraph(""));
 builder.insertField(" DATE ");

 // Comment:
 Comment newComment = new Comment(docOriginal, "John Doe", "J.D.", new Date());
 newComment.setText("Original comment.");
 builder.getCurrentParagraph().appendChild(newComment);

 // Header:
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.writeln("Original header contents.");

 // Create a clone of our document and perform a quick edit on each of the cloned document's elements.
 Document docEdited = (Document)docOriginal.deepClone(true);
 Paragraph firstParagraph = docEdited.getFirstSection().getBody().getFirstParagraph();

 firstParagraph.getRuns().get(0).setText("hello world! this is the first paragraph, after editing.");
 firstParagraph.getParagraphFormat().setStyle(docEdited.getStyles().getByStyleIdentifier(StyleIdentifier.HEADING_1));
 ((Footnote)docEdited.getChild(NodeType.FOOTNOTE, 0, true)).getFirstParagraph().getRuns().get(1).setText("Edited endnote text.");
 ((Table)docEdited.getChild(NodeType.TABLE, 0, true)).getFirstRow().getCells().get(1).getFirstParagraph().getRuns().get(0).setText("Edited Cell 2 contents");
 ((Shape)docEdited.getChild(NodeType.SHAPE, 0, true)).getFirstParagraph().getRuns().get(0).setText("Edited textbox contents");
 ((FieldDate)docEdited.getRange().getFields().get(0)).setUseLunarCalendar(true);
 ((Comment)docEdited.getChild(NodeType.COMMENT, 0, true)).getFirstParagraph().getRuns().get(0).setText("Edited comment.");
 docEdited.getFirstSection().getHeadersFooters().getByHeaderFooterType(HeaderFooterType.HEADER_PRIMARY).getFirstParagraph().getRuns().get(0).setText("Edited header contents.");

 // Comparing documents creates a revision for every edit in the edited document.
 // A CompareOptions object has a series of flags that can suppress revisions
 // on each respective type of element, effectively ignoring their change.
 CompareOptions compareOptions = new CompareOptions();
 compareOptions.setCompareMoves(false);
 compareOptions.setIgnoreFormatting(false);
 compareOptions.setIgnoreCaseChanges(false);
 compareOptions.setIgnoreComments(false);
 compareOptions.setIgnoreTables(false);
 compareOptions.setIgnoreFields(false);
 compareOptions.setIgnoreFootnotes(false);
 compareOptions.setIgnoreTextboxes(false);
 compareOptions.setIgnoreHeadersAndFooters(false);
 compareOptions.setTarget(ComparisonTargetType.NEW);

 docOriginal.compare(docEdited, "John Doe", new Date(), compareOptions);
 docOriginal.save(getArtifactsDir() + "Revision.CompareOptions.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setGranularity(int value) {#setGranularity-int}
```
public void setGranularity(int value)
```


Gibt an, ob Änderungen Zeichenweise oder Wortweise nachverfolgt werden.

 **Remarks:** 

Standardwert ist [Granularity.WORD\_LEVEL](../../com.aspose.words/granularity/\#WORD-LEVEL).

 **Examples:** 

Zeigt, wie man eine Granularität beim Vergleich von Dokumenten angibt.

```

 Document docA = new Document();
 DocumentBuilder builderA = new DocumentBuilder(docA);
 builderA.writeln("Alpha Lorem ipsum dolor sit amet, consectetur adipiscing elit");

 Document docB = new Document();
 DocumentBuilder builderB = new DocumentBuilder(docB);
 builderB.writeln("Lorems ipsum dolor sit amet consectetur - \"adipiscing\" elit");

 // Specify whether changes are tracking
 // by character ('Granularity.CharLevel'), or by word ('Granularity.WordLevel').
 CompareOptions compareOptions = new CompareOptions();
 compareOptions.setGranularity(granularity);

 docA.compare(docB, "author", new Date(), compareOptions);

 // The first document's collection of revision groups contains all the differences between documents.
 RevisionGroupCollection groups = docA.getRevisions().getGroups();
 Assert.assertEquals(5, groups.getCount());
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Der entsprechende  int  Wert. Der Wert muss einer der [Granularity](../../com.aspose.words/granularity/) Konstanten sein. |

### setIgnoreCaseChanges(boolean value) {#setIgnoreCaseChanges-boolean}
```
public void setIgnoreCaseChanges(boolean value)
```


True gibt an, dass der Dokumentvergleich nicht zwischen Groß- und Kleinschreibung unterscheidet.

 **Remarks:** 

Standardmäßig ist der Vergleich groß‑ und kleinschreibungssensitiv.

 **Examples:** 

Zeigt, wie bestimmte Arten von Dokumentelementen beim Vergleich gefiltert werden können.

```

 // Create the original document and populate it with various kinds of elements.
 Document docOriginal = new Document();
 DocumentBuilder builder = new DocumentBuilder(docOriginal);

 // Paragraph text referenced with an endnote:
 builder.writeln("Hello world! This is the first paragraph.");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Original endnote text.");

 // Table:
 builder.startTable();
 builder.insertCell();
 builder.write("Original cell 1 text");
 builder.insertCell();
 builder.write("Original cell 2 text");
 builder.endTable();

 // Textbox:
 Shape textBox = builder.insertShape(ShapeType.TEXT_BOX, 150.0, 20.0);
 builder.moveTo(textBox.getFirstParagraph());
 builder.write("Original textbox contents");

 // DATE field:
 builder.moveTo(docOriginal.getFirstSection().getBody().appendParagraph(""));
 builder.insertField(" DATE ");

 // Comment:
 Comment newComment = new Comment(docOriginal, "John Doe", "J.D.", new Date());
 newComment.setText("Original comment.");
 builder.getCurrentParagraph().appendChild(newComment);

 // Header:
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.writeln("Original header contents.");

 // Create a clone of our document and perform a quick edit on each of the cloned document's elements.
 Document docEdited = (Document)docOriginal.deepClone(true);
 Paragraph firstParagraph = docEdited.getFirstSection().getBody().getFirstParagraph();

 firstParagraph.getRuns().get(0).setText("hello world! this is the first paragraph, after editing.");
 firstParagraph.getParagraphFormat().setStyle(docEdited.getStyles().getByStyleIdentifier(StyleIdentifier.HEADING_1));
 ((Footnote)docEdited.getChild(NodeType.FOOTNOTE, 0, true)).getFirstParagraph().getRuns().get(1).setText("Edited endnote text.");
 ((Table)docEdited.getChild(NodeType.TABLE, 0, true)).getFirstRow().getCells().get(1).getFirstParagraph().getRuns().get(0).setText("Edited Cell 2 contents");
 ((Shape)docEdited.getChild(NodeType.SHAPE, 0, true)).getFirstParagraph().getRuns().get(0).setText("Edited textbox contents");
 ((FieldDate)docEdited.getRange().getFields().get(0)).setUseLunarCalendar(true);
 ((Comment)docEdited.getChild(NodeType.COMMENT, 0, true)).getFirstParagraph().getRuns().get(0).setText("Edited comment.");
 docEdited.getFirstSection().getHeadersFooters().getByHeaderFooterType(HeaderFooterType.HEADER_PRIMARY).getFirstParagraph().getRuns().get(0).setText("Edited header contents.");

 // Comparing documents creates a revision for every edit in the edited document.
 // A CompareOptions object has a series of flags that can suppress revisions
 // on each respective type of element, effectively ignoring their change.
 CompareOptions compareOptions = new CompareOptions();
 compareOptions.setCompareMoves(false);
 compareOptions.setIgnoreFormatting(false);
 compareOptions.setIgnoreCaseChanges(false);
 compareOptions.setIgnoreComments(false);
 compareOptions.setIgnoreTables(false);
 compareOptions.setIgnoreFields(false);
 compareOptions.setIgnoreFootnotes(false);
 compareOptions.setIgnoreTextboxes(false);
 compareOptions.setIgnoreHeadersAndFooters(false);
 compareOptions.setTarget(ComparisonTargetType.NEW);

 docOriginal.compare(docEdited, "John Doe", new Date(), compareOptions);
 docOriginal.save(getArtifactsDir() + "Revision.CompareOptions.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setIgnoreComments(boolean value) {#setIgnoreComments-boolean}
```
public void setIgnoreComments(boolean value)
```


Gibt an, ob Unterschiede in Kommentaren verglichen werden sollen.

 **Remarks:** 

Standardmäßig werden Kommentare nicht ignoriert.

 **Examples:** 

Zeigt, wie bestimmte Arten von Dokumentelementen beim Vergleich gefiltert werden können.

```

 // Create the original document and populate it with various kinds of elements.
 Document docOriginal = new Document();
 DocumentBuilder builder = new DocumentBuilder(docOriginal);

 // Paragraph text referenced with an endnote:
 builder.writeln("Hello world! This is the first paragraph.");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Original endnote text.");

 // Table:
 builder.startTable();
 builder.insertCell();
 builder.write("Original cell 1 text");
 builder.insertCell();
 builder.write("Original cell 2 text");
 builder.endTable();

 // Textbox:
 Shape textBox = builder.insertShape(ShapeType.TEXT_BOX, 150.0, 20.0);
 builder.moveTo(textBox.getFirstParagraph());
 builder.write("Original textbox contents");

 // DATE field:
 builder.moveTo(docOriginal.getFirstSection().getBody().appendParagraph(""));
 builder.insertField(" DATE ");

 // Comment:
 Comment newComment = new Comment(docOriginal, "John Doe", "J.D.", new Date());
 newComment.setText("Original comment.");
 builder.getCurrentParagraph().appendChild(newComment);

 // Header:
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.writeln("Original header contents.");

 // Create a clone of our document and perform a quick edit on each of the cloned document's elements.
 Document docEdited = (Document)docOriginal.deepClone(true);
 Paragraph firstParagraph = docEdited.getFirstSection().getBody().getFirstParagraph();

 firstParagraph.getRuns().get(0).setText("hello world! this is the first paragraph, after editing.");
 firstParagraph.getParagraphFormat().setStyle(docEdited.getStyles().getByStyleIdentifier(StyleIdentifier.HEADING_1));
 ((Footnote)docEdited.getChild(NodeType.FOOTNOTE, 0, true)).getFirstParagraph().getRuns().get(1).setText("Edited endnote text.");
 ((Table)docEdited.getChild(NodeType.TABLE, 0, true)).getFirstRow().getCells().get(1).getFirstParagraph().getRuns().get(0).setText("Edited Cell 2 contents");
 ((Shape)docEdited.getChild(NodeType.SHAPE, 0, true)).getFirstParagraph().getRuns().get(0).setText("Edited textbox contents");
 ((FieldDate)docEdited.getRange().getFields().get(0)).setUseLunarCalendar(true);
 ((Comment)docEdited.getChild(NodeType.COMMENT, 0, true)).getFirstParagraph().getRuns().get(0).setText("Edited comment.");
 docEdited.getFirstSection().getHeadersFooters().getByHeaderFooterType(HeaderFooterType.HEADER_PRIMARY).getFirstParagraph().getRuns().get(0).setText("Edited header contents.");

 // Comparing documents creates a revision for every edit in the edited document.
 // A CompareOptions object has a series of flags that can suppress revisions
 // on each respective type of element, effectively ignoring their change.
 CompareOptions compareOptions = new CompareOptions();
 compareOptions.setCompareMoves(false);
 compareOptions.setIgnoreFormatting(false);
 compareOptions.setIgnoreCaseChanges(false);
 compareOptions.setIgnoreComments(false);
 compareOptions.setIgnoreTables(false);
 compareOptions.setIgnoreFields(false);
 compareOptions.setIgnoreFootnotes(false);
 compareOptions.setIgnoreTextboxes(false);
 compareOptions.setIgnoreHeadersAndFooters(false);
 compareOptions.setTarget(ComparisonTargetType.NEW);

 docOriginal.compare(docEdited, "John Doe", new Date(), compareOptions);
 docOriginal.save(getArtifactsDir() + "Revision.CompareOptions.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setIgnoreDmlUniqueId(boolean value) {#setIgnoreDmlUniqueId-boolean}
```
public void setIgnoreDmlUniqueId(boolean value)
```


Gibt an, ob Unterschiede in der eindeutigen DrawingML‑ID ignoriert werden sollen.

 **Remarks:** 

Standardwert ist false.

 **Examples:** 

Zeigt, wie man Dokumente vergleicht, wobei die eindeutige DML‑ID ignoriert wird.

```

 Document docA = new Document(getMyDir() + "DML unique ID original.docx");
 Document docB = new Document(getMyDir() + "DML unique ID compare.docx");

 // By default, Aspose.Words do not ignore DML's unique ID, and the revisions count was 2.
 // If we are ignoring DML's unique ID, and revisions count were 0.
 CompareOptions compareOptions = new CompareOptions();
 compareOptions.getAdvancedOptions().setIgnoreDmlUniqueId(isIgnoreDmlUniqueId);

 docA.compare(docB, "Aspose.Words", new Date(), compareOptions);

 Assert.assertEquals(isIgnoreDmlUniqueId ? 1 : 3, docA.getRevisions().getCount());
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setIgnoreFields(boolean value) {#setIgnoreFields-boolean}
```
public void setIgnoreFields(boolean value)
```


Gibt an, ob Unterschiede in Feldern verglichen werden sollen.

 **Remarks:** 

Standardmäßig werden Felder nicht ignoriert.

 **Examples:** 

Zeigt, wie bestimmte Arten von Dokumentelementen beim Vergleich gefiltert werden können.

```

 // Create the original document and populate it with various kinds of elements.
 Document docOriginal = new Document();
 DocumentBuilder builder = new DocumentBuilder(docOriginal);

 // Paragraph text referenced with an endnote:
 builder.writeln("Hello world! This is the first paragraph.");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Original endnote text.");

 // Table:
 builder.startTable();
 builder.insertCell();
 builder.write("Original cell 1 text");
 builder.insertCell();
 builder.write("Original cell 2 text");
 builder.endTable();

 // Textbox:
 Shape textBox = builder.insertShape(ShapeType.TEXT_BOX, 150.0, 20.0);
 builder.moveTo(textBox.getFirstParagraph());
 builder.write("Original textbox contents");

 // DATE field:
 builder.moveTo(docOriginal.getFirstSection().getBody().appendParagraph(""));
 builder.insertField(" DATE ");

 // Comment:
 Comment newComment = new Comment(docOriginal, "John Doe", "J.D.", new Date());
 newComment.setText("Original comment.");
 builder.getCurrentParagraph().appendChild(newComment);

 // Header:
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.writeln("Original header contents.");

 // Create a clone of our document and perform a quick edit on each of the cloned document's elements.
 Document docEdited = (Document)docOriginal.deepClone(true);
 Paragraph firstParagraph = docEdited.getFirstSection().getBody().getFirstParagraph();

 firstParagraph.getRuns().get(0).setText("hello world! this is the first paragraph, after editing.");
 firstParagraph.getParagraphFormat().setStyle(docEdited.getStyles().getByStyleIdentifier(StyleIdentifier.HEADING_1));
 ((Footnote)docEdited.getChild(NodeType.FOOTNOTE, 0, true)).getFirstParagraph().getRuns().get(1).setText("Edited endnote text.");
 ((Table)docEdited.getChild(NodeType.TABLE, 0, true)).getFirstRow().getCells().get(1).getFirstParagraph().getRuns().get(0).setText("Edited Cell 2 contents");
 ((Shape)docEdited.getChild(NodeType.SHAPE, 0, true)).getFirstParagraph().getRuns().get(0).setText("Edited textbox contents");
 ((FieldDate)docEdited.getRange().getFields().get(0)).setUseLunarCalendar(true);
 ((Comment)docEdited.getChild(NodeType.COMMENT, 0, true)).getFirstParagraph().getRuns().get(0).setText("Edited comment.");
 docEdited.getFirstSection().getHeadersFooters().getByHeaderFooterType(HeaderFooterType.HEADER_PRIMARY).getFirstParagraph().getRuns().get(0).setText("Edited header contents.");

 // Comparing documents creates a revision for every edit in the edited document.
 // A CompareOptions object has a series of flags that can suppress revisions
 // on each respective type of element, effectively ignoring their change.
 CompareOptions compareOptions = new CompareOptions();
 compareOptions.setCompareMoves(false);
 compareOptions.setIgnoreFormatting(false);
 compareOptions.setIgnoreCaseChanges(false);
 compareOptions.setIgnoreComments(false);
 compareOptions.setIgnoreTables(false);
 compareOptions.setIgnoreFields(false);
 compareOptions.setIgnoreFootnotes(false);
 compareOptions.setIgnoreTextboxes(false);
 compareOptions.setIgnoreHeadersAndFooters(false);
 compareOptions.setTarget(ComparisonTargetType.NEW);

 docOriginal.compare(docEdited, "John Doe", new Date(), compareOptions);
 docOriginal.save(getArtifactsDir() + "Revision.CompareOptions.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setIgnoreFootnotes(boolean value) {#setIgnoreFootnotes-boolean}
```
public void setIgnoreFootnotes(boolean value)
```


Gibt an, ob Unterschiede in Fußnoten und Endnoten verglichen werden sollen.

 **Remarks:** 

Standardmäßig werden Fußnoten nicht ignoriert.

 **Examples:** 

Zeigt, wie bestimmte Arten von Dokumentelementen beim Vergleich gefiltert werden können.

```

 // Create the original document and populate it with various kinds of elements.
 Document docOriginal = new Document();
 DocumentBuilder builder = new DocumentBuilder(docOriginal);

 // Paragraph text referenced with an endnote:
 builder.writeln("Hello world! This is the first paragraph.");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Original endnote text.");

 // Table:
 builder.startTable();
 builder.insertCell();
 builder.write("Original cell 1 text");
 builder.insertCell();
 builder.write("Original cell 2 text");
 builder.endTable();

 // Textbox:
 Shape textBox = builder.insertShape(ShapeType.TEXT_BOX, 150.0, 20.0);
 builder.moveTo(textBox.getFirstParagraph());
 builder.write("Original textbox contents");

 // DATE field:
 builder.moveTo(docOriginal.getFirstSection().getBody().appendParagraph(""));
 builder.insertField(" DATE ");

 // Comment:
 Comment newComment = new Comment(docOriginal, "John Doe", "J.D.", new Date());
 newComment.setText("Original comment.");
 builder.getCurrentParagraph().appendChild(newComment);

 // Header:
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.writeln("Original header contents.");

 // Create a clone of our document and perform a quick edit on each of the cloned document's elements.
 Document docEdited = (Document)docOriginal.deepClone(true);
 Paragraph firstParagraph = docEdited.getFirstSection().getBody().getFirstParagraph();

 firstParagraph.getRuns().get(0).setText("hello world! this is the first paragraph, after editing.");
 firstParagraph.getParagraphFormat().setStyle(docEdited.getStyles().getByStyleIdentifier(StyleIdentifier.HEADING_1));
 ((Footnote)docEdited.getChild(NodeType.FOOTNOTE, 0, true)).getFirstParagraph().getRuns().get(1).setText("Edited endnote text.");
 ((Table)docEdited.getChild(NodeType.TABLE, 0, true)).getFirstRow().getCells().get(1).getFirstParagraph().getRuns().get(0).setText("Edited Cell 2 contents");
 ((Shape)docEdited.getChild(NodeType.SHAPE, 0, true)).getFirstParagraph().getRuns().get(0).setText("Edited textbox contents");
 ((FieldDate)docEdited.getRange().getFields().get(0)).setUseLunarCalendar(true);
 ((Comment)docEdited.getChild(NodeType.COMMENT, 0, true)).getFirstParagraph().getRuns().get(0).setText("Edited comment.");
 docEdited.getFirstSection().getHeadersFooters().getByHeaderFooterType(HeaderFooterType.HEADER_PRIMARY).getFirstParagraph().getRuns().get(0).setText("Edited header contents.");

 // Comparing documents creates a revision for every edit in the edited document.
 // A CompareOptions object has a series of flags that can suppress revisions
 // on each respective type of element, effectively ignoring their change.
 CompareOptions compareOptions = new CompareOptions();
 compareOptions.setCompareMoves(false);
 compareOptions.setIgnoreFormatting(false);
 compareOptions.setIgnoreCaseChanges(false);
 compareOptions.setIgnoreComments(false);
 compareOptions.setIgnoreTables(false);
 compareOptions.setIgnoreFields(false);
 compareOptions.setIgnoreFootnotes(false);
 compareOptions.setIgnoreTextboxes(false);
 compareOptions.setIgnoreHeadersAndFooters(false);
 compareOptions.setTarget(ComparisonTargetType.NEW);

 docOriginal.compare(docEdited, "John Doe", new Date(), compareOptions);
 docOriginal.save(getArtifactsDir() + "Revision.CompareOptions.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setIgnoreFormatting(boolean value) {#setIgnoreFormatting-boolean}
```
public void setIgnoreFormatting(boolean value)
```


True gibt an, dass die Formatierung ignoriert wird.

 **Remarks:** 

Standardmäßig wird die Dokumentformatierung nicht ignoriert.

 **Examples:** 

Zeigt, wie bestimmte Arten von Dokumentelementen beim Vergleich gefiltert werden können.

```

 // Create the original document and populate it with various kinds of elements.
 Document docOriginal = new Document();
 DocumentBuilder builder = new DocumentBuilder(docOriginal);

 // Paragraph text referenced with an endnote:
 builder.writeln("Hello world! This is the first paragraph.");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Original endnote text.");

 // Table:
 builder.startTable();
 builder.insertCell();
 builder.write("Original cell 1 text");
 builder.insertCell();
 builder.write("Original cell 2 text");
 builder.endTable();

 // Textbox:
 Shape textBox = builder.insertShape(ShapeType.TEXT_BOX, 150.0, 20.0);
 builder.moveTo(textBox.getFirstParagraph());
 builder.write("Original textbox contents");

 // DATE field:
 builder.moveTo(docOriginal.getFirstSection().getBody().appendParagraph(""));
 builder.insertField(" DATE ");

 // Comment:
 Comment newComment = new Comment(docOriginal, "John Doe", "J.D.", new Date());
 newComment.setText("Original comment.");
 builder.getCurrentParagraph().appendChild(newComment);

 // Header:
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.writeln("Original header contents.");

 // Create a clone of our document and perform a quick edit on each of the cloned document's elements.
 Document docEdited = (Document)docOriginal.deepClone(true);
 Paragraph firstParagraph = docEdited.getFirstSection().getBody().getFirstParagraph();

 firstParagraph.getRuns().get(0).setText("hello world! this is the first paragraph, after editing.");
 firstParagraph.getParagraphFormat().setStyle(docEdited.getStyles().getByStyleIdentifier(StyleIdentifier.HEADING_1));
 ((Footnote)docEdited.getChild(NodeType.FOOTNOTE, 0, true)).getFirstParagraph().getRuns().get(1).setText("Edited endnote text.");
 ((Table)docEdited.getChild(NodeType.TABLE, 0, true)).getFirstRow().getCells().get(1).getFirstParagraph().getRuns().get(0).setText("Edited Cell 2 contents");
 ((Shape)docEdited.getChild(NodeType.SHAPE, 0, true)).getFirstParagraph().getRuns().get(0).setText("Edited textbox contents");
 ((FieldDate)docEdited.getRange().getFields().get(0)).setUseLunarCalendar(true);
 ((Comment)docEdited.getChild(NodeType.COMMENT, 0, true)).getFirstParagraph().getRuns().get(0).setText("Edited comment.");
 docEdited.getFirstSection().getHeadersFooters().getByHeaderFooterType(HeaderFooterType.HEADER_PRIMARY).getFirstParagraph().getRuns().get(0).setText("Edited header contents.");

 // Comparing documents creates a revision for every edit in the edited document.
 // A CompareOptions object has a series of flags that can suppress revisions
 // on each respective type of element, effectively ignoring their change.
 CompareOptions compareOptions = new CompareOptions();
 compareOptions.setCompareMoves(false);
 compareOptions.setIgnoreFormatting(false);
 compareOptions.setIgnoreCaseChanges(false);
 compareOptions.setIgnoreComments(false);
 compareOptions.setIgnoreTables(false);
 compareOptions.setIgnoreFields(false);
 compareOptions.setIgnoreFootnotes(false);
 compareOptions.setIgnoreTextboxes(false);
 compareOptions.setIgnoreHeadersAndFooters(false);
 compareOptions.setTarget(ComparisonTargetType.NEW);

 docOriginal.compare(docEdited, "John Doe", new Date(), compareOptions);
 docOriginal.save(getArtifactsDir() + "Revision.CompareOptions.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setIgnoreHeadersAndFooters(boolean value) {#setIgnoreHeadersAndFooters-boolean}
```
public void setIgnoreHeadersAndFooters(boolean value)
```


True gibt an, dass der Inhalt von Kopf‑ und Fußzeilen ignoriert wird.

 **Remarks:** 

Standardmäßig werden Kopf‑ und Fußzeilen nicht ignoriert.

 **Examples:** 

Zeigt, wie bestimmte Arten von Dokumentelementen beim Vergleich gefiltert werden können.

```

 // Create the original document and populate it with various kinds of elements.
 Document docOriginal = new Document();
 DocumentBuilder builder = new DocumentBuilder(docOriginal);

 // Paragraph text referenced with an endnote:
 builder.writeln("Hello world! This is the first paragraph.");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Original endnote text.");

 // Table:
 builder.startTable();
 builder.insertCell();
 builder.write("Original cell 1 text");
 builder.insertCell();
 builder.write("Original cell 2 text");
 builder.endTable();

 // Textbox:
 Shape textBox = builder.insertShape(ShapeType.TEXT_BOX, 150.0, 20.0);
 builder.moveTo(textBox.getFirstParagraph());
 builder.write("Original textbox contents");

 // DATE field:
 builder.moveTo(docOriginal.getFirstSection().getBody().appendParagraph(""));
 builder.insertField(" DATE ");

 // Comment:
 Comment newComment = new Comment(docOriginal, "John Doe", "J.D.", new Date());
 newComment.setText("Original comment.");
 builder.getCurrentParagraph().appendChild(newComment);

 // Header:
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.writeln("Original header contents.");

 // Create a clone of our document and perform a quick edit on each of the cloned document's elements.
 Document docEdited = (Document)docOriginal.deepClone(true);
 Paragraph firstParagraph = docEdited.getFirstSection().getBody().getFirstParagraph();

 firstParagraph.getRuns().get(0).setText("hello world! this is the first paragraph, after editing.");
 firstParagraph.getParagraphFormat().setStyle(docEdited.getStyles().getByStyleIdentifier(StyleIdentifier.HEADING_1));
 ((Footnote)docEdited.getChild(NodeType.FOOTNOTE, 0, true)).getFirstParagraph().getRuns().get(1).setText("Edited endnote text.");
 ((Table)docEdited.getChild(NodeType.TABLE, 0, true)).getFirstRow().getCells().get(1).getFirstParagraph().getRuns().get(0).setText("Edited Cell 2 contents");
 ((Shape)docEdited.getChild(NodeType.SHAPE, 0, true)).getFirstParagraph().getRuns().get(0).setText("Edited textbox contents");
 ((FieldDate)docEdited.getRange().getFields().get(0)).setUseLunarCalendar(true);
 ((Comment)docEdited.getChild(NodeType.COMMENT, 0, true)).getFirstParagraph().getRuns().get(0).setText("Edited comment.");
 docEdited.getFirstSection().getHeadersFooters().getByHeaderFooterType(HeaderFooterType.HEADER_PRIMARY).getFirstParagraph().getRuns().get(0).setText("Edited header contents.");

 // Comparing documents creates a revision for every edit in the edited document.
 // A CompareOptions object has a series of flags that can suppress revisions
 // on each respective type of element, effectively ignoring their change.
 CompareOptions compareOptions = new CompareOptions();
 compareOptions.setCompareMoves(false);
 compareOptions.setIgnoreFormatting(false);
 compareOptions.setIgnoreCaseChanges(false);
 compareOptions.setIgnoreComments(false);
 compareOptions.setIgnoreTables(false);
 compareOptions.setIgnoreFields(false);
 compareOptions.setIgnoreFootnotes(false);
 compareOptions.setIgnoreTextboxes(false);
 compareOptions.setIgnoreHeadersAndFooters(false);
 compareOptions.setTarget(ComparisonTargetType.NEW);

 docOriginal.compare(docEdited, "John Doe", new Date(), compareOptions);
 docOriginal.save(getArtifactsDir() + "Revision.CompareOptions.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setIgnoreTables(boolean value) {#setIgnoreTables-boolean}
```
public void setIgnoreTables(boolean value)
```


Gibt an, ob Unterschiede in den in Tabellen enthaltenen Daten verglichen werden sollen.

 **Remarks:** 

Standardmäßig werden Tabellen nicht ignoriert.

 **Examples:** 

Zeigt, wie bestimmte Arten von Dokumentelementen beim Vergleich gefiltert werden können.

```

 // Create the original document and populate it with various kinds of elements.
 Document docOriginal = new Document();
 DocumentBuilder builder = new DocumentBuilder(docOriginal);

 // Paragraph text referenced with an endnote:
 builder.writeln("Hello world! This is the first paragraph.");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Original endnote text.");

 // Table:
 builder.startTable();
 builder.insertCell();
 builder.write("Original cell 1 text");
 builder.insertCell();
 builder.write("Original cell 2 text");
 builder.endTable();

 // Textbox:
 Shape textBox = builder.insertShape(ShapeType.TEXT_BOX, 150.0, 20.0);
 builder.moveTo(textBox.getFirstParagraph());
 builder.write("Original textbox contents");

 // DATE field:
 builder.moveTo(docOriginal.getFirstSection().getBody().appendParagraph(""));
 builder.insertField(" DATE ");

 // Comment:
 Comment newComment = new Comment(docOriginal, "John Doe", "J.D.", new Date());
 newComment.setText("Original comment.");
 builder.getCurrentParagraph().appendChild(newComment);

 // Header:
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.writeln("Original header contents.");

 // Create a clone of our document and perform a quick edit on each of the cloned document's elements.
 Document docEdited = (Document)docOriginal.deepClone(true);
 Paragraph firstParagraph = docEdited.getFirstSection().getBody().getFirstParagraph();

 firstParagraph.getRuns().get(0).setText("hello world! this is the first paragraph, after editing.");
 firstParagraph.getParagraphFormat().setStyle(docEdited.getStyles().getByStyleIdentifier(StyleIdentifier.HEADING_1));
 ((Footnote)docEdited.getChild(NodeType.FOOTNOTE, 0, true)).getFirstParagraph().getRuns().get(1).setText("Edited endnote text.");
 ((Table)docEdited.getChild(NodeType.TABLE, 0, true)).getFirstRow().getCells().get(1).getFirstParagraph().getRuns().get(0).setText("Edited Cell 2 contents");
 ((Shape)docEdited.getChild(NodeType.SHAPE, 0, true)).getFirstParagraph().getRuns().get(0).setText("Edited textbox contents");
 ((FieldDate)docEdited.getRange().getFields().get(0)).setUseLunarCalendar(true);
 ((Comment)docEdited.getChild(NodeType.COMMENT, 0, true)).getFirstParagraph().getRuns().get(0).setText("Edited comment.");
 docEdited.getFirstSection().getHeadersFooters().getByHeaderFooterType(HeaderFooterType.HEADER_PRIMARY).getFirstParagraph().getRuns().get(0).setText("Edited header contents.");

 // Comparing documents creates a revision for every edit in the edited document.
 // A CompareOptions object has a series of flags that can suppress revisions
 // on each respective type of element, effectively ignoring their change.
 CompareOptions compareOptions = new CompareOptions();
 compareOptions.setCompareMoves(false);
 compareOptions.setIgnoreFormatting(false);
 compareOptions.setIgnoreCaseChanges(false);
 compareOptions.setIgnoreComments(false);
 compareOptions.setIgnoreTables(false);
 compareOptions.setIgnoreFields(false);
 compareOptions.setIgnoreFootnotes(false);
 compareOptions.setIgnoreTextboxes(false);
 compareOptions.setIgnoreHeadersAndFooters(false);
 compareOptions.setTarget(ComparisonTargetType.NEW);

 docOriginal.compare(docEdited, "John Doe", new Date(), compareOptions);
 docOriginal.save(getArtifactsDir() + "Revision.CompareOptions.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setIgnoreTextboxes(boolean value) {#setIgnoreTextboxes-boolean}
```
public void setIgnoreTextboxes(boolean value)
```


Gibt an, ob Unterschiede in den in Textfeldern enthaltenen Daten verglichen werden sollen.

 **Remarks:** 

Standardmäßig werden Textfelder nicht ignoriert.

 **Examples:** 

Zeigt, wie bestimmte Arten von Dokumentelementen beim Vergleich gefiltert werden können.

```

 // Create the original document and populate it with various kinds of elements.
 Document docOriginal = new Document();
 DocumentBuilder builder = new DocumentBuilder(docOriginal);

 // Paragraph text referenced with an endnote:
 builder.writeln("Hello world! This is the first paragraph.");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Original endnote text.");

 // Table:
 builder.startTable();
 builder.insertCell();
 builder.write("Original cell 1 text");
 builder.insertCell();
 builder.write("Original cell 2 text");
 builder.endTable();

 // Textbox:
 Shape textBox = builder.insertShape(ShapeType.TEXT_BOX, 150.0, 20.0);
 builder.moveTo(textBox.getFirstParagraph());
 builder.write("Original textbox contents");

 // DATE field:
 builder.moveTo(docOriginal.getFirstSection().getBody().appendParagraph(""));
 builder.insertField(" DATE ");

 // Comment:
 Comment newComment = new Comment(docOriginal, "John Doe", "J.D.", new Date());
 newComment.setText("Original comment.");
 builder.getCurrentParagraph().appendChild(newComment);

 // Header:
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.writeln("Original header contents.");

 // Create a clone of our document and perform a quick edit on each of the cloned document's elements.
 Document docEdited = (Document)docOriginal.deepClone(true);
 Paragraph firstParagraph = docEdited.getFirstSection().getBody().getFirstParagraph();

 firstParagraph.getRuns().get(0).setText("hello world! this is the first paragraph, after editing.");
 firstParagraph.getParagraphFormat().setStyle(docEdited.getStyles().getByStyleIdentifier(StyleIdentifier.HEADING_1));
 ((Footnote)docEdited.getChild(NodeType.FOOTNOTE, 0, true)).getFirstParagraph().getRuns().get(1).setText("Edited endnote text.");
 ((Table)docEdited.getChild(NodeType.TABLE, 0, true)).getFirstRow().getCells().get(1).getFirstParagraph().getRuns().get(0).setText("Edited Cell 2 contents");
 ((Shape)docEdited.getChild(NodeType.SHAPE, 0, true)).getFirstParagraph().getRuns().get(0).setText("Edited textbox contents");
 ((FieldDate)docEdited.getRange().getFields().get(0)).setUseLunarCalendar(true);
 ((Comment)docEdited.getChild(NodeType.COMMENT, 0, true)).getFirstParagraph().getRuns().get(0).setText("Edited comment.");
 docEdited.getFirstSection().getHeadersFooters().getByHeaderFooterType(HeaderFooterType.HEADER_PRIMARY).getFirstParagraph().getRuns().get(0).setText("Edited header contents.");

 // Comparing documents creates a revision for every edit in the edited document.
 // A CompareOptions object has a series of flags that can suppress revisions
 // on each respective type of element, effectively ignoring their change.
 CompareOptions compareOptions = new CompareOptions();
 compareOptions.setCompareMoves(false);
 compareOptions.setIgnoreFormatting(false);
 compareOptions.setIgnoreCaseChanges(false);
 compareOptions.setIgnoreComments(false);
 compareOptions.setIgnoreTables(false);
 compareOptions.setIgnoreFields(false);
 compareOptions.setIgnoreFootnotes(false);
 compareOptions.setIgnoreTextboxes(false);
 compareOptions.setIgnoreHeadersAndFooters(false);
 compareOptions.setTarget(ComparisonTargetType.NEW);

 docOriginal.compare(docEdited, "John Doe", new Date(), compareOptions);
 docOriginal.save(getArtifactsDir() + "Revision.CompareOptions.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setTarget(int value) {#setTarget-int}
```
public void setTarget(int value)
```


Gibt an, welches Dokument während des Vergleichs als Ziel verwendet werden soll.

 **Examples:** 

Zeigt, wie bestimmte Arten von Dokumentelementen beim Vergleich gefiltert werden können.

```

 // Create the original document and populate it with various kinds of elements.
 Document docOriginal = new Document();
 DocumentBuilder builder = new DocumentBuilder(docOriginal);

 // Paragraph text referenced with an endnote:
 builder.writeln("Hello world! This is the first paragraph.");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Original endnote text.");

 // Table:
 builder.startTable();
 builder.insertCell();
 builder.write("Original cell 1 text");
 builder.insertCell();
 builder.write("Original cell 2 text");
 builder.endTable();

 // Textbox:
 Shape textBox = builder.insertShape(ShapeType.TEXT_BOX, 150.0, 20.0);
 builder.moveTo(textBox.getFirstParagraph());
 builder.write("Original textbox contents");

 // DATE field:
 builder.moveTo(docOriginal.getFirstSection().getBody().appendParagraph(""));
 builder.insertField(" DATE ");

 // Comment:
 Comment newComment = new Comment(docOriginal, "John Doe", "J.D.", new Date());
 newComment.setText("Original comment.");
 builder.getCurrentParagraph().appendChild(newComment);

 // Header:
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.writeln("Original header contents.");

 // Create a clone of our document and perform a quick edit on each of the cloned document's elements.
 Document docEdited = (Document)docOriginal.deepClone(true);
 Paragraph firstParagraph = docEdited.getFirstSection().getBody().getFirstParagraph();

 firstParagraph.getRuns().get(0).setText("hello world! this is the first paragraph, after editing.");
 firstParagraph.getParagraphFormat().setStyle(docEdited.getStyles().getByStyleIdentifier(StyleIdentifier.HEADING_1));
 ((Footnote)docEdited.getChild(NodeType.FOOTNOTE, 0, true)).getFirstParagraph().getRuns().get(1).setText("Edited endnote text.");
 ((Table)docEdited.getChild(NodeType.TABLE, 0, true)).getFirstRow().getCells().get(1).getFirstParagraph().getRuns().get(0).setText("Edited Cell 2 contents");
 ((Shape)docEdited.getChild(NodeType.SHAPE, 0, true)).getFirstParagraph().getRuns().get(0).setText("Edited textbox contents");
 ((FieldDate)docEdited.getRange().getFields().get(0)).setUseLunarCalendar(true);
 ((Comment)docEdited.getChild(NodeType.COMMENT, 0, true)).getFirstParagraph().getRuns().get(0).setText("Edited comment.");
 docEdited.getFirstSection().getHeadersFooters().getByHeaderFooterType(HeaderFooterType.HEADER_PRIMARY).getFirstParagraph().getRuns().get(0).setText("Edited header contents.");

 // Comparing documents creates a revision for every edit in the edited document.
 // A CompareOptions object has a series of flags that can suppress revisions
 // on each respective type of element, effectively ignoring their change.
 CompareOptions compareOptions = new CompareOptions();
 compareOptions.setCompareMoves(false);
 compareOptions.setIgnoreFormatting(false);
 compareOptions.setIgnoreCaseChanges(false);
 compareOptions.setIgnoreComments(false);
 compareOptions.setIgnoreTables(false);
 compareOptions.setIgnoreFields(false);
 compareOptions.setIgnoreFootnotes(false);
 compareOptions.setIgnoreTextboxes(false);
 compareOptions.setIgnoreHeadersAndFooters(false);
 compareOptions.setTarget(ComparisonTargetType.NEW);

 docOriginal.compare(docEdited, "John Doe", new Date(), compareOptions);
 docOriginal.save(getArtifactsDir() + "Revision.CompareOptions.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Der entsprechende  int  Wert. Der Wert muss einer der [ComparisonTargetType](../../com.aspose.words/comparisontargettype/) Konstanten sein. |

