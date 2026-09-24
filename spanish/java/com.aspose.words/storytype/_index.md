---
title: "StoryType"
linktitle: "StoryType"
second_title: "Aspose.Words para Java"
description: "El texto de un documento Word se almacena en historias en Java."
type: docs
weight: 634
url: /es/java/com.aspose.words/storytype/
---

**Inheritance:**
java.lang.Object
```
public class StoryType
```

El texto de un documento Word se almacena en historias. [StoryType](../../com.aspose.words/storytype/) identifica una historia.

 **Examples:** 

Muestra cómo eliminar todas las formas de un nodo.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Use a DocumentBuilder to insert a shape. This is an inline shape,
 // which has a parent Paragraph, which is a child node of the first section's Body.
 builder.insertShape(ShapeType.CUBE, 100.0, 100.0);

 Assert.assertEquals(doc.getChildNodes(NodeType.SHAPE, true).getCount(), 1);

 // We can delete all shapes from the child paragraphs of this Body.
 Assert.assertEquals(doc.getFirstSection().getBody().getStoryType(), StoryType.MAIN_TEXT);
 doc.getFirstSection().getBody().deleteShapes();

 Assert.assertEquals(doc.getChildNodes(NodeType.SHAPE, true).getCount(), 0);
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [COMMENTS](#COMMENTS) | Contiene comentarios del documento (anotaciones), representados por [Comment](../../com.aspose.words/comment/). |
| [ENDNOTES](#ENDNOTES) | Contiene el texto de notas al final, representado por [Footnote](../../com.aspose.words/footnote/). |
| [ENDNOTE_CONTINUATION_NOTICE](#ENDNOTE-CONTINUATION-NOTICE) | Contiene el texto del separador de aviso de continuación de nota al final. |
| [ENDNOTE_CONTINUATION_SEPARATOR](#ENDNOTE-CONTINUATION-SEPARATOR) | Contiene el texto del separador de continuación de nota al final. |
| [ENDNOTE_SEPARATOR](#ENDNOTE-SEPARATOR) | Contiene el texto del separador de nota al final. |
| [EVEN_PAGES_FOOTER](#EVEN-PAGES-FOOTER) | Contiene el texto del pie de página de las páginas pares, representado por [HeaderFooter](../../com.aspose.words/headerfooter/). |
| [EVEN_PAGES_HEADER](#EVEN-PAGES-HEADER) | Contiene el texto del encabezado de las páginas pares, representado por [HeaderFooter](../../com.aspose.words/headerfooter/). |
| [FIRST_PAGE_FOOTER](#FIRST-PAGE-FOOTER) | Contiene el texto del pie de página de la primera página, representado por [HeaderFooter](../../com.aspose.words/headerfooter/). |
| [FIRST_PAGE_HEADER](#FIRST-PAGE-HEADER) | Contiene el texto del encabezado de la primera página, representado por [HeaderFooter](../../com.aspose.words/headerfooter/). |
| [FOOTNOTES](#FOOTNOTES) | Contiene el texto de la nota al pie, representado por [Footnote](../../com.aspose.words/footnote/). |
| [FOOTNOTE_CONTINUATION_NOTICE](#FOOTNOTE-CONTINUATION-NOTICE) | Contiene el texto del separador del aviso de continuación de nota al pie. |
| [FOOTNOTE_CONTINUATION_SEPARATOR](#FOOTNOTE-CONTINUATION-SEPARATOR) | Contiene el texto del separador de continuación de nota al pie. |
| [FOOTNOTE_SEPARATOR](#FOOTNOTE-SEPARATOR) | Contiene el texto del separador de nota al pie. |
| [MAIN_TEXT](#MAIN-TEXT) | Contiene el texto principal del documento, representado por [Body](../../com.aspose.words/body/). |
| [NONE](#NONE) | Valor predeterminado. |
| [PRIMARY_FOOTER](#PRIMARY-FOOTER) | Contiene el texto del pie de página principal. |
| [PRIMARY_HEADER](#PRIMARY-HEADER) | Contiene el texto del encabezado principal. |
| [TEXTBOX](#TEXTBOX) | Contiene el texto de forma o cuadro de texto, representado por [Shape](../../com.aspose.words/shape/). |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String storyTypeName)](#fromName-java.lang.String) |  |
| [getName(int storyType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int storyType)](#toString-int) |  |
### COMMENTS {#COMMENTS}
```
public static int COMMENTS
```


Contiene comentarios del documento (anotaciones), representados por [Comment](../../com.aspose.words/comment/).

### ENDNOTES {#ENDNOTES}
```
public static int ENDNOTES
```


Contiene el texto de notas al final, representado por [Footnote](../../com.aspose.words/footnote/).

### ENDNOTE_CONTINUATION_NOTICE {#ENDNOTE-CONTINUATION-NOTICE}
```
public static int ENDNOTE_CONTINUATION_NOTICE
```


Contiene el texto del separador de aviso de continuación de nota al final.

### ENDNOTE_CONTINUATION_SEPARATOR {#ENDNOTE-CONTINUATION-SEPARATOR}
```
public static int ENDNOTE_CONTINUATION_SEPARATOR
```


Contiene el texto del separador de continuación de nota al final.

### ENDNOTE_SEPARATOR {#ENDNOTE-SEPARATOR}
```
public static int ENDNOTE_SEPARATOR
```


Contiene el texto del separador de nota al final.

### EVEN_PAGES_FOOTER {#EVEN-PAGES-FOOTER}
```
public static int EVEN_PAGES_FOOTER
```


Contiene el texto del pie de página de las páginas pares, representado por [HeaderFooter](../../com.aspose.words/headerfooter/).

### EVEN_PAGES_HEADER {#EVEN-PAGES-HEADER}
```
public static int EVEN_PAGES_HEADER
```


Contiene el texto del encabezado de las páginas pares, representado por [HeaderFooter](../../com.aspose.words/headerfooter/).

### FIRST_PAGE_FOOTER {#FIRST-PAGE-FOOTER}
```
public static int FIRST_PAGE_FOOTER
```


Contiene el texto del pie de página de la primera página, representado por [HeaderFooter](../../com.aspose.words/headerfooter/).

### FIRST_PAGE_HEADER {#FIRST-PAGE-HEADER}
```
public static int FIRST_PAGE_HEADER
```


Contiene el texto del encabezado de la primera página, representado por [HeaderFooter](../../com.aspose.words/headerfooter/).

### FOOTNOTES {#FOOTNOTES}
```
public static int FOOTNOTES
```


Contiene el texto de la nota al pie, representado por [Footnote](../../com.aspose.words/footnote/).

### FOOTNOTE_CONTINUATION_NOTICE {#FOOTNOTE-CONTINUATION-NOTICE}
```
public static int FOOTNOTE_CONTINUATION_NOTICE
```


Contiene el texto del separador del aviso de continuación de nota al pie.

### FOOTNOTE_CONTINUATION_SEPARATOR {#FOOTNOTE-CONTINUATION-SEPARATOR}
```
public static int FOOTNOTE_CONTINUATION_SEPARATOR
```


Contiene el texto del separador de continuación de nota al pie.

### FOOTNOTE_SEPARATOR {#FOOTNOTE-SEPARATOR}
```
public static int FOOTNOTE_SEPARATOR
```


Contiene el texto del separador de nota al pie.

### MAIN_TEXT {#MAIN-TEXT}
```
public static int MAIN_TEXT
```


Contiene el texto principal del documento, representado por [Body](../../com.aspose.words/body/).

### NONE {#NONE}
```
public static int NONE
```


Valor predeterminado. No existe tal historia en el documento.

### PRIMARY_FOOTER {#PRIMARY-FOOTER}
```
public static int PRIMARY_FOOTER
```


Contiene el texto del pie de página principal. Cuando el pie de página es diferente para páginas impares y pares, contiene el texto del pie de página de las páginas impares. Representado por [HeaderFooter](../../com.aspose.words/headerfooter/).

### PRIMARY_HEADER {#PRIMARY-HEADER}
```
public static int PRIMARY_HEADER
```


Contiene el texto del encabezado principal. Cuando el encabezado es diferente para páginas impares y pares, contiene el texto del encabezado de las páginas impares. Representado por [HeaderFooter](../../com.aspose.words/headerfooter/).

### TEXTBOX {#TEXTBOX}
```
public static int TEXTBOX
```


Contiene el texto de forma o cuadro de texto, representado por [Shape](../../com.aspose.words/shape/).

### length {#length}
```
public static int length
```


### fromName(String storyTypeName) {#fromName-java.lang.String}
```
public static int fromName(String storyTypeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| storyTypeName | java.lang.String |  |

**Returns:**
int
### getName(int storyType) {#getName-int}
```
public static String getName(int storyType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| storyType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int storyType) {#toString-int}
```
public static String toString(int storyType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| storyType | int |  |

**Returns:**
java.lang.String
