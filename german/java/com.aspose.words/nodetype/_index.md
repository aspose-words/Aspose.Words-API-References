---
title: "NodeType"
linktitle: "NodeType"
second_title: "Aspose.Words für Java"
description: "Gibt den Typ eines Word-Dokuments-Knotens in Java an."
type: docs
weight: 483
url: /de/java/com.aspose.words/nodetype/
---

**Inheritance:**
java.lang.Object
```
public class NodeType
```

Gibt den Typ eines Word-Dokumentknotens an.

 **Examples:** 

Zeigt, wie man die Sammlung von Kindknoten eines zusammengesetzten Knotens durchläuft.

```

 Document doc = new Document();

 // Add two runs and one shape as child nodes to the first paragraph of this document.
 Paragraph paragraph = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);
 paragraph.appendChild(new Run(doc, "Hello world! "));

 Shape shape = new Shape(doc, ShapeType.RECTANGLE);
 shape.setWidth(200.0);
 shape.setHeight(200.0);
 // Note that the 'CustomNodeId' is not saved to an output file and exists only during the node lifetime.
 shape.setCustomNodeId(100);
 shape.setWrapType(WrapType.INLINE);
 paragraph.appendChild(shape);

 paragraph.appendChild(new Run(doc, "Hello again!"));

 // Iterate through the paragraph's collection of immediate children,
 // and print any runs or shapes that we find within.
 NodeCollection children = paragraph.getChildNodes(NodeType.ANY, false);

 Assert.assertEquals(3, paragraph.getChildNodes(NodeType.ANY, false).getCount());

 for (Node child : (Iterable) children)
     switch (child.getNodeType()) {
         case NodeType.RUN:
             System.out.println("Run contents:");
             System.out.println(MessageFormat.format("\t\"{0}\"", child.getText().trim()));
             break;
         case NodeType.SHAPE:
             Shape childShape = (Shape)child;
             System.out.println("Shape:");
             System.out.println(MessageFormat.format("\t{0}, {1}x{2}", childShape.getShapeType(), childShape.getWidth(), childShape.getHeight()));
             break;
     }
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [ANY](#ANY) | Zeigt alle Knotentypen an. |
| [BODY](#BODY) | Ein [Body](../../com.aspose.words/body/) Objekt, das den Haupttext eines Abschnitts (Haupttextgeschichte) enthält. |
| [BOOKMARK_END](#BOOKMARK-END) | Ein Endemarkierung eines Lesezeichens. |
| [BOOKMARK_START](#BOOKMARK-START) | Ein Beginn eines Lesezeichen-Markers. |
| [BUILDING_BLOCK](#BUILDING-BLOCK) | Ein Baustein innerhalb eines Glossar-Dokuments (z.B. |
| [CELL](#CELL) | Eine Zelle einer Tabellenzeile. |
| [COMMENT](#COMMENT) | Ein Kommentar in einem Word-Dokument. |
| [COMMENT_RANGE_END](#COMMENT-RANGE-END) | Ein Markerknoten, der das Ende eines kommentierten Bereichs darstellt. |
| [COMMENT_RANGE_START](#COMMENT-RANGE-START) | Ein Markerknoten, der den Beginn eines kommentierten Bereichs darstellt. |
| [DOCUMENT](#DOCUMENT) | Ein [Document](../../com.aspose.words/document/) Objekt, das als Wurzel des Dokumentbaums Zugriff auf das gesamte Word-Dokument bietet. |
| [EDITABLE_RANGE_END](#EDITABLE-RANGE-END) | Ein Ende eines bearbeitbaren Bereichs. |
| [EDITABLE_RANGE_START](#EDITABLE-RANGE-START) | Ein Beginn eines bearbeitbaren Bereichs. |
| [FIELD_END](#FIELD-END) | Ein Sonderzeichen, das das Ende eines Word-Feldes bezeichnet. |
| [FIELD_SEPARATOR](#FIELD-SEPARATOR) | Ein Sonderzeichen, das den Feldcode vom Feldergebnis trennt. |
| [FIELD_START](#FIELD-START) | Ein Sonderzeichen, das den Beginn eines Word-Feldes bezeichnet. |
| [FOOTNOTE](#FOOTNOTE) | Eine Fußnote oder Endnote in einem Word-Dokument. |
| [FORM_FIELD](#FORM-FIELD) | Ein Formularfeld. |
| [GLOSSARY_DOCUMENT](#GLOSSARY-DOCUMENT) | Ein Glossar-Dokument innerhalb des Hauptdokuments. |
| [GROUP_SHAPE](#GROUP-SHAPE) | Eine Gruppe von Formen, Bildern, OLE-Objekten oder anderen Gruppierungsformen. |
| [HEADER_FOOTER](#HEADER-FOOTER) | Ein [HeaderFooter](../../com.aspose.words/headerfooter/) Objekt, das den Text einer bestimmten Kopf- oder Fußzeile innerhalb eines Abschnitts enthält. |
| [MOVE_FROM_RANGE_END](#MOVE-FROM-RANGE-END) | Ein Ende eines MoveFrom-Bereichs. |
| [MOVE_FROM_RANGE_START](#MOVE-FROM-RANGE-START) | Ein Beginn eines MoveFrom-Bereichs. |
| [MOVE_TO_RANGE_END](#MOVE-TO-RANGE-END) | Ein Ende eines MoveTo-Bereichs. |
| [MOVE_TO_RANGE_START](#MOVE-TO-RANGE-START) | Ein Beginn eines MoveTo-Bereichs. |
| [NULL](#NULL) | Für die interne Verwendung durch Aspose.Words reserviert. |
| [OFFICE_MATH](#OFFICE-MATH) | Ein Office Math-Objekt. |
| [PARAGRAPH](#PARAGRAPH) | Ein Textabsatz. |
| [ROW](#ROW) | Eine Zeile einer Tabelle. |
| [RUN](#RUN) | Ein Textlauf. |
| [SECTION](#SECTION) | Ein [Section](../../com.aspose.words/section/) Objekt, das einem Abschnitt in einem Word-Dokument entspricht. |
| [SHAPE](#SHAPE) | Ein Zeichenobjekt, wie z. B. eine OfficeArt‑Form, ein Bild oder ein OLE‑Objekt. |
| [SMART_TAG](#SMART-TAG) | Ein Smart‑Tag um eine oder mehrere Inline‑Strukturen (Läufe, Bilder, Felder usw.) innerhalb eines Absatzes. |
| [SPECIAL_CHAR](#SPECIAL-CHAR) | Ein Sonderzeichen, das nicht zu den spezifischeren Sonderzeichenarten gehört. |
| [STRUCTURED_DOCUMENT_TAG](#STRUCTURED-DOCUMENT-TAG) | Ermöglicht die Definition kundenspezifischer Informationen und deren Darstellung. |
| [STRUCTURED_DOCUMENT_TAG_RANGE_END](#STRUCTURED-DOCUMENT-TAG-RANGE-END) | Ein End‑Tag des **ranged** strukturierten Dokument‑Tags, das Inhalte mit mehreren Abschnitten akzeptiert. |
| [STRUCTURED_DOCUMENT_TAG_RANGE_START](#STRUCTURED-DOCUMENT-TAG-RANGE-START) | Ein Start‑Tag des **ranged** strukturierten Dokument‑Tags, das Inhalte mit mehreren Abschnitten akzeptiert. |
| [SUB_DOCUMENT](#SUB-DOCUMENT) | Ein Subdokument‑Knoten, der ein Link zu einem anderen Dokument ist. |
| [SYSTEM](#SYSTEM) | Für die interne Verwendung durch Aspose.Words reserviert. |
| [TABLE](#TABLE) | Ein [Table](../../com.aspose.words/table/) Objekt, das eine Tabelle in einem Word-Dokument darstellt. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String nodeTypeName)](#fromName-java.lang.String) |  |
| [getName(int nodeType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int nodeType)](#toString-int) |  |
### ANY {#ANY}
```
public static int ANY
```


Zeigt alle Knotentypen an. Ermöglicht die Auswahl aller Kindknoten.

### BODY {#BODY}
```
public static int BODY
```


Ein [Body](../../com.aspose.words/body/) Objekt, das den Haupttext eines Abschnitts (Haupttextgeschichte) enthält.

Ein [Body](../../com.aspose.words/body/) Knoten kann [Paragraph](../../com.aspose.words/paragraph/) und [Table](../../com.aspose.words/table/) Knoten enthalten.

### BOOKMARK_END {#BOOKMARK-END}
```
public static int BOOKMARK_END
```


Ein Endemarkierung eines Lesezeichens.

### BOOKMARK_START {#BOOKMARK-START}
```
public static int BOOKMARK_START
```


Ein Beginn eines Lesezeichen-Markers.

### BUILDING_BLOCK {#BUILDING-BLOCK}
```
public static int BUILDING_BLOCK
```


Ein Baustein innerhalb eines Glossar‑Dokuments (z. B. Glossar‑Eintrag).

### CELL {#CELL}
```
public static int CELL
```


Eine Zelle einer Tabellenzeile.

Ein [Cell](../../com.aspose.words/cell/) Knoten kann [Paragraph](../../com.aspose.words/paragraph/) und [Table](../../com.aspose.words/table/) Knoten enthalten.

### COMMENT {#COMMENT}
```
public static int COMMENT
```


Ein Kommentar in einem Word-Dokument.

Ein [Comment](../../com.aspose.words/comment/) Knoten kann [Paragraph](../../com.aspose.words/paragraph/) und [Table](../../com.aspose.words/table/) Knoten enthalten.

### COMMENT_RANGE_END {#COMMENT-RANGE-END}
```
public static int COMMENT_RANGE_END
```


Ein Markerknoten, der das Ende eines kommentierten Bereichs darstellt.

### COMMENT_RANGE_START {#COMMENT-RANGE-START}
```
public static int COMMENT_RANGE_START
```


Ein Markerknoten, der den Beginn eines kommentierten Bereichs darstellt.

### DOCUMENT {#DOCUMENT}
```
public static int DOCUMENT
```


Ein [Document](../../com.aspose.words/document/) Objekt, das als Wurzel des Dokumentbaums Zugriff auf das gesamte Word-Dokument bietet.

Ein [Document](../../com.aspose.words/document/) Knoten kann [Section](../../com.aspose.words/section/) Knoten enthalten.

### EDITABLE_RANGE_END {#EDITABLE-RANGE-END}
```
public static int EDITABLE_RANGE_END
```


Ein Ende eines bearbeitbaren Bereichs.

### EDITABLE_RANGE_START {#EDITABLE-RANGE-START}
```
public static int EDITABLE_RANGE_START
```


Ein Beginn eines bearbeitbaren Bereichs.

### FIELD_END {#FIELD-END}
```
public static int FIELD_END
```


Ein Sonderzeichen, das das Ende eines Word-Feldes bezeichnet.

### FIELD_SEPARATOR {#FIELD-SEPARATOR}
```
public static int FIELD_SEPARATOR
```


Ein Sonderzeichen, das den Feldcode vom Feldergebnis trennt.

### FIELD_START {#FIELD-START}
```
public static int FIELD_START
```


Ein Sonderzeichen, das den Beginn eines Word-Feldes bezeichnet.

### FOOTNOTE {#FOOTNOTE}
```
public static int FOOTNOTE
```


Eine Fußnote oder Endnote in einem Word-Dokument.

Ein [Footnote](../../com.aspose.words/footnote/) Knoten kann [Paragraph](../../com.aspose.words/paragraph/) und [Table](../../com.aspose.words/table/) Knoten enthalten.

### FORM_FIELD {#FORM-FIELD}
```
public static int FORM_FIELD
```


Ein Formularfeld.

### GLOSSARY_DOCUMENT {#GLOSSARY-DOCUMENT}
```
public static int GLOSSARY_DOCUMENT
```


Ein Glossar-Dokument innerhalb des Hauptdokuments.

### GROUP_SHAPE {#GROUP-SHAPE}
```
public static int GROUP_SHAPE
```


Eine Gruppe von Formen, Bildern, OLE-Objekten oder anderen Gruppierungsformen.

Ein [GroupShape](../../com.aspose.words/groupshape/) Knoten kann andere [Shape](../../com.aspose.words/shape/) und [GroupShape](../../com.aspose.words/groupshape/) Knoten enthalten.

### HEADER_FOOTER {#HEADER-FOOTER}
```
public static int HEADER_FOOTER
```


Ein [HeaderFooter](../../com.aspose.words/headerfooter/) Objekt, das den Text einer bestimmten Kopf- oder Fußzeile innerhalb eines Abschnitts enthält.

Ein [HeaderFooter](../../com.aspose.words/headerfooter/) Knoten kann [Paragraph](../../com.aspose.words/paragraph/) und [Table](../../com.aspose.words/table/) Knoten enthalten.

### MOVE_FROM_RANGE_END {#MOVE-FROM-RANGE-END}
```
public static int MOVE_FROM_RANGE_END
```


Ein Ende eines MoveFrom-Bereichs.

### MOVE_FROM_RANGE_START {#MOVE-FROM-RANGE-START}
```
public static int MOVE_FROM_RANGE_START
```


Ein Beginn eines MoveFrom-Bereichs.

### MOVE_TO_RANGE_END {#MOVE-TO-RANGE-END}
```
public static int MOVE_TO_RANGE_END
```


Ein Ende eines MoveTo-Bereichs.

### MOVE_TO_RANGE_START {#MOVE-TO-RANGE-START}
```
public static int MOVE_TO_RANGE_START
```


Ein Beginn eines MoveTo-Bereichs.

### NULL {#NULL}
```
public static int NULL
```


Für die interne Verwendung durch Aspose.Words reserviert.

### OFFICE_MATH {#OFFICE-MATH}
```
public static int OFFICE_MATH
```


Ein Office‑Math‑Objekt. Kann eine Gleichung, Funktion, Matrix oder eines der anderen mathematischen Objekte sein. Kann eine Sammlung mathematischer Objekte sein und auch nicht‑mathematische Objekte wie Textläufe enthalten.

### PARAGRAPH {#PARAGRAPH}
```
public static int PARAGRAPH
```


Ein Textabsatz.

Ein [Paragraph](../../com.aspose.words/paragraph/) Knoten ist ein Container für Inline‑Elemente [Run](../../com.aspose.words/run/), [FieldStart](../../com.aspose.words/fieldstart/), [FieldSeparator](../../com.aspose.words/fieldseparator/), [FieldEnd](../../com.aspose.words/fieldend/), [FormField](../../com.aspose.words/formfield/), [Shape](../../com.aspose.words/shape/), [GroupShape](../../com.aspose.words/groupshape/), [Footnote](../../com.aspose.words/footnote/), [Comment](../../com.aspose.words/comment/), [SpecialChar](../../com.aspose.words/specialchar/), sowie [BookmarkStart](../../com.aspose.words/bookmarkstart/) und [BookmarkEnd](../../com.aspose.words/bookmarkend/).

### ROW {#ROW}
```
public static int ROW
```


Eine Zeile einer Tabelle.

Ein [Row](../../com.aspose.words/row/) Knoten kann [Cell](../../com.aspose.words/cell/) Knoten enthalten.

### RUN {#RUN}
```
public static int RUN
```


Ein Textlauf.

### SECTION {#SECTION}
```
public static int SECTION
```


Ein [Section](../../com.aspose.words/section/) Objekt, das einem Abschnitt in einem Word-Dokument entspricht.

Ein [Section](../../com.aspose.words/section/) Knoten kann [Body](../../com.aspose.words/body/) und [HeaderFooter](../../com.aspose.words/headerfooter/) Knoten haben.

### SHAPE {#SHAPE}
```
public static int SHAPE
```


Ein Zeichenobjekt, wie z. B. eine OfficeArt‑Form, ein Bild oder ein OLE‑Objekt.

Ein [Shape](../../com.aspose.words/shape/) Knoten kann [Paragraph](../../com.aspose.words/paragraph/) und [Table](../../com.aspose.words/table/) Knoten enthalten.

### SMART_TAG {#SMART-TAG}
```
public static int SMART_TAG
```


Ein Smart‑Tag um eine oder mehrere Inline‑Strukturen (Läufe, Bilder, Felder usw.) innerhalb eines Absatzes.

### SPECIAL_CHAR {#SPECIAL-CHAR}
```
public static int SPECIAL_CHAR
```


Ein Sonderzeichen, das nicht zu den spezifischeren Sonderzeichenarten gehört.

### STRUCTURED_DOCUMENT_TAG {#STRUCTURED-DOCUMENT-TAG}
```
public static int STRUCTURED_DOCUMENT_TAG
```


Ermöglicht die Definition kundenspezifischer Informationen und deren Darstellung.

### STRUCTURED_DOCUMENT_TAG_RANGE_END {#STRUCTURED-DOCUMENT-TAG-RANGE-END}
```
public static int STRUCTURED_DOCUMENT_TAG_RANGE_END
```


Ein End‑Tag des **ranged** strukturierten Dokument‑Tags, das Inhalte mit mehreren Abschnitten akzeptiert.

### STRUCTURED_DOCUMENT_TAG_RANGE_START {#STRUCTURED-DOCUMENT-TAG-RANGE-START}
```
public static int STRUCTURED_DOCUMENT_TAG_RANGE_START
```


Ein Start‑Tag des **ranged** strukturierten Dokument‑Tags, das Inhalte mit mehreren Abschnitten akzeptiert.

### SUB_DOCUMENT {#SUB-DOCUMENT}
```
public static int SUB_DOCUMENT
```


Ein Subdokument‑Knoten, der ein Link zu einem anderen Dokument ist.

### SYSTEM {#SYSTEM}
```
public static int SYSTEM
```


Für die interne Verwendung durch Aspose.Words reserviert.

### TABLE {#TABLE}
```
public static int TABLE
```


Ein [Table](../../com.aspose.words/table/) Objekt, das eine Tabelle in einem Word-Dokument darstellt.

Ein [Table](../../com.aspose.words/table/) Knoten kann [Row](../../com.aspose.words/row/) Knoten haben.

### length {#length}
```
public static int length
```


### fromName(String nodeTypeName) {#fromName-java.lang.String}
```
public static int fromName(String nodeTypeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| nodeTypeName | java.lang.String |  |

**Returns:**
int
### getName(int nodeType) {#getName-int}
```
public static String getName(int nodeType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| nodeType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int nodeType) {#toString-int}
```
public static String toString(int nodeType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| nodeType | int |  |

**Returns:**
java.lang.String
