---
title: "PageBorderAppliesTo"
linktitle: "PageBorderAppliesTo"
second_title: "Aspose.Words لـ Java"
description: "يحدد الصفحات التي يُطبع عليها حد الصفحة في Java."
type: docs
weight: 510
url: /ar/java/com.aspose.words/pageborderappliesto/
---

**Inheritance:**
java.lang.Object
```
public class PageBorderAppliesTo
```

يحدد الصفحات التي يُطبع عليها حد الصفحة.

 **Examples:** 

يوضح كيفية إنشاء حد على شكل شريط أزرق عريض في أعلى الصفحة الأولى.

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
## الحقول

| حقل | الوصف |
| --- | --- |
| [ALL_PAGES](#ALL-PAGES) | يظهر حد الصفحة على جميع صفحات القسم. |
| [FIRST_PAGE](#FIRST-PAGE) | يظهر حد الصفحة فقط على الصفحة الأولى من القسم. |
| [OTHER_PAGES](#OTHER-PAGES) | يظهر حد الصفحة على جميع الصفحات باستثناء الصفحة الأولى من القسم. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String pageBorderAppliesToName)](#fromName-java.lang.String) |  |
| [getName(int pageBorderAppliesTo)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pageBorderAppliesTo)](#toString-int) |  |
### ALL_PAGES {#ALL-PAGES}
```
public static int ALL_PAGES
```


يظهر حد الصفحة على جميع صفحات القسم.

### FIRST_PAGE {#FIRST-PAGE}
```
public static int FIRST_PAGE
```


يظهر حد الصفحة فقط على الصفحة الأولى من القسم.

### OTHER_PAGES {#OTHER-PAGES}
```
public static int OTHER_PAGES
```


يظهر حد الصفحة على جميع الصفحات باستثناء الصفحة الأولى من القسم.

### length {#length}
```
public static int length
```


### fromName(String pageBorderAppliesToName) {#fromName-java.lang.String}
```
public static int fromName(String pageBorderAppliesToName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| pageBorderAppliesToName | java.lang.String |  |

**Returns:**
int
### getName(int pageBorderAppliesTo) {#getName-int}
```
public static String getName(int pageBorderAppliesTo)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| pageBorderAppliesTo | int |  |

**Returns:**
java.lang.String
