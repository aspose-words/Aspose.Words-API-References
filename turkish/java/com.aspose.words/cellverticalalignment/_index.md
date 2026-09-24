---
title: "CellVerticalAlignment"
linktitle: "CellVerticalAlignment"
second_title: "Aspose.Words Java için"
description: "Java'da bir tablo hücresindeki metnin dikey hizalamasını belirtir."
type: docs
weight: 63
url: /tr/java/com.aspose.words/cellverticalalignment/
---

**Inheritance:**
java.lang.Object
```
public class CellVerticalAlignment
```

Bir tablo hücresi içindeki metnin dikey hizalamasını belirtir.

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
| [BOTTOM](#BOTTOM) | Metin hücrenin alt kısmına hizalanmıştır. |
| [CENTER](#CENTER) | Metin bir hücrenin ortasına hizalanmıştır. |
| [TOP](#TOP) | Metin bir hücrenin üst kısmına hizalanmıştır. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String cellVerticalAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int cellVerticalAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int cellVerticalAlignment)](#toString-int) |  |
### BOTTOM {#BOTTOM}
```
public static int BOTTOM
```


Metin hücrenin alt kısmına hizalanmıştır.

### CENTER {#CENTER}
```
public static int CENTER
```


Metin bir hücrenin ortasına hizalanmıştır.

### TOP {#TOP}
```
public static int TOP
```


Metin bir hücrenin üst kısmına hizalanmıştır.

### length {#length}
```
public static int length
```


### fromName(String cellVerticalAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String cellVerticalAlignmentName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| cellVerticalAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int cellVerticalAlignment) {#getName-int}
```
public static String getName(int cellVerticalAlignment)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| cellVerticalAlignment | int |  |

**Returns:**
java.lang.String
