---
title: "TextOrientation"
linktitle: "TextOrientation"
second_title: "Aspose.Words для Java"
description: "Указывает ориентацию текста на странице в ячейке таблицы или текстовой рамке в Java."
type: docs
weight: 675
url: /ru/java/com.aspose.words/textorientation/
---

**Inheritance:**
java.lang.Object
```
public class TextOrientation
```

Указывает ориентацию текста на странице, в ячейке таблицы или в текстовой рамке.

 **Examples:** 

Показывает, как построить отформатированную таблицу 2x2.

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
## Поля

| Поле | Описание |
| --- | --- |
| [DOWNWARD](#DOWNWARD) | Текст вращается на 90 градусов вправо, чтобы отображаться сверху вниз (tb-rl). |
| [HORIZONTAL](#HORIZONTAL) | Текст располагается горизонтально (lr-tb). |
| [HORIZONTAL_ROTATED_FAR_EAST](#HORIZONTAL-ROTATED-FAR-EAST) | Текст располагается горизонтально, но символы Дальнего Востока вращаются на 90 градусов влево (lr-tb-v). |
| [UPWARD](#UPWARD) | Текст вращается на 90 градусов влево, чтобы отображаться снизу вверх (bt-lr). |
| [VERTICAL_FAR_EAST](#VERTICAL-FAR-EAST) | Символы Дальнего Востока отображаются вертикально, остальной текст вращается на 90 градусов вправо, чтобы отображаться сверху вниз (tb-rl-v). |
| [VERTICAL_ROTATED_FAR_EAST](#VERTICAL-ROTATED-FAR-EAST) | Символы Дальнего Востока отображаются вертикально, другой текст повернут на 90 градусов вправо, чтобы отображаться сверху вниз вертикально, затем слева направо горизонтально (tb-lr-v). |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String textOrientationName)](#fromName-java.lang.String) |  |
| [getName(int textOrientation)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int textOrientation)](#toString-int) |  |
### DOWNWARD {#DOWNWARD}
```
public static int DOWNWARD
```


Текст вращается на 90 градусов вправо, чтобы отображаться сверху вниз (tb-rl).

### HORIZONTAL {#HORIZONTAL}
```
public static int HORIZONTAL
```


Текст располагается горизонтально (lr-tb).

### HORIZONTAL_ROTATED_FAR_EAST {#HORIZONTAL-ROTATED-FAR-EAST}
```
public static int HORIZONTAL_ROTATED_FAR_EAST
```


Текст располагается горизонтально, но символы Дальнего Востока вращаются на 90 градусов влево (lr-tb-v).

### UPWARD {#UPWARD}
```
public static int UPWARD
```


Текст вращается на 90 градусов влево, чтобы отображаться снизу вверх (bt-lr).

### VERTICAL_FAR_EAST {#VERTICAL-FAR-EAST}
```
public static int VERTICAL_FAR_EAST
```


Символы Дальнего Востока отображаются вертикально, остальной текст вращается на 90 градусов вправо, чтобы отображаться сверху вниз (tb-rl-v).

### VERTICAL_ROTATED_FAR_EAST {#VERTICAL-ROTATED-FAR-EAST}
```
public static int VERTICAL_ROTATED_FAR_EAST
```


Символы Дальнего Востока отображаются вертикально, другой текст повернут на 90 градусов вправо, чтобы отображаться сверху вниз вертикально, затем слева направо горизонтально (tb-lr-v).

### length {#length}
```
public static int length
```


### fromName(String textOrientationName) {#fromName-java.lang.String}
```
public static int fromName(String textOrientationName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| textOrientationName | java.lang.String |  |

**Returns:**
int
### getName(int textOrientation) {#getName-int}
```
public static String getName(int textOrientation)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| textOrientation | int |  |

**Returns:**
java.lang.String
