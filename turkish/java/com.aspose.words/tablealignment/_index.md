---
title: "TableAlignment"
linktitle: "TableAlignment"
second_title: "Aspose.Words Java için"
description: "Java'da satır içi bir tablo için hizalamayı belirtir."
type: docs
weight: 657
url: /tr/java/com.aspose.words/tablealignment/
---

**Inheritance:**
java.lang.Object
```
public class TableAlignment
```

Satır içi bir tablo için hizalamayı belirtir.

 **Examples:** 

Bir tabloya dış kenarlık nasıl uygulanacağını gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [CENTER](#CENTER) | Tablo ortalanmıştır. |
| [LEFT](#LEFT) | Tablo sola hizalanmıştır. |
| [RIGHT](#RIGHT) | Tablo sağa hizalanmıştır. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String tableAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int tableAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int tableAlignment)](#toString-int) |  |
### CENTER {#CENTER}
```
public static int CENTER
```


Tablo ortalanmıştır.

### LEFT {#LEFT}
```
public static int LEFT
```


Tablo sola hizalanmıştır.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Tablo sağa hizalanmıştır.

### length {#length}
```
public static int length
```


### fromName(String tableAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String tableAlignmentName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| tableAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int tableAlignment) {#getName-int}
```
public static String getName(int tableAlignment)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| tableAlignment | int |  |

**Returns:**
java.lang.String
