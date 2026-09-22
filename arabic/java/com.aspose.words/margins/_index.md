---
title: "الهوامش"
linktitle: "الهوامش"
second_title: "Aspose.Words لـ Java"
description: "يحدد الهوامش المسبقة في جافا."
type: docs
weight: 449
url: /ar/java/com.aspose.words/margins/
---

**Inheritance:**
java.lang.Object
```
public class Margins
```

يحدد الهوامش المحددة مسبقًا.

 **Examples:** 

يظهر متى يتم إعادة حساب تخطيط الصفحة للمستند.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 // Saving a document to PDF, to an image, or printing for the first time will automatically
 // cache the layout of the document within its pages.
 doc.save(getArtifactsDir() + "Document.UpdatePageLayout.1.pdf");

 // Modify the document in some way.
 doc.getStyles().get("Normal").getFont().setSize(6.0);
 doc.getSections().get(0).getPageSetup().setOrientation(Orientation.LANDSCAPE);
 doc.getSections().get(0).getPageSetup().setMargins(Margins.MIRRORED);

 // In the current version of Aspose.Words, modifying the document does not automatically rebuild
 // the cached page layout. If we wish for the cached layout
 // to stay up to date, we will need to update it manually.
 doc.updatePageLayout();

 doc.save(getArtifactsDir() + "Document.UpdatePageLayout.2.pdf");
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [CUSTOM](#CUSTOM) | هوامش مخصصة. |
| [MIRRORED](#MIRRORED) | هوامش معكوسة. |
| [MODERATE](#MODERATE) | هوامش معتدلة. |
| [NARROW](#NARROW) | هوامش ضيقة. |
| [NORMAL](#NORMAL) | هوامش عادية. |
| [WIDE](#WIDE) | هوامش واسعة. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String marginsName)](#fromName-java.lang.String) |  |
| [getName(int margins)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int margins)](#toString-int) |  |
### CUSTOM {#CUSTOM}
```
public static int CUSTOM
```


هوامش مخصصة.

### MIRRORED {#MIRRORED}
```
public static int MIRRORED
```


هوامش معكوسة.

 **Remarks:** 

ضبط الهوامش إلى معكوس سيحدد القيمة المناسبة لخاصية [PageSetup.getMultiplePages()](../../com.aspose.words/pagesetup/\#getMultiplePages) / [PageSetup.setMultiplePages(int)](../../com.aspose.words/pagesetup/\#setMultiplePages-int). سيؤثر ذلك على المستند بأكمله، وليس فقط على القسم الحالي.

### MODERATE {#MODERATE}
```
public static int MODERATE
```


هوامش معتدلة.

### NARROW {#NARROW}
```
public static int NARROW
```


هوامش ضيقة.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


هوامش عادية.

### WIDE {#WIDE}
```
public static int WIDE
```


هوامش واسعة.

### length {#length}
```
public static int length
```


### fromName(String marginsName) {#fromName-java.lang.String}
```
public static int fromName(String marginsName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| marginsName | java.lang.String |  |

**Returns:**
int
### getName(int margins) {#getName-int}
```
public static String getName(int margins)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| margins | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int margins) {#toString-int}
```
public static String toString(int margins)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| margins | int |  |

**Returns:**
java.lang.String
