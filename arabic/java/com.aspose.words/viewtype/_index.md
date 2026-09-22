---
title: "ViewType"
linktitle: "ViewType"
second_title: "Aspose.Words لـ Java"
description: "القيم المحتملة لوضع العرض في Microsoft Word في جافا."
type: docs
weight: 715
url: /ar/java/com.aspose.words/viewtype/
---

**Inheritance:**
java.lang.Object
```
public class ViewType
```

القيم الممكنة لوضع العرض في Microsoft Word.

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
| [NONE](#NONE) | يجب عرض المستند في طريقة العرض الافتراضية للتطبيق. |
| [NORMAL](#NORMAL) | يجب عرض المستند في طريقة عرض مُحسّنة لتقسيم الفقرات أو إنشاء مستندات طويلة. |
| [OUTLINE](#OUTLINE) | يجب عرض المستند في طريقة عرض مُحسّنة لتقسيم الفقرات أو إنشاء مستندات طويلة. |
| [PAGE_LAYOUT](#PAGE-LAYOUT) | يجب فتح المستند في طريقة عرض تُظهر المستند كما سيُطبع. |
| [READING](#READING) | يجب عرض المستند في طريقة العرض الافتراضية للتطبيق. |
| [WEB](#WEB) | يجب عرض المستند في طريقة عرض تحاكي الطريقة التي سيُعرض بها المستند في صفحة ويب. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String viewTypeName)](#fromName-java.lang.String) |  |
| [getName(int viewType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int viewType)](#toString-int) |  |
### NONE {#NONE}
```
public static int NONE
```


يجب عرض المستند في طريقة العرض الافتراضية للتطبيق.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


يجب عرض المستند في طريقة عرض مُحسّنة لتقسيم الفقرات أو إنشاء مستندات طويلة.

### OUTLINE {#OUTLINE}
```
public static int OUTLINE
```


يجب عرض المستند في طريقة عرض مُحسّنة لتقسيم الفقرات أو إنشاء مستندات طويلة.

### PAGE_LAYOUT {#PAGE-LAYOUT}
```
public static int PAGE_LAYOUT
```


يجب فتح المستند في طريقة عرض تُظهر المستند كما سيُطبع.

### READING {#READING}
```
public static int READING
```


يجب عرض المستند في طريقة العرض الافتراضية للتطبيق.

### WEB {#WEB}
```
public static int WEB
```


يجب عرض المستند في طريقة عرض تحاكي الطريقة التي سيُعرض بها المستند في صفحة ويب.

### length {#length}
```
public static int length
```


### fromName(String viewTypeName) {#fromName-java.lang.String}
```
public static int fromName(String viewTypeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| viewTypeName | java.lang.String |  |

**Returns:**
int
### getName(int viewType) {#getName-int}
```
public static String getName(int viewType)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| viewType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int viewType) {#toString-int}
```
public static String toString(int viewType)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| viewType | int |  |

**Returns:**
java.lang.String
