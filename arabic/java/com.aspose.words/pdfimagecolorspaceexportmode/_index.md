---
title: "PdfImageColorSpaceExportMode"
linktitle: "PdfImageColorSpaceExportMode"
second_title: "Aspose.Words لـ Java"
description: "يحدد كيفية اختيار مساحة اللون للصور في مستند PDF في Java."
type: docs
weight: 536
url: /ar/java/com.aspose.words/pdfimagecolorspaceexportmode/
---

**Inheritance:**
java.lang.Object
```
public class PdfImageColorSpaceExportMode
```

يحدد كيفية اختيار مساحة اللون للصور في مستند PDF.

 **Examples:** 

يوضح كيفية تعيين مساحة لون مختلفة للصور في مستند عند تصديره إلى PDF.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Jpeg image:");
 builder.insertImage(getImageDir() + "Logo.jpg");
 builder.insertParagraph();
 builder.writeln("Png image:");
 builder.insertImage(getImageDir() + "Transparent background logo.png");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();

 // Set the "ImageColorSpaceExportMode" property to "PdfImageColorSpaceExportMode.Auto" to get Aspose.Words to
 // automatically select the color space for images in the document that it converts to PDF.
 // In most cases, the color space will be RGB.
 // Set the "ImageColorSpaceExportMode" property to "PdfImageColorSpaceExportMode.SimpleCmyk"
 // to use the CMYK color space for all images in the saved PDF.
 // Aspose.Words will also apply Flate compression to all images and ignore the "ImageCompression" property's value.
 pdfSaveOptions.setImageColorSpaceExportMode(pdfImageColorSpaceExportMode);

 doc.save(getArtifactsDir() + "PdfSaveOptions.ImageColorSpaceExportMode.pdf", pdfSaveOptions);
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [AUTO](#AUTO) | Aspose.Words يختار تلقائيًا أنسب مساحة لون لكل صورة. |
| [SIMPLE_CMYK](#SIMPLE-CMYK) | Aspose.Words يحول صور RGB إلى مساحة لون CMYK باستخدام صيغة بسيطة. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String pdfImageColorSpaceExportModeName)](#fromName-java.lang.String) |  |
| [getName(int pdfImageColorSpaceExportMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfImageColorSpaceExportMode)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Aspose.Words يختار تلقائيًا أنسب مساحة لون لكل صورة.

 **Remarks:** 

معظم الصور تُحفظ في مساحة لون RGB. كما قد تُستخدم مساحات اللون Indexed و Grayscale. لا تُستخدم مساحة لون CMYK أبدًا.

قد تكون مساحة اللون لبعض الصور مختلفة على منصات مختلفة.

### SIMPLE_CMYK {#SIMPLE-CMYK}
```
public static int SIMPLE_CMYK
```


Aspose.Words يحول صور RGB إلى مساحة لون CMYK باستخدام صيغة بسيطة.

 **Remarks:** 

يتم تحويل الصور في مساحة لون RGB إلى CMYK باستخدام الصيغة: Black = minimum(1-Red,1-Green,1-Blue). Cyan = (1-Red-Black)/(1-Black). Magenta = (1-Green-Black)/(1-Black). Yellow = (1-Blue-Black)/(1-Black). قيم RGB مُعَدَّلة - فهي بين 0 و 1.0.

### length {#length}
```
public static int length
```


### fromName(String pdfImageColorSpaceExportModeName) {#fromName-java.lang.String}
```
public static int fromName(String pdfImageColorSpaceExportModeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| pdfImageColorSpaceExportModeName | java.lang.String |  |

**Returns:**
int
### getName(int pdfImageColorSpaceExportMode) {#getName-int}
```
public static String getName(int pdfImageColorSpaceExportMode)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| pdfImageColorSpaceExportMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int pdfImageColorSpaceExportMode) {#toString-int}
```
public static String toString(int pdfImageColorSpaceExportMode)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| pdfImageColorSpaceExportMode | int |  |

**Returns:**
java.lang.String
