---
title: "PageBorderAppliesTo"
linktitle: "PageBorderAppliesTo"
second_title: "Aspose.Words Java için"
description: "Java'da sayfa kenarlığının hangi sayfalarda basılacağını belirtir."
type: docs
weight: 510
url: /tr/java/com.aspose.words/pageborderappliesto/
---

**Inheritance:**
java.lang.Object
```
public class PageBorderAppliesTo
```

Sayfa kenarlığının hangi sayfalarda basılacağını belirtir.

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
| [ALL_PAGES](#ALL-PAGES) | Sayfa kenarlığı bölümün tüm sayfalarında gösterilir. |
| [FIRST_PAGE](#FIRST-PAGE) | Sayfa kenarlığı yalnızca bölümün ilk sayfasında gösterilir. |
| [OTHER_PAGES](#OTHER-PAGES) | Sayfa kenarlığı bölümün ilk sayfası dışındaki tüm sayfalarda gösterilir. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String pageBorderAppliesToName)](#fromName-java.lang.String) |  |
| [getName(int pageBorderAppliesTo)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pageBorderAppliesTo)](#toString-int) |  |
### ALL_PAGES {#ALL-PAGES}
```
public static int ALL_PAGES
```


Sayfa kenarlığı bölümün tüm sayfalarında gösterilir.

### FIRST_PAGE {#FIRST-PAGE}
```
public static int FIRST_PAGE
```


Sayfa kenarlığı yalnızca bölümün ilk sayfasında gösterilir.

### OTHER_PAGES {#OTHER-PAGES}
```
public static int OTHER_PAGES
```


Sayfa kenarlığı bölümün ilk sayfası dışındaki tüm sayfalarda gösterilir.

### length {#length}
```
public static int length
```


### fromName(String pageBorderAppliesToName) {#fromName-java.lang.String}
```
public static int fromName(String pageBorderAppliesToName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| pageBorderAppliesToName | java.lang.String |  |

**Returns:**
int
### getName(int pageBorderAppliesTo) {#getName-int}
```
public static String getName(int pageBorderAppliesTo)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| pageBorderAppliesTo | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int pageBorderAppliesTo) {#toString-int}
```
public static String toString(int pageBorderAppliesTo)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| pageBorderAppliesTo | int |  |

**Returns:**
java.lang.String
