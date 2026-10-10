---
title: "CellVerticalAlignment"
linktitle: "CellVerticalAlignment"
second_title: "Aspose.Words para Java"
description: "Especifica la justificación vertical del texto dentro de una celda de tabla en Java."
type: docs
weight: 63
url: /es/java/com.aspose.words/cellverticalalignment/
---

**Inheritance:**
java.lang.Object
```
public class CellVerticalAlignment
```

Especifica la justificación vertical del texto dentro de una celda de tabla.

 **Examples:** 

Muestra cómo crear una tabla formateada de 2x2.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.write("Row 1, cell 1.");
 builder.insertCell();
 builder.write("Row 1, cell 2.");
 builder.endRow();

 // While building the table, the document builder will apply its current RowFormat/CellFormat property values
 // to the current row/cell that its cursor is in and any new rows/cells as it creates them.
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(0).getCellFormat().getVerticalAlignment());
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(1).getCellFormat().getVerticalAlignment());

 builder.insertCell();
 builder.getRowFormat().setHeight(100.0);
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 2, cell 1.");
 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 2, cell 2.");
 builder.endRow();
 builder.endTable();

 // Previously added rows and cells are not retroactively affected by changes to the builder's formatting.
 Assert.assertEquals(0.0, table.getRows().get(0).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.AUTO, table.getRows().get(0).getRowFormat().getHeightRule());
 Assert.assertEquals(100.0, table.getRows().get(1).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.EXACTLY, table.getRows().get(1).getRowFormat().getHeightRule());
 Assert.assertEquals(TextOrientation.UPWARD, table.getRows().get(1).getCells().get(0).getCellFormat().getOrientation());
 Assert.assertEquals(TextOrientation.DOWNWARD, table.getRows().get(1).getCells().get(1).getCellFormat().getOrientation());

 doc.save(getArtifactsDir() + "DocumentBuilder.BuildTable.docx");
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [BOTTOM](#BOTTOM) | El texto está alineado en la parte inferior de la celda. |
| [CENTER](#CENTER) | El texto está alineado en el medio de una celda. |
| [TOP](#TOP) | El texto está alineado en la parte superior de una celda. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String cellVerticalAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int cellVerticalAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int cellVerticalAlignment)](#toString-int) |  |
### BOTTOM {#BOTTOM}
```
public static int BOTTOM
```


El texto está alineado en la parte inferior de la celda.

### CENTER {#CENTER}
```
public static int CENTER
```


El texto está alineado en el medio de una celda.

### TOP {#TOP}
```
public static int TOP
```


El texto está alineado en la parte superior de una celda.

### length {#length}
```
public static int length
```


### fromName(String cellVerticalAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String cellVerticalAlignmentName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| cellVerticalAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int cellVerticalAlignment) {#getName-int}
```
public static String getName(int cellVerticalAlignment)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| cellVerticalAlignment | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int cellVerticalAlignment) {#toString-int}
```
public static String toString(int cellVerticalAlignment)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| cellVerticalAlignment | int |  |

**Returns:**
java.lang.String
