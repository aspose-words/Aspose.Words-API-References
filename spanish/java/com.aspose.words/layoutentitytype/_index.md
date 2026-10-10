---
title: "LayoutEntityType"
linktitle: "LayoutEntityType"
second_title: "Aspose.Words para Java"
description: "Tipos de las entidades de diseño en Java."
type: docs
weight: 416
url: /es/java/com.aspose.words/layoutentitytype/
---

**Inheritance:**
java.lang.Object
```
public class LayoutEntityType
```

Tipos de las entidades de diseño.

 **Examples:** 

Muestra formas de recorrer las entidades de diseño de un documento.

```

 public void layoutEnumerator() throws Exception {
     // Open a document that contains a variety of layout entities.
     // Layout entities are pages, cells, rows, lines, and other objects included in the LayoutEntityType enum.
     // Each layout entity has a rectangular space that it occupies in the document body.
     Document doc = new Document(getMyDir() + "Layout entities.docx");

     // Create an enumerator that can traverse these entities like a tree.
     LayoutEnumerator layoutEnumerator = new LayoutEnumerator(doc);

     Assert.assertEquals(doc, layoutEnumerator.getDocument());

     layoutEnumerator.moveParent(LayoutEntityType.PAGE);

     Assert.assertEquals(LayoutEntityType.PAGE, layoutEnumerator.getType());
     Assert.assertThrows(IllegalStateException.class, () -> System.out.println(layoutEnumerator.getText()));

     // We can call this method to make sure that the enumerator will be at the first layout entity.
     layoutEnumerator.reset();

     // There are two orders that determine how the layout enumerator continues traversing layout entities
     // when it encounters entities that span across multiple pages.
     // 1 -  In visual order:
     // When moving through an entity's children that span multiple pages,
     // page layout takes precedence, and we move to other child elements on this page and avoid the ones on the next.
     System.out.println("Traversing from first to last, elements between pages separated:");
     traverseLayoutForward(layoutEnumerator, 1);

     // Our enumerator is now at the end of the collection. We can traverse the layout entities backwards to go back to the beginning.
     System.out.println("Traversing from last to first, elements between pages separated:");
     traverseLayoutBackward(layoutEnumerator, 1);

     // 2 -  In logical order:
     // When moving through an entity's children that span multiple pages,
     // the enumerator will move between pages to traverse all the child entities.
     System.out.println("Traversing from first to last, elements between pages mixed:");
     traverseLayoutForwardLogical(layoutEnumerator, 1);

     System.out.println("Traversing from last to first, elements between pages mixed:");
     traverseLayoutBackwardLogical(layoutEnumerator, 1);
 }

 /// 
 /// Enumerate through layoutEnumerator's layout entity collection front-to-back,
 /// in a depth-first manner, and in the "Visual" order.
 /// 
 private static void traverseLayoutForward(LayoutEnumerator layoutEnumerator, int depth) throws Exception {
     do {
         printCurrentEntity(layoutEnumerator, depth);

         if (layoutEnumerator.moveFirstChild()) {
             traverseLayoutForward(layoutEnumerator, depth + 1);
             layoutEnumerator.moveParent();
         }
     } while (layoutEnumerator.moveNext());
 }

 /// 
 /// Enumerate through layoutEnumerator's layout entity collection back-to-front,
 /// in a depth-first manner, and in the "Visual" order.
 /// 
 private static void traverseLayoutBackward(LayoutEnumerator layoutEnumerator, int depth) throws Exception {
     do {
         printCurrentEntity(layoutEnumerator, depth);

         if (layoutEnumerator.moveLastChild()) {
             traverseLayoutBackward(layoutEnumerator, depth + 1);
             layoutEnumerator.moveParent();
         }
     } while (layoutEnumerator.movePrevious());
 }

 /// 
 /// Enumerate through layoutEnumerator's layout entity collection front-to-back,
 /// in a depth-first manner, and in the "Logical" order.
 /// 
 private static void traverseLayoutForwardLogical(LayoutEnumerator layoutEnumerator, int depth) throws Exception {
     do {
         printCurrentEntity(layoutEnumerator, depth);

         if (layoutEnumerator.moveFirstChild()) {
             traverseLayoutForwardLogical(layoutEnumerator, depth + 1);
             layoutEnumerator.moveParent();
         }
     } while (layoutEnumerator.moveNextLogical());
 }

 /// 
 /// Enumerate through layoutEnumerator's layout entity collection back-to-front,
 /// in a depth-first manner, and in the "Logical" order.
 /// 
 private static void traverseLayoutBackwardLogical(LayoutEnumerator layoutEnumerator, int depth) throws Exception {
     do {
         printCurrentEntity(layoutEnumerator, depth);

         if (layoutEnumerator.moveLastChild()) {
             traverseLayoutBackwardLogical(layoutEnumerator, depth + 1);
             layoutEnumerator.moveParent();
         }
     } while (layoutEnumerator.movePreviousLogical());
 }

 /// 
 /// Print information about layoutEnumerator's current entity to the console, while indenting the text with tab characters
 /// based on its depth relative to the root node that we provided in the constructor LayoutEnumerator instance.
 /// The rectangle that we process at the end represents the area and location that the entity takes up in the document.
 /// 
 private static void printCurrentEntity(LayoutEnumerator layoutEnumerator, int indent) throws Exception {
     String tabs = StringUtils.repeat("\t", indent);

     System.out.println(layoutEnumerator.getKind().equals("")
             ? MessageFormat.format("{0}-> Entity type: {1}", tabs, layoutEnumerator.getType())
             : MessageFormat.format("{0}-> Entity type & kind: {1}, {2}", tabs, layoutEnumerator.getType(), layoutEnumerator.getKind()));

     // Only spans can contain text.
     if (layoutEnumerator.getType() == LayoutEntityType.SPAN)
         System.out.println("{tabs}   Span contents: \"{layoutEnumerator.Text}\"");

     Rectangle2D.Float leRect = layoutEnumerator.getRectangle();
     System.out.println(MessageFormat.format("{0}   Rectangle dimensions {1}x{2}, X={3} Y={4}", tabs, leRect.getWidth(), leRect.getHeight(), leRect.getX(), leRect.getY()));
     System.out.println(MessageFormat.format("{0}   Page {1}", tabs, layoutEnumerator.getPageIndex()));
 }
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [CELL](#CELL) | Representa una celda de tabla. |
| [COLUMN](#COLUMN) | Representa una columna de texto en una página. |
| [COMMENT](#COMMENT) | Representa un marcador de posición para el contenido de comentarios. |
| [ENDNOTE](#ENDNOTE) | Representa un marcador de posición para el contenido de notas finales. |
| [FOOTNOTE](#FOOTNOTE) | Representa un marcador de posición para el contenido de notas al pie. |
| [HEADER_FOOTER](#HEADER-FOOTER) | Representa un marcador de posición para el contenido de encabezado/pie de página en una página. |
| [LINE](#LINE) | Representa una línea de caracteres de texto y objetos en línea. |
| [NONE](#NONE) | Valor predeterminado. |
| [NOTE](#NOTE) | Representa un marcador de posición para el contenido de la nota. |
| [NOTE_SEPARATOR](#NOTE-SEPARATOR) | Representa el separador de notas al pie/finales. |
| [PAGE](#PAGE) | Representa una página de un documento. |
| [ROW](#ROW) | Representa una fila de tabla. |
| [SPAN](#SPAN) | Representa uno o más caracteres en una línea. |
| [TEXT_BOX](#TEXT-BOX) | Representa el área de texto dentro de una forma. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String layoutEntityTypeName)](#fromName-java.lang.String) |  |
| [fromNames(Set layoutEntityTypeNames)](#fromNames-java.util.Set) |  |
| [getName(int layoutEntityType)](#getName-int) |  |
| [getNames(int layoutEntityType)](#getNames-int) |  |
| [getValues()](#getValues) |  |
| [toString(int layoutEntityType)](#toString-int) |  |
| [toStringSet(int attr)](#toStringSet-int) |  |
### CELL {#CELL}
```
public static int CELL
```


Representa una celda de tabla. La celda puede tener entidades hijas [LINE](../../com.aspose.words/layoutentitytype/\#LINE) y [ROW](../../com.aspose.words/layoutentitytype/\#ROW).

### COLUMN {#COLUMN}
```
public static int COLUMN
```


Representa una columna de texto en una página. La columna puede tener las mismas entidades hijas que [CELL](../../com.aspose.words/layoutentitytype/\#CELL), además de [FOOTNOTE](../../com.aspose.words/layoutentitytype/\#FOOTNOTE), [ENDNOTE](../../com.aspose.words/layoutentitytype/\#ENDNOTE) y [NOTE\_SEPARATOR](../../com.aspose.words/layoutentitytype/\#NOTE-SEPARATOR).

### COMMENT {#COMMENT}
```
public static int COMMENT
```


Representa un marcador de posición para el contenido del comentario. El comentario puede tener [LINE](../../com.aspose.words/layoutentitytype/\#LINE) y [ROW](../../com.aspose.words/layoutentitytype/\#ROW) entidades secundarias.

### ENDNOTE {#ENDNOTE}
```
public static int ENDNOTE
```


Representa un marcador de posición para el contenido de la nota al final. La nota al final puede tener [NOTE](../../com.aspose.words/layoutentitytype/\#NOTE) entidades secundarias.

### FOOTNOTE {#FOOTNOTE}
```
public static int FOOTNOTE
```


Representa un marcador de posición para el contenido de la nota al pie. La nota al pie puede tener [NOTE](../../com.aspose.words/layoutentitytype/\#NOTE) entidades secundarias.

### HEADER_FOOTER {#HEADER-FOOTER}
```
public static int HEADER_FOOTER
```


Representa un marcador de posición para el contenido del encabezado/pie de página. HeaderFooter puede tener [LINE](../../com.aspose.words/layoutentitytype/\#LINE) y [ROW](../../com.aspose.words/layoutentitytype/\#ROW) entidades secundarias.

### LINE {#LINE}
```
public static int LINE
```


Representa una línea de caracteres de texto y objetos en línea. Line puede tener [SPAN](../../com.aspose.words/layoutentitytype/\#SPAN) entidades secundarias.

### NONE {#NONE}
```
public static int NONE
```


Valor predeterminado.

### NOTE {#NOTE}
```
public static int NOTE
```


Representa un marcador de posición para el contenido de la nota. Note puede tener [LINE](../../com.aspose.words/layoutentitytype/\#LINE) y [ROW](../../com.aspose.words/layoutentitytype/\#ROW) entidades secundarias.

### NOTE_SEPARATOR {#NOTE-SEPARATOR}
```
public static int NOTE_SEPARATOR
```


Representa el separador de nota al pie/nota al final. NoteSeparator puede tener [LINE](../../com.aspose.words/layoutentitytype/\#LINE) y [ROW](../../com.aspose.words/layoutentitytype/\#ROW) entidades secundarias.

### PAGE {#PAGE}
```
public static int PAGE
```


Representa una página de un documento. Page puede tener [COLUMN](../../com.aspose.words/layoutentitytype/\#COLUMN), [HEADER\_FOOTER](../../com.aspose.words/layoutentitytype/\#HEADER-FOOTER) y [COMMENT](../../com.aspose.words/layoutentitytype/\#COMMENT) entidades secundarias.

### ROW {#ROW}
```
public static int ROW
```


Representa una fila de tabla. Row puede tener [CELL](../../com.aspose.words/layoutentitytype/\#CELL) como entidades secundarias.

### SPAN {#SPAN}
```
public static int SPAN
```


Representa uno o más caracteres en una línea. Esto incluye caracteres especiales como marcadores de inicio/final de campo, marcadores y comentarios. Span no puede tener entidades secundarias.

### TEXT_BOX {#TEXT-BOX}
```
public static int TEXT_BOX
```


Representa el área de texto dentro de una forma. Textbox puede tener [LINE](../../com.aspose.words/layoutentitytype/\#LINE) y [ROW](../../com.aspose.words/layoutentitytype/\#ROW) entidades secundarias.

### length {#length}
```
public static int length
```


### fromName(String layoutEntityTypeName) {#fromName-java.lang.String}
```
public static int fromName(String layoutEntityTypeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| layoutEntityTypeName | java.lang.String |  |

**Returns:**
int
### fromNames(Set layoutEntityTypeNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set layoutEntityTypeNames)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| layoutEntityTypeNames | java.util.Set |  |

**Returns:**
int
### getName(int layoutEntityType) {#getName-int}
```
public static String getName(int layoutEntityType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| layoutEntityType | int |  |

**Returns:**
java.lang.String
### getNames(int layoutEntityType) {#getNames-int}
```
public static Set getNames(int layoutEntityType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| layoutEntityType | int |  |

**Returns:**
java.util.Set
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int layoutEntityType) {#toString-int}
```
public static String toString(int layoutEntityType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| layoutEntityType | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
