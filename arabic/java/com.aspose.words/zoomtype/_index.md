---
title: "ZoomType"
linktitle: "ZoomType"
second_title: "Aspose.Words لـ Java"
description: "القيم الممكنة لكيفية ظهور المستند كبيرًا أو صغيرًا على الشاشة في Microsoft Word في Java."
type: docs
weight: 751
url: /ar/java/com.aspose.words/zoomtype/
---

**Inheritance:**
java.lang.Object
```
public class ZoomType
```

القيم المحتملة لكيفية ظهور المستند كبيرًا أو صغيرًا على الشاشة في Microsoft Word.

 **Examples:** 

يظهر كيفية تعيين عامل تكبير مخصص، والذي ستطبقه الإصدارات القديمة من Microsoft Word على المستند عند التحميل.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 doc.getViewOptions().setViewType(ViewType.PAGE_LAYOUT);
 doc.getViewOptions().setZoomPercent(50);

 Assert.assertEquals(ZoomType.CUSTOM, doc.getViewOptions().getZoomType());
 Assert.assertEquals(ZoomType.NONE, doc.getViewOptions().getZoomType());

 doc.save(getArtifactsDir() + "ViewOptions.SetZoomPercentage.doc");
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [CUSTOM](#CUSTOM) | نسبة التكبير يتم تعيينها صراحةً. |
| [FULL_PAGE](#FULL-PAGE) | نسبة التكبير يتم إعادة حسابها تلقائيًا لتلائم صفحة كاملة واحدة. |
| [NONE](#NONE) | يشير إلى استخدام نسبة التكبير الصريحة. |
| [PAGE_WIDTH](#PAGE-WIDTH) | نسبة التكبير يتم إعادة حسابها تلقائيًا لتلائم عرض الصفحة. |
| [TEXT_FIT](#TEXT-FIT) | نسبة التكبير يتم إعادة حسابها تلقائيًا لتلائم النص. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String zoomTypeName)](#fromName-java.lang.String) |  |
| [getName(int zoomType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int zoomType)](#toString-int) |  |
### CUSTOM {#CUSTOM}
```
public static int CUSTOM
```


نسبة التكبير يتم تعيينها صراحةً. لا يتم إعادة حسابها تلقائيًا عندما يتغير حجم التحكم.

### FULL_PAGE {#FULL-PAGE}
```
public static int FULL_PAGE
```


نسبة التكبير يتم إعادة حسابها تلقائيًا لتلائم صفحة كاملة واحدة.

### NONE {#NONE}
```
public static int NONE
```


يشير إلى استخدام نسبة التكبير الصريحة. نفس ما هو في [CUSTOM](../../com.aspose.words/zoomtype/\#CUSTOM).

### PAGE_WIDTH {#PAGE-WIDTH}
```
public static int PAGE_WIDTH
```


نسبة التكبير يتم إعادة حسابها تلقائيًا لتلائم عرض الصفحة.

### TEXT_FIT {#TEXT-FIT}
```
public static int TEXT_FIT
```


نسبة التكبير يتم إعادة حسابها تلقائيًا لتلائم النص.

### length {#length}
```
public static int length
```


### fromName(String zoomTypeName) {#fromName-java.lang.String}
```
public static int fromName(String zoomTypeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| zoomTypeName | java.lang.String |  |

**Returns:**
int
### getName(int zoomType) {#getName-int}
```
public static String getName(int zoomType)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| zoomType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int zoomType) {#toString-int}
```
public static String toString(int zoomType)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| zoomType | int |  |

**Returns:**
java.lang.String
