---
title: "NodeType"
linktitle: "NodeType"
second_title: "Aspose.Words per Java"
description: "Specifica il tipo di nodo di un documento Word in Java."
type: docs
weight: 483
url: /it/java/com.aspose.words/nodetype/
---

**Inheritance:**
java.lang.Object
```
public class NodeType
```

Specifica il tipo di nodo di un documento Word.

 **Examples:** 

Mostra come attraversare la collezione di nodi figli di un nodo composito.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [ANY](#ANY) | Indica tutti i tipi di nodo. |
| [BODY](#BODY) | Un oggetto [Body](../../com.aspose.words/body/) che contiene il testo principale di una sezione (storia di testo principale). |
| [BOOKMARK_END](#BOOKMARK-END) | Una fine di un marcatore di segnalibro. |
| [BOOKMARK_START](#BOOKMARK-START) | Un inizio di un marcatore di segnalibro. |
| [BUILDING_BLOCK](#BUILDING-BLOCK) | Un blocco di costruzione all'interno di un documento glossario (ad es. |
| [CELL](#CELL) | Una cella di una riga di tabella. |
| [COMMENT](#COMMENT) | Un commento in un documento Word. |
| [COMMENT_RANGE_END](#COMMENT-RANGE-END) | Un nodo marcatore che rappresenta la fine di un intervallo commentato. |
| [COMMENT_RANGE_START](#COMMENT-RANGE-START) | Un nodo marcatore che rappresenta l'inizio di un intervallo commentato. |
| [DOCUMENT](#DOCUMENT) | Un oggetto [Document](../../com.aspose.words/document/) che, come radice dell'albero del documento, fornisce l'accesso all'intero documento Word. |
| [EDITABLE_RANGE_END](#EDITABLE-RANGE-END) | Una fine di un intervallo modificabile. |
| [EDITABLE_RANGE_START](#EDITABLE-RANGE-START) | Un inizio di un intervallo modificabile. |
| [FIELD_END](#FIELD-END) | Un carattere speciale che designa la fine di un campo Word. |
| [FIELD_SEPARATOR](#FIELD-SEPARATOR) | Un carattere speciale che separa il codice del campo dal risultato del campo. |
| [FIELD_START](#FIELD-START) | Un carattere speciale che designa l'inizio di un campo Word. |
| [FOOTNOTE](#FOOTNOTE) | Una nota a piè di pagina o una nota di chiusura in un documento Word. |
| [FORM_FIELD](#FORM-FIELD) | Un campo modulo. |
| [GLOSSARY_DOCUMENT](#GLOSSARY-DOCUMENT) | Un documento di glossario all'interno del documento principale. |
| [GROUP_SHAPE](#GROUP-SHAPE) | Un gruppo di forme, immagini, oggetti OLE o altre forme di gruppo. |
| [HEADER_FOOTER](#HEADER-FOOTER) | Un oggetto [HeaderFooter](../../com.aspose.words/headerfooter/) che contiene il testo di un'intestazione o di un piè di pagina particolare all'interno di una sezione. |
| [MOVE_FROM_RANGE_END](#MOVE-FROM-RANGE-END) | Una fine di un intervallo MoveFrom. |
| [MOVE_FROM_RANGE_START](#MOVE-FROM-RANGE-START) | Un inizio di un intervallo MoveFrom. |
| [MOVE_TO_RANGE_END](#MOVE-TO-RANGE-END) | Una fine di un intervallo MoveTo. |
| [MOVE_TO_RANGE_START](#MOVE-TO-RANGE-START) | Un inizio di un intervallo MoveTo. |
| [NULL](#NULL) | Riservato per uso interno da Aspose.Words. |
| [OFFICE_MATH](#OFFICE-MATH) | Un oggetto Office Math. |
| [PARAGRAPH](#PARAGRAPH) | Un paragrafo di testo. |
| [ROW](#ROW) | Una riga di una tabella. |
| [RUN](#RUN) | Una sequenza di testo. |
| [SECTION](#SECTION) | Un oggetto [Section](../../com.aspose.words/section/) che corrisponde a una sezione in un documento Word. |
| [SHAPE](#SHAPE) | Un oggetto di disegno, come una forma OfficeArt, un'immagine o un oggetto OLE. |
| [SMART_TAG](#SMART-TAG) | Un tag intelligente attorno a una o più strutture in linea (run, immagini, campi, ecc.) all'interno di un paragrafo. |
| [SPECIAL_CHAR](#SPECIAL-CHAR) | Un carattere speciale che non è uno dei tipi di carattere speciale più specifici. |
| [STRUCTURED_DOCUMENT_TAG](#STRUCTURED-DOCUMENT-TAG) | Consente di definire informazioni specifiche per il cliente e i relativi mezzi di presentazione. |
| [STRUCTURED_DOCUMENT_TAG_RANGE_END](#STRUCTURED-DOCUMENT-TAG-RANGE-END) | Una fine del tag di documento strutturato **ranged** che accetta contenuto a più sezioni. |
| [STRUCTURED_DOCUMENT_TAG_RANGE_START](#STRUCTURED-DOCUMENT-TAG-RANGE-START) | Un inizio del tag di documento strutturato **ranged** che accetta contenuto a più sezioni. |
| [SUB_DOCUMENT](#SUB-DOCUMENT) | Un nodo subdocumento che è un collegamento a un altro documento. |
| [SYSTEM](#SYSTEM) | Riservato per uso interno da Aspose.Words. |
| [TABLE](#TABLE) | Un oggetto [Table](../../com.aspose.words/table/) che rappresenta una tabella in un documento Word. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String nodeTypeName)](#fromName-java.lang.String) |  |
| [getName(int nodeType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int nodeType)](#toString-int) |  |
### ANY {#ANY}
```
public static int ANY
```


Indica tutti i tipi di nodo. Consente di selezionare tutti i figli.

### BODY {#BODY}
```
public static int BODY
```


Un oggetto [Body](../../com.aspose.words/body/) che contiene il testo principale di una sezione (storia di testo principale).

Un nodo [Body](../../com.aspose.words/body/) può contenere nodi [Paragraph](../../com.aspose.words/paragraph/) e [Table](../../com.aspose.words/table/).

### BOOKMARK_END {#BOOKMARK-END}
```
public static int BOOKMARK_END
```


Una fine di un marcatore di segnalibro.

### BOOKMARK_START {#BOOKMARK-START}
```
public static int BOOKMARK_START
```


Un inizio di un marcatore di segnalibro.

### BUILDING_BLOCK {#BUILDING-BLOCK}
```
public static int BUILDING_BLOCK
```


Un blocco di costruzione all'interno di un documento glossario (ad es. voce del documento glossario).

### CELL {#CELL}
```
public static int CELL
```


Una cella di una riga di tabella.

Un nodo [Cell](../../com.aspose.words/cell/) può contenere nodi [Paragraph](../../com.aspose.words/paragraph/) e [Table](../../com.aspose.words/table/).

### COMMENT {#COMMENT}
```
public static int COMMENT
```


Un commento in un documento Word.

Un nodo [Comment](../../com.aspose.words/comment/) può contenere nodi [Paragraph](../../com.aspose.words/paragraph/) e [Table](../../com.aspose.words/table/).

### COMMENT_RANGE_END {#COMMENT-RANGE-END}
```
public static int COMMENT_RANGE_END
```


Un nodo marcatore che rappresenta la fine di un intervallo commentato.

### COMMENT_RANGE_START {#COMMENT-RANGE-START}
```
public static int COMMENT_RANGE_START
```


Un nodo marcatore che rappresenta l'inizio di un intervallo commentato.

### DOCUMENT {#DOCUMENT}
```
public static int DOCUMENT
```


Un oggetto [Document](../../com.aspose.words/document/) che, come radice dell'albero del documento, fornisce l'accesso all'intero documento Word.

Un nodo [Document](../../com.aspose.words/document/) può contenere nodi [Section](../../com.aspose.words/section/).

### EDITABLE_RANGE_END {#EDITABLE-RANGE-END}
```
public static int EDITABLE_RANGE_END
```


Una fine di un intervallo modificabile.

### EDITABLE_RANGE_START {#EDITABLE-RANGE-START}
```
public static int EDITABLE_RANGE_START
```


Un inizio di un intervallo modificabile.

### FIELD_END {#FIELD-END}
```
public static int FIELD_END
```


Un carattere speciale che designa la fine di un campo Word.

### FIELD_SEPARATOR {#FIELD-SEPARATOR}
```
public static int FIELD_SEPARATOR
```


Un carattere speciale che separa il codice del campo dal risultato del campo.

### FIELD_START {#FIELD-START}
```
public static int FIELD_START
```


Un carattere speciale che designa l'inizio di un campo Word.

### FOOTNOTE {#FOOTNOTE}
```
public static int FOOTNOTE
```


Una nota a piè di pagina o una nota di chiusura in un documento Word.

Un nodo [Footnote](../../com.aspose.words/footnote/) può contenere nodi [Paragraph](../../com.aspose.words/paragraph/) e [Table](../../com.aspose.words/table/).

### FORM_FIELD {#FORM-FIELD}
```
public static int FORM_FIELD
```


Un campo modulo.

### GLOSSARY_DOCUMENT {#GLOSSARY-DOCUMENT}
```
public static int GLOSSARY_DOCUMENT
```


Un documento di glossario all'interno del documento principale.

### GROUP_SHAPE {#GROUP-SHAPE}
```
public static int GROUP_SHAPE
```


Un gruppo di forme, immagini, oggetti OLE o altre forme di gruppo.

Un nodo [GroupShape](../../com.aspose.words/groupshape/) può contenere altri nodi [Shape](../../com.aspose.words/shape/) e [GroupShape](../../com.aspose.words/groupshape/).

### HEADER_FOOTER {#HEADER-FOOTER}
```
public static int HEADER_FOOTER
```


Un oggetto [HeaderFooter](../../com.aspose.words/headerfooter/) che contiene il testo di un'intestazione o di un piè di pagina particolare all'interno di una sezione.

Un nodo [HeaderFooter](../../com.aspose.words/headerfooter/) può contenere nodi [Paragraph](../../com.aspose.words/paragraph/) e [Table](../../com.aspose.words/table/).

### MOVE_FROM_RANGE_END {#MOVE-FROM-RANGE-END}
```
public static int MOVE_FROM_RANGE_END
```


Una fine di un intervallo MoveFrom.

### MOVE_FROM_RANGE_START {#MOVE-FROM-RANGE-START}
```
public static int MOVE_FROM_RANGE_START
```


Un inizio di un intervallo MoveFrom.

### MOVE_TO_RANGE_END {#MOVE-TO-RANGE-END}
```
public static int MOVE_TO_RANGE_END
```


Una fine di un intervallo MoveTo.

### MOVE_TO_RANGE_START {#MOVE-TO-RANGE-START}
```
public static int MOVE_TO_RANGE_START
```


Un inizio di un intervallo MoveTo.

### NULL {#NULL}
```
public static int NULL
```


Riservato per uso interno da Aspose.Words.

### OFFICE_MATH {#OFFICE-MATH}
```
public static int OFFICE_MATH
```


Un oggetto Office Math. Può essere un'equazione, una funzione, una matrice o uno degli altri oggetti matematici. Può essere una collezione di oggetti matematici e può anche contenere alcuni oggetti non matematici, come sequenze di testo.

### PARAGRAPH {#PARAGRAPH}
```
public static int PARAGRAPH
```


Un paragrafo di testo.

Un nodo [Paragraph](../../com.aspose.words/paragraph/) è un contenitore per elementi di livello inline [Run](../../com.aspose.words/run/), [FieldStart](../../com.aspose.words/fieldstart/), [FieldSeparator](../../com.aspose.words/fieldseparator/), [FieldEnd](../../com.aspose.words/fieldend/), [FormField](../../com.aspose.words/formfield/), [Shape](../../com.aspose.words/shape/), [GroupShape](../../com.aspose.words/groupshape/), [Footnote](../../com.aspose.words/footnote/), [Comment](../../com.aspose.words/comment/), [SpecialChar](../../com.aspose.words/specialchar/), così come [BookmarkStart](../../com.aspose.words/bookmarkstart/) e [BookmarkEnd](../../com.aspose.words/bookmarkend/).

### ROW {#ROW}
```
public static int ROW
```


Una riga di una tabella.

Un nodo [Row](../../com.aspose.words/row/) può contenere nodi [Cell](../../com.aspose.words/cell/).

### RUN {#RUN}
```
public static int RUN
```


Una sequenza di testo.

### SECTION {#SECTION}
```
public static int SECTION
```


Un oggetto [Section](../../com.aspose.words/section/) che corrisponde a una sezione in un documento Word.

Un nodo [Section](../../com.aspose.words/section/) può contenere nodi [Body](../../com.aspose.words/body/) e [HeaderFooter](../../com.aspose.words/headerfooter/).

### SHAPE {#SHAPE}
```
public static int SHAPE
```


Un oggetto di disegno, come una forma OfficeArt, un'immagine o un oggetto OLE.

Un nodo [Shape](../../com.aspose.words/shape/) può contenere nodi [Paragraph](../../com.aspose.words/paragraph/) e [Table](../../com.aspose.words/table/).

### SMART_TAG {#SMART-TAG}
```
public static int SMART_TAG
```


Un tag intelligente attorno a una o più strutture in linea (run, immagini, campi, ecc.) all'interno di un paragrafo.

### SPECIAL_CHAR {#SPECIAL-CHAR}
```
public static int SPECIAL_CHAR
```


Un carattere speciale che non è uno dei tipi di carattere speciale più specifici.

### STRUCTURED_DOCUMENT_TAG {#STRUCTURED-DOCUMENT-TAG}
```
public static int STRUCTURED_DOCUMENT_TAG
```


Consente di definire informazioni specifiche per il cliente e i relativi mezzi di presentazione.

### STRUCTURED_DOCUMENT_TAG_RANGE_END {#STRUCTURED-DOCUMENT-TAG-RANGE-END}
```
public static int STRUCTURED_DOCUMENT_TAG_RANGE_END
```


Una fine del tag di documento strutturato **ranged** che accetta contenuto a più sezioni.

### STRUCTURED_DOCUMENT_TAG_RANGE_START {#STRUCTURED-DOCUMENT-TAG-RANGE-START}
```
public static int STRUCTURED_DOCUMENT_TAG_RANGE_START
```


Un inizio del tag di documento strutturato **ranged** che accetta contenuto a più sezioni.

### SUB_DOCUMENT {#SUB-DOCUMENT}
```
public static int SUB_DOCUMENT
```


Un nodo subdocumento che è un collegamento a un altro documento.

### SYSTEM {#SYSTEM}
```
public static int SYSTEM
```


Riservato per uso interno da Aspose.Words.

### TABLE {#TABLE}
```
public static int TABLE
```


Un oggetto [Table](../../com.aspose.words/table/) che rappresenta una tabella in un documento Word.

Un nodo [Table](../../com.aspose.words/table/) può contenere nodi [Row](../../com.aspose.words/row/).

### length {#length}
```
public static int length
```


### fromName(String nodeTypeName) {#fromName-java.lang.String}
```
public static int fromName(String nodeTypeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| nodeTypeName | java.lang.String |  |

**Returns:**
int
### getName(int nodeType) {#getName-int}
```
public static String getName(int nodeType)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| nodeType | int |  |

**Returns:**
java.lang.String
