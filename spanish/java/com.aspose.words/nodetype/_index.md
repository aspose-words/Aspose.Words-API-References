---
title: "NodeType"
linktitle: "NodeType"
second_title: "Aspose.Words para Java"
description: "Especifica el tipo de nodo de un documento Word en Java."
type: docs
weight: 483
url: /es/java/com.aspose.words/nodetype/
---

**Inheritance:**
java.lang.Object
```
public class NodeType
```

Especifica el tipo de un nodo de documento Word.

 **Examples:** 

Muestra cómo recorrer la colección de nodos hijos de un nodo compuesto.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [ANY](#ANY) | Indica todos los tipos de nodos. |
| [BODY](#BODY) | Un objeto [Body](../../com.aspose.words/body/) que contiene el texto principal de una sección (historia de texto principal). |
| [BOOKMARK_END](#BOOKMARK-END) | Un final de un marcador. |
| [BOOKMARK_START](#BOOKMARK-START) | Un comienzo de un marcador. |
| [BUILDING_BLOCK](#BUILDING-BLOCK) | Un bloque de construcción dentro de un documento de glosario (p.ej. |
| [CELL](#CELL) | Una celda de una fila de tabla. |
| [COMMENT](#COMMENT) | Un comentario en un documento Word. |
| [COMMENT_RANGE_END](#COMMENT-RANGE-END) | Un nodo marcador que representa el final de un rango comentado. |
| [COMMENT_RANGE_START](#COMMENT-RANGE-START) | Un nodo marcador que representa el inicio de un rango comentado. |
| [DOCUMENT](#DOCUMENT) | Un objeto [Document](../../com.aspose.words/document/) que, como la raíz del árbol del documento, brinda acceso a todo el documento Word. |
| [EDITABLE_RANGE_END](#EDITABLE-RANGE-END) | Un final de un rango editable. |
| [EDITABLE_RANGE_START](#EDITABLE-RANGE-START) | Un comienzo de un rango editable. |
| [FIELD_END](#FIELD-END) | Un carácter especial que designa el final de un campo de Word. |
| [FIELD_SEPARATOR](#FIELD-SEPARATOR) | Un carácter especial que separa el código del campo del resultado del campo. |
| [FIELD_START](#FIELD-START) | Un carácter especial que designa el inicio de un campo de Word. |
| [FOOTNOTE](#FOOTNOTE) | Una nota al pie o nota final en un documento de Word. |
| [FORM_FIELD](#FORM-FIELD) | Un campo de formulario. |
| [GLOSSARY_DOCUMENT](#GLOSSARY-DOCUMENT) | Un documento de glosario dentro del documento principal. |
| [GROUP_SHAPE](#GROUP-SHAPE) | Un grupo de formas, imágenes, objetos OLE u otras formas agrupadas. |
| [HEADER_FOOTER](#HEADER-FOOTER) | Un objeto [HeaderFooter](../../com.aspose.words/headerfooter/) que contiene el texto de un encabezado o pie de página particular dentro de una sección. |
| [MOVE_FROM_RANGE_END](#MOVE-FROM-RANGE-END) | Un final de un rango MoveFrom. |
| [MOVE_FROM_RANGE_START](#MOVE-FROM-RANGE-START) | Un comienzo de un rango MoveFrom. |
| [MOVE_TO_RANGE_END](#MOVE-TO-RANGE-END) | Un final de un rango MoveTo. |
| [MOVE_TO_RANGE_START](#MOVE-TO-RANGE-START) | Un comienzo de un rango MoveTo. |
| [NULL](#NULL) | Reservado para uso interno por Aspose.Words. |
| [OFFICE_MATH](#OFFICE-MATH) | Un objeto Office Math. |
| [PARAGRAPH](#PARAGRAPH) | Un párrafo de texto. |
| [ROW](#ROW) | Una fila de una tabla. |
| [RUN](#RUN) | Un segmento de texto. |
| [SECTION](#SECTION) | Un objeto [Section](../../com.aspose.words/section/) que corresponde a una sección en un documento de Word. |
| [SHAPE](#SHAPE) | Un objeto de dibujo, como una forma OfficeArt, una imagen o un objeto OLE. |
| [SMART_TAG](#SMART-TAG) | Una etiqueta inteligente alrededor de una o más estructuras en línea (segmentos, imágenes, campos, etc.) dentro de un párrafo. |
| [SPECIAL_CHAR](#SPECIAL-CHAR) | Un carácter especial que no es uno de los tipos de caracteres especiales más específicos. |
| [STRUCTURED_DOCUMENT_TAG](#STRUCTURED-DOCUMENT-TAG) | Permite definir información específica del cliente y sus medios de presentación. |
| [STRUCTURED_DOCUMENT_TAG_RANGE_END](#STRUCTURED-DOCUMENT-TAG-RANGE-END) | Un final de la etiqueta estructurada de documento **ranged** que acepta contenido de múltiples secciones. |
| [STRUCTURED_DOCUMENT_TAG_RANGE_START](#STRUCTURED-DOCUMENT-TAG-RANGE-START) | Un inicio de la etiqueta estructurada de documento **ranged** que acepta contenido de múltiples secciones. |
| [SUB_DOCUMENT](#SUB-DOCUMENT) | Un nodo de subdocumento que es un enlace a otro documento. |
| [SYSTEM](#SYSTEM) | Reservado para uso interno por Aspose.Words. |
| [TABLE](#TABLE) | Un objeto [Table](../../com.aspose.words/table/) que representa una tabla en un documento de Word. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String nodeTypeName)](#fromName-java.lang.String) |  |
| [getName(int nodeType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int nodeType)](#toString-int) |  |
### ANY {#ANY}
```
public static int ANY
```


Indica todos los tipos de nodo. Permite seleccionar todos los hijos.

### BODY {#BODY}
```
public static int BODY
```


Un objeto [Body](../../com.aspose.words/body/) que contiene el texto principal de una sección (historia de texto principal).

Un nodo [Body](../../com.aspose.words/body/) puede contener nodos [Paragraph](../../com.aspose.words/paragraph/) y [Table](../../com.aspose.words/table/).

### BOOKMARK_END {#BOOKMARK-END}
```
public static int BOOKMARK_END
```


Un final de un marcador.

### BOOKMARK_START {#BOOKMARK-START}
```
public static int BOOKMARK_START
```


Un comienzo de un marcador.

### BUILDING_BLOCK {#BUILDING-BLOCK}
```
public static int BUILDING_BLOCK
```


Un bloque de construcción dentro de un documento de glosario (p.ej., entrada de documento de glosario).

### CELL {#CELL}
```
public static int CELL
```


Una celda de una fila de tabla.

Un nodo [Cell](../../com.aspose.words/cell/) puede contener nodos [Paragraph](../../com.aspose.words/paragraph/) y [Table](../../com.aspose.words/table/).

### COMMENT {#COMMENT}
```
public static int COMMENT
```


Un comentario en un documento Word.

Un nodo [Comment](../../com.aspose.words/comment/) puede contener nodos [Paragraph](../../com.aspose.words/paragraph/) y [Table](../../com.aspose.words/table/).

### COMMENT_RANGE_END {#COMMENT-RANGE-END}
```
public static int COMMENT_RANGE_END
```


Un nodo marcador que representa el final de un rango comentado.

### COMMENT_RANGE_START {#COMMENT-RANGE-START}
```
public static int COMMENT_RANGE_START
```


Un nodo marcador que representa el inicio de un rango comentado.

### DOCUMENT {#DOCUMENT}
```
public static int DOCUMENT
```


Un objeto [Document](../../com.aspose.words/document/) que, como la raíz del árbol del documento, brinda acceso a todo el documento Word.

Un nodo [Document](../../com.aspose.words/document/) puede contener nodos [Section](../../com.aspose.words/section/).

### EDITABLE_RANGE_END {#EDITABLE-RANGE-END}
```
public static int EDITABLE_RANGE_END
```


Un final de un rango editable.

### EDITABLE_RANGE_START {#EDITABLE-RANGE-START}
```
public static int EDITABLE_RANGE_START
```


Un comienzo de un rango editable.

### FIELD_END {#FIELD-END}
```
public static int FIELD_END
```


Un carácter especial que designa el final de un campo de Word.

### FIELD_SEPARATOR {#FIELD-SEPARATOR}
```
public static int FIELD_SEPARATOR
```


Un carácter especial que separa el código del campo del resultado del campo.

### FIELD_START {#FIELD-START}
```
public static int FIELD_START
```


Un carácter especial que designa el inicio de un campo de Word.

### FOOTNOTE {#FOOTNOTE}
```
public static int FOOTNOTE
```


Una nota al pie o nota final en un documento de Word.

Un nodo [Footnote](../../com.aspose.words/footnote/) puede contener nodos [Paragraph](../../com.aspose.words/paragraph/) y [Table](../../com.aspose.words/table/).

### FORM_FIELD {#FORM-FIELD}
```
public static int FORM_FIELD
```


Un campo de formulario.

### GLOSSARY_DOCUMENT {#GLOSSARY-DOCUMENT}
```
public static int GLOSSARY_DOCUMENT
```


Un documento de glosario dentro del documento principal.

### GROUP_SHAPE {#GROUP-SHAPE}
```
public static int GROUP_SHAPE
```


Un grupo de formas, imágenes, objetos OLE u otras formas agrupadas.

Un nodo [GroupShape](../../com.aspose.words/groupshape/) puede contener otros nodos [Shape](../../com.aspose.words/shape/) y [GroupShape](../../com.aspose.words/groupshape/).

### HEADER_FOOTER {#HEADER-FOOTER}
```
public static int HEADER_FOOTER
```


Un objeto [HeaderFooter](../../com.aspose.words/headerfooter/) que contiene el texto de un encabezado o pie de página particular dentro de una sección.

Un nodo [HeaderFooter](../../com.aspose.words/headerfooter/) puede contener nodos [Paragraph](../../com.aspose.words/paragraph/) y [Table](../../com.aspose.words/table/).

### MOVE_FROM_RANGE_END {#MOVE-FROM-RANGE-END}
```
public static int MOVE_FROM_RANGE_END
```


Un final de un rango MoveFrom.

### MOVE_FROM_RANGE_START {#MOVE-FROM-RANGE-START}
```
public static int MOVE_FROM_RANGE_START
```


Un comienzo de un rango MoveFrom.

### MOVE_TO_RANGE_END {#MOVE-TO-RANGE-END}
```
public static int MOVE_TO_RANGE_END
```


Un final de un rango MoveTo.

### MOVE_TO_RANGE_START {#MOVE-TO-RANGE-START}
```
public static int MOVE_TO_RANGE_START
```


Un comienzo de un rango MoveTo.

### NULL {#NULL}
```
public static int NULL
```


Reservado para uso interno por Aspose.Words.

### OFFICE_MATH {#OFFICE-MATH}
```
public static int OFFICE_MATH
```


Un objeto Office Math. Puede ser una ecuación, función, matriz o uno de otros objetos matemáticos. Puede ser una colección de objetos matemáticos y también puede contener algunos objetos no matemáticos, como secuencias de texto.

### PARAGRAPH {#PARAGRAPH}
```
public static int PARAGRAPH
```


Un párrafo de texto.

Un nodo [Paragraph](../../com.aspose.words/paragraph/) es un contenedor para elementos de nivel en línea [Run](../../com.aspose.words/run/), [FieldStart](../../com.aspose.words/fieldstart/), [FieldSeparator](../../com.aspose.words/fieldseparator/), [FieldEnd](../../com.aspose.words/fieldend/), [FormField](../../com.aspose.words/formfield/), [Shape](../../com.aspose.words/shape/), [GroupShape](../../com.aspose.words/groupshape/), [Footnote](../../com.aspose.words/footnote/), [Comment](../../com.aspose.words/comment/), [SpecialChar](../../com.aspose.words/specialchar/), así como [BookmarkStart](../../com.aspose.words/bookmarkstart/) y [BookmarkEnd](../../com.aspose.words/bookmarkend/).

### ROW {#ROW}
```
public static int ROW
```


Una fila de una tabla.

Un nodo [Row](../../com.aspose.words/row/) puede contener nodos [Cell](../../com.aspose.words/cell/).

### RUN {#RUN}
```
public static int RUN
```


Un segmento de texto.

### SECTION {#SECTION}
```
public static int SECTION
```


Un objeto [Section](../../com.aspose.words/section/) que corresponde a una sección en un documento de Word.

Un nodo [Section](../../com.aspose.words/section/) puede contener nodos [Body](../../com.aspose.words/body/) y [HeaderFooter](../../com.aspose.words/headerfooter/).

### SHAPE {#SHAPE}
```
public static int SHAPE
```


Un objeto de dibujo, como una forma OfficeArt, una imagen o un objeto OLE.

Un nodo [Shape](../../com.aspose.words/shape/) puede contener nodos [Paragraph](../../com.aspose.words/paragraph/) y [Table](../../com.aspose.words/table/).

### SMART_TAG {#SMART-TAG}
```
public static int SMART_TAG
```


Una etiqueta inteligente alrededor de una o más estructuras en línea (segmentos, imágenes, campos, etc.) dentro de un párrafo.

### SPECIAL_CHAR {#SPECIAL-CHAR}
```
public static int SPECIAL_CHAR
```


Un carácter especial que no es uno de los tipos de caracteres especiales más específicos.

### STRUCTURED_DOCUMENT_TAG {#STRUCTURED-DOCUMENT-TAG}
```
public static int STRUCTURED_DOCUMENT_TAG
```


Permite definir información específica del cliente y sus medios de presentación.

### STRUCTURED_DOCUMENT_TAG_RANGE_END {#STRUCTURED-DOCUMENT-TAG-RANGE-END}
```
public static int STRUCTURED_DOCUMENT_TAG_RANGE_END
```


Un final de la etiqueta estructurada de documento **ranged** que acepta contenido de múltiples secciones.

### STRUCTURED_DOCUMENT_TAG_RANGE_START {#STRUCTURED-DOCUMENT-TAG-RANGE-START}
```
public static int STRUCTURED_DOCUMENT_TAG_RANGE_START
```


Un inicio de la etiqueta estructurada de documento **ranged** que acepta contenido de múltiples secciones.

### SUB_DOCUMENT {#SUB-DOCUMENT}
```
public static int SUB_DOCUMENT
```


Un nodo de subdocumento que es un enlace a otro documento.

### SYSTEM {#SYSTEM}
```
public static int SYSTEM
```


Reservado para uso interno por Aspose.Words.

### TABLE {#TABLE}
```
public static int TABLE
```


Un objeto [Table](../../com.aspose.words/table/) que representa una tabla en un documento de Word.

Un nodo [Table](../../com.aspose.words/table/) puede contener nodos [Row](../../com.aspose.words/row/).

### length {#length}
```
public static int length
```


### fromName(String nodeTypeName) {#fromName-java.lang.String}
```
public static int fromName(String nodeTypeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| nodeTypeName | java.lang.String |  |

**Returns:**
int
### getName(int nodeType) {#getName-int}
```
public static String getName(int nodeType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| nodeType | int |  |

**Returns:**
java.lang.String
