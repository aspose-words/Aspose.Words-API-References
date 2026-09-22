---
title: "TextOrientation"
linktitle: "TextOrientation"
second_title: "Aspose.Words لـ Java"
description: "يحدد اتجاه النص على الصفحة في خلية جدول أو إطار نص في Java."
type: docs
weight: 675
url: /ar/java/com.aspose.words/textorientation/
---

**Inheritance:**
java.lang.Object
```
public class TextOrientation
```

يحدد اتجاه النص على الصفحة، في خلية جدول أو إطار نص.

 **Examples:** 

يعرض كيفية إنشاء جدول 2x2 منسق.

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
## الحقول

| حقل | الوصف |
| --- | --- |
| [DOWNWARD](#DOWNWARD) | النص مُدوَّر 90 درجة إلى اليمين ليظهر من الأعلى إلى الأسفل (tb-rl). |
| [HORIZONTAL](#HORIZONTAL) | النص مُرتب أفقيًا (lr-tb). |
| [HORIZONTAL_ROTATED_FAR_EAST](#HORIZONTAL-ROTATED-FAR-EAST) | النص مُرتب أفقيًا، لكن أحرف الشرق الأقصى مُدوَّرة 90 درجة إلى اليسار (lr-tb-v). |
| [UPWARD](#UPWARD) | النص مُدوَّر 90 درجة إلى اليسار ليظهر من الأسفل إلى الأعلى (bt-lr). |
| [VERTICAL_FAR_EAST](#VERTICAL-FAR-EAST) | أحرف الشرق الأقصى تظهر عموديًا، والنص الآخر مُدوَّر 90 درجة إلى اليمين ليظهر من الأعلى إلى الأسفل (tb-rl-v). |
| [VERTICAL_ROTATED_FAR_EAST](#VERTICAL-ROTATED-FAR-EAST) | تظهر أحرف الشرق الأقصى عمودية، والنص الآخر يتم تدويره 90 درجة إلى اليمين ليظهر من أعلى إلى أسفل عموديًا، ثم من اليسار إلى اليمين أفقيًا (tb-lr-v). |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String textOrientationName)](#fromName-java.lang.String) |  |
| [getName(int textOrientation)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int textOrientation)](#toString-int) |  |
### DOWNWARD {#DOWNWARD}
```
public static int DOWNWARD
```


النص مُدوَّر 90 درجة إلى اليمين ليظهر من الأعلى إلى الأسفل (tb-rl).

### HORIZONTAL {#HORIZONTAL}
```
public static int HORIZONTAL
```


النص مُرتب أفقيًا (lr-tb).

### HORIZONTAL_ROTATED_FAR_EAST {#HORIZONTAL-ROTATED-FAR-EAST}
```
public static int HORIZONTAL_ROTATED_FAR_EAST
```


النص مُرتب أفقيًا، لكن أحرف الشرق الأقصى مُدوَّرة 90 درجة إلى اليسار (lr-tb-v).

### UPWARD {#UPWARD}
```
public static int UPWARD
```


النص مُدوَّر 90 درجة إلى اليسار ليظهر من الأسفل إلى الأعلى (bt-lr).

### VERTICAL_FAR_EAST {#VERTICAL-FAR-EAST}
```
public static int VERTICAL_FAR_EAST
```


أحرف الشرق الأقصى تظهر عموديًا، والنص الآخر مُدوَّر 90 درجة إلى اليمين ليظهر من الأعلى إلى الأسفل (tb-rl-v).

### VERTICAL_ROTATED_FAR_EAST {#VERTICAL-ROTATED-FAR-EAST}
```
public static int VERTICAL_ROTATED_FAR_EAST
```


تظهر أحرف الشرق الأقصى عمودية، والنص الآخر يتم تدويره 90 درجة إلى اليمين ليظهر من أعلى إلى أسفل عموديًا، ثم من اليسار إلى اليمين أفقيًا (tb-lr-v).

### length {#length}
```
public static int length
```


### fromName(String textOrientationName) {#fromName-java.lang.String}
```
public static int fromName(String textOrientationName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| textOrientationName | java.lang.String |  |

**Returns:**
int
### getName(int textOrientation) {#getName-int}
```
public static String getName(int textOrientation)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| textOrientation | int |  |

**Returns:**
java.lang.String
