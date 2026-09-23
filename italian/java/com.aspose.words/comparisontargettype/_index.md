---
title: "ComparisonTargetType"
linktitle: "ComparisonTargetType"
second_title: "Aspose.Words per Java"
description: "Consente di specificare il documento di base che verrà utilizzato durante il confronto in Java."
type: docs
weight: 118
url: /it/java/com.aspose.words/comparisontargettype/
---

**Inheritance:**
java.lang.Object
```
public class ComparisonTargetType
```

Consente di specificare il documento di base che verrà utilizzato durante il confronto. Il valore predefinito è [CURRENT](../../com.aspose.words/comparisontargettype/\#CURRENT).

 **Remarks:** 

Riguarda l'opzione "Mostra modifiche in" di Microsoft Word nella finestra di dialogo "Confronta documenti".

 **Examples:** 

Mostra come filtrare tipi specifici di elementi del documento durante un confronto.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [CURRENT](#CURRENT) | Questo documento è usato come base durante il confronto. |
| [NEW](#NEW) | L'altro documento è usato come base durante il confronto. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String comparisonTargetTypeName)](#fromName-java.lang.String) |  |
| [getName(int comparisonTargetType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int comparisonTargetType)](#toString-int) |  |
### CURRENT {#CURRENT}
```
public static int CURRENT
```


Questo documento è usato come base durante il confronto.

### NEW {#NEW}
```
public static int NEW
```


L'altro documento è usato come base durante il confronto.

### length {#length}
```
public static int length
```


### fromName(String comparisonTargetTypeName) {#fromName-java.lang.String}
```
public static int fromName(String comparisonTargetTypeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| comparisonTargetTypeName | java.lang.String |  |

**Returns:**
int
### getName(int comparisonTargetType) {#getName-int}
```
public static String getName(int comparisonTargetType)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| comparisonTargetType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int comparisonTargetType) {#toString-int}
```
public static String toString(int comparisonTargetType)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| comparisonTargetType | int |  |

**Returns:**
java.lang.String
