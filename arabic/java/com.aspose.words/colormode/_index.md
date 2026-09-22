---
title: "ColorMode"
linktitle: "ColorMode"
second_title: "Aspose.Words لـ Java"
description: "يحدد كيفية عرض الألوان في Java."
type: docs
weight: 105
url: /ar/java/com.aspose.words/colormode/
---

**Inheritance:**
java.lang.Object
```
public class ColorMode
```

يحدد كيفية عرض الألوان.

 **Examples:** 

يوضح كيفية تغيير لون الصورة باستخدام خاصية خيارات الحفظ.

```

 Document doc = new Document(getMyDir() + "Images.docx");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 // Set the "ColorMode" property to "Grayscale" to render all images from the document in black and white.
 // The size of the output document may be larger with this setting.
 // Set the "ColorMode" property to "Normal" to render all images in color.
 PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
 {
     pdfSaveOptions.setColorMode(colorMode);
 }

 doc.save(getArtifactsDir() + "PdfSaveOptions.ColorRendering.pdf", pdfSaveOptions);
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [GRAYSCALE](#GRAYSCALE) | العرض بألوان في نطاق من درجات الرمادي من الأبيض إلى الأسود. |
| [NORMAL](#NORMAL) | العرض بألوان غير معدلة. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String colorModeName)](#fromName-java.lang.String) |  |
| [getName(int colorMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int colorMode)](#toString-int) |  |
### GRAYSCALE {#GRAYSCALE}
```
public static int GRAYSCALE
```


العرض بألوان في نطاق من درجات الرمادي من الأبيض إلى الأسود.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


العرض بألوان غير معدلة.

### length {#length}
```
public static int length
```


### fromName(String colorModeName) {#fromName-java.lang.String}
```
public static int fromName(String colorModeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| colorModeName | java.lang.String |  |

**Returns:**
int
### getName(int colorMode) {#getName-int}
```
public static String getName(int colorMode)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| colorMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int colorMode) {#toString-int}
```
public static String toString(int colorMode)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| colorMode | int |  |

**Returns:**
java.lang.String
