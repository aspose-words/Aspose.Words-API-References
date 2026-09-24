---
title: "PreferredWidthType"
linktitle: "PreferredWidthType"
second_title: "Aspose.Words Java için"
description: "Java'da bir tablo veya hücrenin tercih edilen genişliği için ölçü birimini belirtir."
type: docs
weight: 551
url: /tr/java/com.aspose.words/preferredwidthtype/
---

**Inheritance:**
java.lang.Object
```
public class PreferredWidthType
```

Bir tablo veya hücrenin tercih edilen genişliği için ölçü birimini belirtir.

 **Examples:** 

Bir tablo hücresinin tercih edilen genişlik türünü ve değerini nasıl doğrulayacağınızı gösterir.

```

 Document doc = new Document(getMyDir() + "Tables.docx");

 Table table = doc.getFirstSection().getBody().getTables().get(0);
 Cell firstCell = table.getFirstRow().getFirstCell();

 Assert.assertEquals(PreferredWidthType.PERCENT, firstCell.getCellFormat().getPreferredWidth().getType());
 Assert.assertEquals(11.16d, firstCell.getCellFormat().getPreferredWidth().getValue());
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [AUTO](#AUTO) | Tercih edilen genişlik belirtilmemiştir. |
| [PERCENT](#PERCENT) | Belirtilen bir yüzde kullanarak mevcut öğenin genişliğini ölçün. |
| [POINTS](#POINTS) | Belirtilen bir puan sayısını (1/72 inç) kullanarak mevcut öğenin genişliğini ölçün. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String preferredWidthTypeName)](#fromName-java.lang.String) |  |
| [getName(int preferredWidthType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int preferredWidthType)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Tercih edilen genişlik belirtilmemiştir. Tablo veya hücrenin gerçek genişliği, açıkça belirtilen genişlik kullanılararak belirtilir ya da tablo görüntülendiğinde tablo otomatik sığdırma ayarına bağlı olarak tablo yerleşim algoritması tarafından otomatik olarak belirlenir.

### PERCENT {#PERCENT}
```
public static int PERCENT
```


Belirtilen bir yüzde kullanarak mevcut öğenin genişliğini ölçün.

### POINTS {#POINTS}
```
public static int POINTS
```


Belirtilen bir puan sayısını (1/72 inç) kullanarak mevcut öğenin genişliğini ölçün.

### length {#length}
```
public static int length
```


### fromName(String preferredWidthTypeName) {#fromName-java.lang.String}
```
public static int fromName(String preferredWidthTypeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| preferredWidthTypeName | java.lang.String |  |

**Returns:**
int
### getName(int preferredWidthType) {#getName-int}
```
public static String getName(int preferredWidthType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| preferredWidthType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int preferredWidthType) {#toString-int}
```
public static String toString(int preferredWidthType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| preferredWidthType | int |  |

**Returns:**
java.lang.String
