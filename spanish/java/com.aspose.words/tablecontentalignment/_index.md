---
title: "TableContentAlignment"
linktitle: "TableContentAlignment"
second_title: "Aspose.Words para Java"
description: "Permite especificar la alineación del contenido de la tabla que se usará al exportar al formato Markdown en Java."
type: docs
weight: 659
url: /es/java/com.aspose.words/tablecontentalignment/
---

**Inheritance:**
java.lang.Object
```
public class TableContentAlignment
```

Permite especificar la alineación del contenido de la tabla que se usará al exportar al formato Markdown.

 **Examples:** 

Muestra cómo alinear el contenido en tablas.

```

 DocumentBuilder builder = new DocumentBuilder();

 builder.insertCell();
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.RIGHT);
 builder.write("Cell1");
 builder.insertCell();
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 builder.write("Cell2");

 MarkdownSaveOptions saveOptions = new MarkdownSaveOptions(); { saveOptions.setTableContentAlignment(tableContentAlignment); }

 builder.getDocument().save(getArtifactsDir() + "MarkdownSaveOptions.MarkdownDocumentTableContentAlignment.md", saveOptions);

 Document doc = new Document(getArtifactsDir() + "MarkdownSaveOptions.MarkdownDocumentTableContentAlignment.md");
 Table table = doc.getFirstSection().getBody().getTables().get(0);

 switch (tableContentAlignment)
 {
     case TableContentAlignment.AUTO:
         Assert.assertEquals(ParagraphAlignment.RIGHT,
             table.getFirstRow().getCells().get(0).getFirstParagraph().getParagraphFormat().getAlignment());
         Assert.assertEquals(ParagraphAlignment.CENTER,
             table.getFirstRow().getCells().get(1).getFirstParagraph().getParagraphFormat().getAlignment());
         break;
     case TableContentAlignment.LEFT:
         Assert.assertEquals(ParagraphAlignment.LEFT,
             table.getFirstRow().getCells().get(0).getFirstParagraph().getParagraphFormat().getAlignment());
         Assert.assertEquals(ParagraphAlignment.LEFT,
             table.getFirstRow().getCells().get(1).getFirstParagraph().getParagraphFormat().getAlignment());
         break;
     case TableContentAlignment.CENTER:
         Assert.assertEquals(ParagraphAlignment.CENTER,
             table.getFirstRow().getCells().get(0).getFirstParagraph().getParagraphFormat().getAlignment());
         Assert.assertEquals(ParagraphAlignment.CENTER,
             table.getFirstRow().getCells().get(1).getFirstParagraph().getParagraphFormat().getAlignment());
         break;
     case TableContentAlignment.RIGHT:
         Assert.assertEquals(ParagraphAlignment.RIGHT,
             table.getFirstRow().getCells().get(0).getFirstParagraph().getParagraphFormat().getAlignment());
         Assert.assertEquals(ParagraphAlignment.RIGHT,
             table.getFirstRow().getCells().get(1).getFirstParagraph().getParagraphFormat().getAlignment());
         break;
 }
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [AUTO](#AUTO) | La alineación se tomará del primer párrafo en la columna de tabla correspondiente. |
| [CENTER](#CENTER) | El contenido de las tablas se alineará al Centro. |
| [LEFT](#LEFT) | El contenido de las tablas se alineará a la Izquierda. |
| [RIGHT](#RIGHT) | El contenido de las tablas se alineará a la Derecha. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String tableContentAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int tableContentAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int tableContentAlignment)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


La alineación se tomará del primer párrafo en la columna de tabla correspondiente.

### CENTER {#CENTER}
```
public static int CENTER
```


El contenido de las tablas se alineará al Centro.

### LEFT {#LEFT}
```
public static int LEFT
```


El contenido de las tablas se alineará a la Izquierda.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


El contenido de las tablas se alineará a la Derecha.

### length {#length}
```
public static int length
```


### fromName(String tableContentAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String tableContentAlignmentName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| tableContentAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int tableContentAlignment) {#getName-int}
```
public static String getName(int tableContentAlignment)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| tableContentAlignment | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int tableContentAlignment) {#toString-int}
```
public static String toString(int tableContentAlignment)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| tableContentAlignment | int |  |

**Returns:**
java.lang.String
