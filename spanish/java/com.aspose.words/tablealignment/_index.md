---
title: "TableAlignment"
linktitle: "TableAlignment"
second_title: "Aspose.Words para Java"
description: "Especifica la alineación para una tabla en línea en Java."
type: docs
weight: 657
url: /es/java/com.aspose.words/tablealignment/
---

**Inheritance:**
java.lang.Object
```
public class TableAlignment
```

Especifica la alineación para una tabla en línea.

 **Examples:** 

Muestra cómo aplicar un borde de contorno a una tabla.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [CENTER](#CENTER) | La tabla está centrada. |
| [LEFT](#LEFT) | La tabla está alineada a la izquierda. |
| [RIGHT](#RIGHT) | La tabla está alineada a la derecha. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String tableAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int tableAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int tableAlignment)](#toString-int) |  |
### CENTER {#CENTER}
```
public static int CENTER
```


La tabla está centrada.

### LEFT {#LEFT}
```
public static int LEFT
```


La tabla está alineada a la izquierda.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


La tabla está alineada a la derecha.

### length {#length}
```
public static int length
```


### fromName(String tableAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String tableAlignmentName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| tableAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int tableAlignment) {#getName-int}
```
public static String getName(int tableAlignment)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| tableAlignment | int |  |

**Returns:**
java.lang.String
