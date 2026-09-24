---
title: "BaselineAlignment"
linktitle: "BaselineAlignment"
second_title: "Aspose.Words Java için"
description: "Java'da bir satırdaki yazı tiplerinin dikey konumunu belirtir."
type: docs
weight: 36
url: /tr/java/com.aspose.words/baselinealignment/
---

**Inheritance:**
java.lang.Object
```
public class BaselineAlignment
```

Bir satırdaki yazı tiplerinin dikey konumunu belirtir.

 **Examples:** 

Bir satırdaki yazı tiplerinin dikey konumunu nasıl ayarlayacağınızı gösterir.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 ParagraphFormat format = doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat();
 if (format.getBaselineAlignment() == BaselineAlignment.AUTO)
 {
     format.setBaselineAlignment(BaselineAlignment.TOP);
 }

 doc.save(getArtifactsDir() + "ParagraphFormat.ParagraphBaselineAlignment.docx");
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [AUTO](#AUTO) | Taban çizgisi otomatik olarak ayarlanır. |
| [BASELINE](#BASELINE) | Paragrafın taban çizgisine hizalar. |
| [BOTTOM](#BOTTOM) | Her yazı tipinin alt kısmına hizalar. |
| [CENTER](#CENTER) | Her yazı tipinin merkez noktalarına hizalar. |
| [TOP](#TOP) | Her yazı tipinin üst kısmına hizalar. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String baselineAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int baselineAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int baselineAlignment)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Taban çizgisi otomatik olarak ayarlanır.

### BASELINE {#BASELINE}
```
public static int BASELINE
```


Paragrafın taban çizgisine hizalar.

### BOTTOM {#BOTTOM}
```
public static int BOTTOM
```


Her yazı tipinin alt kısmına hizalar.

### CENTER {#CENTER}
```
public static int CENTER
```


Her yazı tipinin merkez noktalarına hizalar.

### TOP {#TOP}
```
public static int TOP
```


Her yazı tipinin üst kısmına hizalar.

### length {#length}
```
public static int length
```


### fromName(String baselineAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String baselineAlignmentName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| baselineAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int baselineAlignment) {#getName-int}
```
public static String getName(int baselineAlignment)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| baselineAlignment | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int baselineAlignment) {#toString-int}
```
public static String toString(int baselineAlignment)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| baselineAlignment | int |  |

**Returns:**
java.lang.String
