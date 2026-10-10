---
title: "TableAlignment"
linktitle: "TableAlignment"
second_title: "Aspose.Words per Java"
description: "Specifica l'allineamento per una tabella inline in Java."
type: docs
weight: 657
url: /it/java/com.aspose.words/tablealignment/
---

**Inheritance:**
java.lang.Object
```
public class TableAlignment
```

Specifica l'allineamento per una tabella inline.

 **Examples:** 

Mostra come applicare un bordo di contorno a una tabella.

```

 Document doc = new Document(getMyDir() + "Tables.docx");
 Table table = doc.getFirstSection().getBody().getTables().get(0);

 // Align the table to the center of the page.
 table.setAlignment(TableAlignment.CENTER);

 // Clear any existing borders and shading from the table.
 table.clearBorders();
 table.clearShading();

 // Add green borders to the outline of the table.
 table.setBorder(BorderType.LEFT, LineStyle.SINGLE, 1.5, Color.GREEN, true);
 table.setBorder(BorderType.RIGHT, LineStyle.SINGLE, 1.5, Color.GREEN, true);
 table.setBorder(BorderType.TOP, LineStyle.SINGLE, 1.5, Color.GREEN, true);
 table.setBorder(BorderType.BOTTOM, LineStyle.SINGLE, 1.5, Color.GREEN, true);

 // Fill the cells with a light green solid color.
 table.setShading(TextureIndex.TEXTURE_SOLID, Color.GREEN, Color.GREEN);

 doc.save(getArtifactsDir() + "Table.SetOutlineBorders.docx");
 
```
## Campi

| Campo | Descrizione |
| --- | --- |
| [CENTER](#CENTER) | La tabella è centrata. |
| [LEFT](#LEFT) | La tabella è allineata a sinistra. |
| [RIGHT](#RIGHT) | La tabella è allineata a destra. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String tableAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int tableAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int tableAlignment)](#toString-int) |  |
### CENTER {#CENTER}
```
public static int CENTER
```


La tabella è centrata.

### LEFT {#LEFT}
```
public static int LEFT
```


La tabella è allineata a sinistra.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


La tabella è allineata a destra.

### length {#length}
```
public static int length
```


### fromName(String tableAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String tableAlignmentName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| tableAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int tableAlignment) {#getName-int}
```
public static String getName(int tableAlignment)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| tableAlignment | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int tableAlignment) {#toString-int}
```
public static String toString(int tableAlignment)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| tableAlignment | int |  |

**Returns:**
java.lang.String
