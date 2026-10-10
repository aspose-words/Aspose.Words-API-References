---
title: "TextOrientation"
linktitle: "TextOrientation"
second_title: "Aspose.Words para Java"
description: "Especifica la orientación del texto en una página dentro de una celda de tabla o un marco de texto en Java."
type: docs
weight: 675
url: /es/java/com.aspose.words/textorientation/
---

**Inheritance:**
java.lang.Object
```
public class TextOrientation
```

Especifica la orientación del texto en una página, en una celda de tabla o en un marco de texto.

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
| [DOWNWARD](#DOWNWARD) | El texto se rota 90 grados a la derecha para aparecer de arriba a abajo (tb-rl). |
| [HORIZONTAL](#HORIZONTAL) | El texto se dispone horizontalmente (lr-tb). |
| [HORIZONTAL_ROTATED_FAR_EAST](#HORIZONTAL-ROTATED-FAR-EAST) | El texto se dispone horizontalmente, pero los caracteres de Extremo Oriente se rotan 90 grados a la izquierda (lr-tb-v). |
| [UPWARD](#UPWARD) | El texto se rota 90 grados a la izquierda para aparecer de abajo a arriba (bt-lr). |
| [VERTICAL_FAR_EAST](#VERTICAL-FAR-EAST) | Los caracteres de Extremo Oriente aparecen verticales, el resto del texto se rota 90 grados a la derecha para aparecer de arriba a abajo (tb-rl-v). |
| [VERTICAL_ROTATED_FAR_EAST](#VERTICAL-ROTATED-FAR-EAST) | Los caracteres del Lejano Oriente aparecen verticales, el resto del texto está rotado 90 grados a la derecha para aparecer de arriba a abajo verticalmente, luego de izquierda a derecha horizontalmente (tb-lr-v). |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String textOrientationName)](#fromName-java.lang.String) |  |
| [getName(int textOrientation)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int textOrientation)](#toString-int) |  |
### DOWNWARD {#DOWNWARD}
```
public static int DOWNWARD
```


El texto se rota 90 grados a la derecha para aparecer de arriba a abajo (tb-rl).

### HORIZONTAL {#HORIZONTAL}
```
public static int HORIZONTAL
```


El texto se dispone horizontalmente (lr-tb).

### HORIZONTAL_ROTATED_FAR_EAST {#HORIZONTAL-ROTATED-FAR-EAST}
```
public static int HORIZONTAL_ROTATED_FAR_EAST
```


El texto se dispone horizontalmente, pero los caracteres de Extremo Oriente se rotan 90 grados a la izquierda (lr-tb-v).

### UPWARD {#UPWARD}
```
public static int UPWARD
```


El texto se rota 90 grados a la izquierda para aparecer de abajo a arriba (bt-lr).

### VERTICAL_FAR_EAST {#VERTICAL-FAR-EAST}
```
public static int VERTICAL_FAR_EAST
```


Los caracteres de Extremo Oriente aparecen verticales, el resto del texto se rota 90 grados a la derecha para aparecer de arriba a abajo (tb-rl-v).

### VERTICAL_ROTATED_FAR_EAST {#VERTICAL-ROTATED-FAR-EAST}
```
public static int VERTICAL_ROTATED_FAR_EAST
```


Los caracteres del Lejano Oriente aparecen verticales, el resto del texto está rotado 90 grados a la derecha para aparecer de arriba a abajo verticalmente, luego de izquierda a derecha horizontalmente (tb-lr-v).

### length {#length}
```
public static int length
```


### fromName(String textOrientationName) {#fromName-java.lang.String}
```
public static int fromName(String textOrientationName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| textOrientationName | java.lang.String |  |

**Returns:**
int
### getName(int textOrientation) {#getName-int}
```
public static String getName(int textOrientation)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| textOrientation | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int textOrientation) {#toString-int}
```
public static String toString(int textOrientation)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| textOrientation | int |  |

**Returns:**
java.lang.String
