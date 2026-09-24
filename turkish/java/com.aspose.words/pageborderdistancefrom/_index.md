---
title: "PageBorderDistanceFrom"
linktitle: "PageBorderDistanceFrom"
second_title: "Aspose.Words Java için"
description: "Java'da sayfa kenarlığının sayfa kenar boşluğuna göre konumlandırılmasını belirtir."
type: docs
weight: 511
url: /tr/java/com.aspose.words/pageborderdistancefrom/
---

**Inheritance:**
java.lang.Object
```
public class PageBorderDistanceFrom
```

Sayfa kenarlığının sayfa kenar boşluğuna göre konumlandırılmasını belirtir.

 **Examples:** 

İlk sayfanın üst kısmında geniş mavi bir şerit kenarlık nasıl oluşturulacağını gösterir.

```

 Document doc = new Document();

 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setBorderAlwaysInFront(false);
 pageSetup.setBorderDistanceFrom(PageBorderDistanceFrom.PAGE_EDGE);
 pageSetup.setBorderAppliesTo(PageBorderAppliesTo.FIRST_PAGE);

 Border border = pageSetup.getBorders().getByBorderType(BorderType.TOP);
 border.setLineStyle(LineStyle.SINGLE);
 border.setLineWidth(30.0);
 border.setColor(Color.BLUE);
 border.setDistanceFromText(0.0);

 doc.save(getArtifactsDir() + "PageSetup.PageBorderProperties.docx");
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [PAGE_EDGE](#PAGE-EDGE) | Kenarlık konumu sayfa kenarından ölçülür. |
| [TEXT](#TEXT) | Kenarlık konumu sayfa kenar boşluğundan ölçülür. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String pageBorderDistanceFromName)](#fromName-java.lang.String) |  |
| [getName(int pageBorderDistanceFrom)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pageBorderDistanceFrom)](#toString-int) |  |
### PAGE_EDGE {#PAGE-EDGE}
```
public static int PAGE_EDGE
```


Kenarlık konumu sayfa kenarından ölçülür.

### TEXT {#TEXT}
```
public static int TEXT
```


Kenarlık konumu sayfa kenar boşluğundan ölçülür.

### length {#length}
```
public static int length
```


### fromName(String pageBorderDistanceFromName) {#fromName-java.lang.String}
```
public static int fromName(String pageBorderDistanceFromName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| pageBorderDistanceFromName | java.lang.String |  |

**Returns:**
int
### getName(int pageBorderDistanceFrom) {#getName-int}
```
public static String getName(int pageBorderDistanceFrom)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| pageBorderDistanceFrom | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int pageBorderDistanceFrom) {#toString-int}
```
public static String toString(int pageBorderDistanceFrom)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| pageBorderDistanceFrom | int |  |

**Returns:**
java.lang.String
