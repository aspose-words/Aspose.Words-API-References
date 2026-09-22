---
title: "WrapType"
linktitle: "WrapType"
second_title: "Aspose.Words لـ Java"
description: "يحدد كيفية التفاف النص حول شكل أو صورة في Java."
type: docs
weight: 737
url: /ar/java/com.aspose.words/wraptype/
---

**Inheritance:**
java.lang.Object
```
public class WrapType
```

يحدد كيفية التفاف النص حول الشكل أو الصورة.

 **Examples:** 

يوضح كيفية إدراج صورة واستخدامها كعلامة مائية.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert the image into the header so that it will be visible on every page.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 Shape shape = builder.insertImage(getImageDir() + "Transparent background logo.png");
 shape.setWrapType(WrapType.NONE);
 shape.setBehindText(true);

 // Place the image at the center of the page.
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setLeft((builder.getPageSetup().getPageWidth() - shape.getWidth()) / 2.0);
 shape.setTop((builder.getPageSetup().getPageHeight() - shape.getHeight()) / 2.0);

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertWatermark.docx");
 
```

يوضح كيفية إدراج صورة عائمة في مركز الصفحة.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a floating image that will appear behind the overlapping text and align it to the page's center.
 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");
 shape.setWrapType(WrapType.NONE);
 shape.setBehindText(true);
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setHorizontalAlignment(HorizontalAlignment.CENTER);
 shape.setVerticalAlignment(VerticalAlignment.CENTER);

 doc.save(getArtifactsDir() + "Image.CreateFloatingPageCenter.docx");
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [INLINE](#INLINE) | يبقى الشكل على نفس طبقة النص ويُعامل كحرف. |
| [NONE](#NONE) | لا يوجد التفاف للنص حول الشكل. |
| [SQUARE](#SQUARE) | يفلف النص حول جميع جوانب الصندوق المربع المحيط بالشكل. |
| [THROUGH](#THROUGH) | نفس طريقة Tight، ولكن يلف داخل أي أجزاء من الشكل المفتوحة. |
| [TIGHT](#TIGHT) | يفلف بإحكام حول حواف الشكل، بدلاً من الالتفاف حول الصندوق المحيط. |
| [TOP_BOTTOM](#TOP-BOTTOM) | يتوقف النص عند أعلى الشكل ويستأنف على السطر أسفل الشكل. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String wrapTypeName)](#fromName-java.lang.String) |  |
| [getName(int wrapType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int wrapType)](#toString-int) |  |
### INLINE {#INLINE}
```
public static int INLINE
```


يبقى الشكل على نفس طبقة النص ويُعامل كحرف.

### NONE {#NONE}
```
public static int NONE
```


لا يوجد التفاف للنص حول الشكل. يتم وضع الشكل خلف النص أو أمامه.

### SQUARE {#SQUARE}
```
public static int SQUARE
```


يفلف النص حول جميع جوانب الصندوق المربع المحيط بالشكل.

### THROUGH {#THROUGH}
```
public static int THROUGH
```


نفس طريقة Tight، ولكن يلف داخل أي أجزاء من الشكل المفتوحة.

### TIGHT {#TIGHT}
```
public static int TIGHT
```


يفلف بإحكام حول حواف الشكل، بدلاً من الالتفاف حول الصندوق المحيط.

### TOP_BOTTOM {#TOP-BOTTOM}
```
public static int TOP_BOTTOM
```


يتوقف النص عند أعلى الشكل ويستأنف على السطر أسفل الشكل.

### length {#length}
```
public static int length
```


### fromName(String wrapTypeName) {#fromName-java.lang.String}
```
public static int fromName(String wrapTypeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| wrapTypeName | java.lang.String |  |

**Returns:**
int
### getName(int wrapType) {#getName-int}
```
public static String getName(int wrapType)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| wrapType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int wrapType) {#toString-int}
```
public static String toString(int wrapType)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| wrapType | int |  |

**Returns:**
java.lang.String
