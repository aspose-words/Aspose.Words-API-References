---
title: "TableContentAlignment"
linktitle: "TableContentAlignment"
second_title: "Aspose.Words per Java"
description: "Consente di specificare l'allineamento del contenuto della tabella da utilizzare durante l'esportazione in formato Markdown in Java."
type: docs
weight: 659
url: /it/java/com.aspose.words/tablecontentalignment/
---

**Inheritance:**
java.lang.Object
```
public class TableContentAlignment
```

Consente di specificare l'allineamento del contenuto della tabella da utilizzare quando si esporta in formato Markdown.

 **Examples:** 

Mostra come allineare i contenuti nelle tabelle.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [AUTO](#AUTO) | L'allineamento sarà preso dal primo paragrafo nella colonna della tabella corrispondente. |
| [CENTER](#CENTER) | Il contenuto delle tabelle sarà allineato al Centro. |
| [LEFT](#LEFT) | Il contenuto delle tabelle sarà allineato a Sinistra. |
| [RIGHT](#RIGHT) | Il contenuto delle tabelle sarà allineato a Destra. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String tableContentAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int tableContentAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int tableContentAlignment)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


L'allineamento sarà preso dal primo paragrafo nella colonna della tabella corrispondente.

### CENTER {#CENTER}
```
public static int CENTER
```


Il contenuto delle tabelle sarà allineato al Centro.

### LEFT {#LEFT}
```
public static int LEFT
```


Il contenuto delle tabelle sarà allineato a Sinistra.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Il contenuto delle tabelle sarà allineato a Destra.

### length {#length}
```
public static int length
```


### fromName(String tableContentAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String tableContentAlignmentName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| tableContentAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int tableContentAlignment) {#getName-int}
```
public static String getName(int tableContentAlignment)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| tableContentAlignment | int |  |

**Returns:**
java.lang.String
