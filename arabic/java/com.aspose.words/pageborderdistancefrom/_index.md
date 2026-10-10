---
title: "PageBorderDistanceFrom"
linktitle: "PageBorderDistanceFrom"
second_title: "Aspose.Words لـ Java"
description: "يحدد موضع حد الصفحة بالنسبة لهامش الصفحة في Java."
type: docs
weight: 511
url: /ar/java/com.aspose.words/pageborderdistancefrom/
---

**Inheritance:**
java.lang.Object
```
public class PageBorderDistanceFrom
```

يحدد موضع حد الصفحة بالنسبة لهامش الصفحة.

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
| [PAGE_EDGE](#PAGE-EDGE) | يتم قياس موضع الحد من حافة الصفحة. |
| [TEXT](#TEXT) | يتم قياس موضع الحد من هامش الصفحة. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String pageBorderDistanceFromName)](#fromName-java.lang.String) |  |
| [getName(int pageBorderDistanceFrom)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pageBorderDistanceFrom)](#toString-int) |  |
### PAGE_EDGE {#PAGE-EDGE}
```
public static int PAGE_EDGE
```


يتم قياس موضع الحد من حافة الصفحة.

### TEXT {#TEXT}
```
public static int TEXT
```


يتم قياس موضع الحد من هامش الصفحة.

### length {#length}
```
public static int length
```


### fromName(String pageBorderDistanceFromName) {#fromName-java.lang.String}
```
public static int fromName(String pageBorderDistanceFromName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| pageBorderDistanceFromName | java.lang.String |  |

**Returns:**
int
### getName(int pageBorderDistanceFrom) {#getName-int}
```
public static String getName(int pageBorderDistanceFrom)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| pageBorderDistanceFrom | int |  |

**Returns:**
java.lang.String
