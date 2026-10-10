---
title: "TextOrientation"
linktitle: "TextOrientation"
second_title: "Aspose.Words Java için"
description: "Java'da bir tablo hücresi veya metin çerçevesindeki sayfadaki metnin yönünü belirtir."
type: docs
weight: 675
url: /tr/java/com.aspose.words/textorientation/
---

**Inheritance:**
java.lang.Object
```
public class TextOrientation
```

Metnin bir sayfada, tablo hücresinde veya metin çerçevesinde yönünü belirtir.

 **Examples:** 

Biçimlendirilmiş 2x2 bir tablo nasıl oluşturulur gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [DOWNWARD](#DOWNWARD) | Metin, üstten alta görünmek için 90 derece sağa döndürülür (tb-rl). |
| [HORIZONTAL](#HORIZONTAL) | Metin yatay olarak düzenlenir (lr-tb). |
| [HORIZONTAL_ROTATED_FAR_EAST](#HORIZONTAL-ROTATED-FAR-EAST) | Metin yatay olarak düzenlenir, ancak Uzak Doğu karakterleri 90 derece sola döndürülür (lr-tb-v). |
| [UPWARD](#UPWARD) | Metin, alttan üste görünmek için 90 derece sola döndürülür (bt-lr). |
| [VERTICAL_FAR_EAST](#VERTICAL-FAR-EAST) | Uzak Doğu karakterleri dikey görünür, diğer metin ise üstten alta görünmek için 90 derece sağa döndürülür (tb-rl-v). |
| [VERTICAL_ROTATED_FAR_EAST](#VERTICAL-ROTATED-FAR-EAST) | Uzak Doğu karakterleri dikey olarak görünür, diğer metin sağa 90 derece döndürülerek yukarıdan aşağıya dikey, ardından soldan sağa yatay olarak görünür (tb-lr-v). |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String textOrientationName)](#fromName-java.lang.String) |  |
| [getName(int textOrientation)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int textOrientation)](#toString-int) |  |
### DOWNWARD {#DOWNWARD}
```
public static int DOWNWARD
```


Metin, üstten alta görünmek için 90 derece sağa döndürülür (tb-rl).

### HORIZONTAL {#HORIZONTAL}
```
public static int HORIZONTAL
```


Metin yatay olarak düzenlenir (lr-tb).

### HORIZONTAL_ROTATED_FAR_EAST {#HORIZONTAL-ROTATED-FAR-EAST}
```
public static int HORIZONTAL_ROTATED_FAR_EAST
```


Metin yatay olarak düzenlenir, ancak Uzak Doğu karakterleri 90 derece sola döndürülür (lr-tb-v).

### UPWARD {#UPWARD}
```
public static int UPWARD
```


Metin, alttan üste görünmek için 90 derece sola döndürülür (bt-lr).

### VERTICAL_FAR_EAST {#VERTICAL-FAR-EAST}
```
public static int VERTICAL_FAR_EAST
```


Uzak Doğu karakterleri dikey görünür, diğer metin ise üstten alta görünmek için 90 derece sağa döndürülür (tb-rl-v).

### VERTICAL_ROTATED_FAR_EAST {#VERTICAL-ROTATED-FAR-EAST}
```
public static int VERTICAL_ROTATED_FAR_EAST
```


Uzak Doğu karakterleri dikey olarak görünür, diğer metin sağa 90 derece döndürülerek yukarıdan aşağıya dikey, ardından soldan sağa yatay olarak görünür (tb-lr-v).

### length {#length}
```
public static int length
```


### fromName(String textOrientationName) {#fromName-java.lang.String}
```
public static int fromName(String textOrientationName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| textOrientationName | java.lang.String |  |

**Returns:**
int
### getName(int textOrientation) {#getName-int}
```
public static String getName(int textOrientation)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| textOrientation | int |  |

**Returns:**
java.lang.String
