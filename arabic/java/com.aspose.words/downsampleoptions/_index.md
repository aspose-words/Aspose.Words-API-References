---
title: "DownsampleOptions"
linktitle: "DownsampleOptions"
second_title: "Aspose.Words لـ Java"
description: "يسمح بتحديد خيارات تقليل العينات في Java."
type: docs
weight: 176
url: /ar/java/com.aspose.words/downsampleoptions/
---

**Inheritance:**
java.lang.Object
```
public class DownsampleOptions
```

يسمح بتحديد خيارات تقليل العينة.

للتعرف على المزيد، زر [ Save a Document ][Save a Document] مقالة الوثائق.

 **Examples:** 

يوضح كيفية تغيير دقة الصور في مستند PDF.

```

 Document doc = new Document(getMyDir() + "Images.docx");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // By default, Aspose.Words downsample all images in a document that we save to PDF to 220 ppi.
 Assert.assertTrue(options.getDownsampleOptions().getDownsampleImages());
 Assert.assertEquals(220, options.getDownsampleOptions().getResolution());
 Assert.assertEquals(0, options.getDownsampleOptions().getResolutionThreshold());

 doc.save(getArtifactsDir() + "PdfSaveOptions.DownsampleOptions.Default.pdf", options);

 // Set the "Resolution" property to "36" to downsample all images to 36 ppi.
 options.getDownsampleOptions().setResolution(36);

 // Set the "ResolutionThreshold" property to only apply the downsampling to
 // images with a resolution that is above 128 ppi.
 options.getDownsampleOptions().setResolutionThreshold(128);

 // Only the first two images from the document will be downsampled at this stage.
 doc.save(getArtifactsDir() + "PdfSaveOptions.DownsampleOptions.LowerResolution.pdf", options);
 
```


[Save a Document]: https://docs.aspose.com/words/java/save-a-document/
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getDownsampleImages()](#getDownsampleImages) | يحدد ما إذا كان يجب تقليل عينات الصور. |
| [getResolution()](#getResolution) | يحدد الدقة بوحدة البكسل لكل بوصة التي يجب تقليل عينات الصور إليها. |
| [getResolutionThreshold()](#getResolutionThreshold) | يحدد حد الدقة بوحدة البكسل لكل بوصة. |
| [setDownsampleImages(boolean value)](#setDownsampleImages-boolean) | يحدد ما إذا كان يجب تقليل عينات الصور. |
| [setResolution(int value)](#setResolution-int) | يحدد الدقة بوحدة البكسل لكل بوصة التي يجب تقليل عينات الصور إليها. |
| [setResolutionThreshold(int value)](#setResolutionThreshold-int) | يحدد حد الدقة بوحدة البكسل لكل بوصة. |
### getDownsampleImages() {#getDownsampleImages}
```
public boolean getDownsampleImages()
```


يحدد ما إذا كان يجب تقليل عينات الصور.

 **Remarks:** 

القيمة الافتراضية هي  true .

 **Examples:** 

يوضح كيفية تغيير دقة الصور في مستند PDF.

```

 Document doc = new Document(getMyDir() + "Images.docx");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // By default, Aspose.Words downsample all images in a document that we save to PDF to 220 ppi.
 Assert.assertTrue(options.getDownsampleOptions().getDownsampleImages());
 Assert.assertEquals(220, options.getDownsampleOptions().getResolution());
 Assert.assertEquals(0, options.getDownsampleOptions().getResolutionThreshold());

 doc.save(getArtifactsDir() + "PdfSaveOptions.DownsampleOptions.Default.pdf", options);

 // Set the "Resolution" property to "36" to downsample all images to 36 ppi.
 options.getDownsampleOptions().setResolution(36);

 // Set the "ResolutionThreshold" property to only apply the downsampling to
 // images with a resolution that is above 128 ppi.
 options.getDownsampleOptions().setResolutionThreshold(128);

 // Only the first two images from the document will be downsampled at this stage.
 doc.save(getArtifactsDir() + "PdfSaveOptions.DownsampleOptions.LowerResolution.pdf", options);
 
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
### getResolution() {#getResolution}
```
public int getResolution()
```


يحدد الدقة بوحدة البكسل لكل بوصة التي يجب تقليل عينات الصور إليها.

 **Remarks:** 

القيمة الافتراضية هي 220 ppi.

 **Examples:** 

يوضح كيفية تغيير دقة الصور في مستند PDF.

```

 Document doc = new Document(getMyDir() + "Images.docx");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // By default, Aspose.Words downsample all images in a document that we save to PDF to 220 ppi.
 Assert.assertTrue(options.getDownsampleOptions().getDownsampleImages());
 Assert.assertEquals(220, options.getDownsampleOptions().getResolution());
 Assert.assertEquals(0, options.getDownsampleOptions().getResolutionThreshold());

 doc.save(getArtifactsDir() + "PdfSaveOptions.DownsampleOptions.Default.pdf", options);

 // Set the "Resolution" property to "36" to downsample all images to 36 ppi.
 options.getDownsampleOptions().setResolution(36);

 // Set the "ResolutionThreshold" property to only apply the downsampling to
 // images with a resolution that is above 128 ppi.
 options.getDownsampleOptions().setResolutionThreshold(128);

 // Only the first two images from the document will be downsampled at this stage.
 doc.save(getArtifactsDir() + "PdfSaveOptions.DownsampleOptions.LowerResolution.pdf", options);
 
```

**Returns:**
int - القيمة المقابلة  int .
### getResolutionThreshold() {#getResolutionThreshold}
```
public int getResolutionThreshold()
```


يحدد حد الدقة بوحدة البكسل لكل بوصة. إذا كانت دقة صورة في المستند أقل من قيمة الحد، فلن يتم تطبيق خوارزمية تقليل العينات. قيمة 0 تعني عدم استخدام فحص الحد ويتم تقليل جميع الصور القابلة لتقليل الحجم.

 **Remarks:** 

القيمة الافتراضية هي 0.

 **Examples:** 

يوضح كيفية تغيير دقة الصور في مستند PDF.

```

 Document doc = new Document(getMyDir() + "Images.docx");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // By default, Aspose.Words downsample all images in a document that we save to PDF to 220 ppi.
 Assert.assertTrue(options.getDownsampleOptions().getDownsampleImages());
 Assert.assertEquals(220, options.getDownsampleOptions().getResolution());
 Assert.assertEquals(0, options.getDownsampleOptions().getResolutionThreshold());

 doc.save(getArtifactsDir() + "PdfSaveOptions.DownsampleOptions.Default.pdf", options);

 // Set the "Resolution" property to "36" to downsample all images to 36 ppi.
 options.getDownsampleOptions().setResolution(36);

 // Set the "ResolutionThreshold" property to only apply the downsampling to
 // images with a resolution that is above 128 ppi.
 options.getDownsampleOptions().setResolutionThreshold(128);

 // Only the first two images from the document will be downsampled at this stage.
 doc.save(getArtifactsDir() + "PdfSaveOptions.DownsampleOptions.LowerResolution.pdf", options);
 
```

**Returns:**
int - القيمة المقابلة  int .
### setDownsampleImages(boolean value) {#setDownsampleImages-boolean}
```
public void setDownsampleImages(boolean value)
```


يحدد ما إذا كان يجب تقليل عينات الصور.

 **Remarks:** 

القيمة الافتراضية هي  true .

 **Examples:** 

يوضح كيفية تغيير دقة الصور في مستند PDF.

```

 Document doc = new Document(getMyDir() + "Images.docx");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // By default, Aspose.Words downsample all images in a document that we save to PDF to 220 ppi.
 Assert.assertTrue(options.getDownsampleOptions().getDownsampleImages());
 Assert.assertEquals(220, options.getDownsampleOptions().getResolution());
 Assert.assertEquals(0, options.getDownsampleOptions().getResolutionThreshold());

 doc.save(getArtifactsDir() + "PdfSaveOptions.DownsampleOptions.Default.pdf", options);

 // Set the "Resolution" property to "36" to downsample all images to 36 ppi.
 options.getDownsampleOptions().setResolution(36);

 // Set the "ResolutionThreshold" property to only apply the downsampling to
 // images with a resolution that is above 128 ppi.
 options.getDownsampleOptions().setResolutionThreshold(128);

 // Only the first two images from the document will be downsampled at this stage.
 doc.save(getArtifactsDir() + "PdfSaveOptions.DownsampleOptions.LowerResolution.pdf", options);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setResolution(int value) {#setResolution-int}
```
public void setResolution(int value)
```


يحدد الدقة بوحدة البكسل لكل بوصة التي يجب تقليل عينات الصور إليها.

 **Remarks:** 

القيمة الافتراضية هي 220 ppi.

 **Examples:** 

يوضح كيفية تغيير دقة الصور في مستند PDF.

```

 Document doc = new Document(getMyDir() + "Images.docx");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // By default, Aspose.Words downsample all images in a document that we save to PDF to 220 ppi.
 Assert.assertTrue(options.getDownsampleOptions().getDownsampleImages());
 Assert.assertEquals(220, options.getDownsampleOptions().getResolution());
 Assert.assertEquals(0, options.getDownsampleOptions().getResolutionThreshold());

 doc.save(getArtifactsDir() + "PdfSaveOptions.DownsampleOptions.Default.pdf", options);

 // Set the "Resolution" property to "36" to downsample all images to 36 ppi.
 options.getDownsampleOptions().setResolution(36);

 // Set the "ResolutionThreshold" property to only apply the downsampling to
 // images with a resolution that is above 128 ppi.
 options.getDownsampleOptions().setResolutionThreshold(128);

 // Only the first two images from the document will be downsampled at this stage.
 doc.save(getArtifactsDir() + "PdfSaveOptions.DownsampleOptions.LowerResolution.pdf", options);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | int | القيمة  int  المقابلة. |

### setResolutionThreshold(int value) {#setResolutionThreshold-int}
```
public void setResolutionThreshold(int value)
```


يحدد حد الدقة بوحدة البكسل لكل بوصة. إذا كانت دقة صورة في المستند أقل من قيمة الحد، فلن يتم تطبيق خوارزمية تقليل العينات. قيمة 0 تعني عدم استخدام فحص الحد ويتم تقليل جميع الصور القابلة لتقليل الحجم.

 **Remarks:** 

القيمة الافتراضية هي 0.

 **Examples:** 

يوضح كيفية تغيير دقة الصور في مستند PDF.

```

 Document doc = new Document(getMyDir() + "Images.docx");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // By default, Aspose.Words downsample all images in a document that we save to PDF to 220 ppi.
 Assert.assertTrue(options.getDownsampleOptions().getDownsampleImages());
 Assert.assertEquals(220, options.getDownsampleOptions().getResolution());
 Assert.assertEquals(0, options.getDownsampleOptions().getResolutionThreshold());

 doc.save(getArtifactsDir() + "PdfSaveOptions.DownsampleOptions.Default.pdf", options);

 // Set the "Resolution" property to "36" to downsample all images to 36 ppi.
 options.getDownsampleOptions().setResolution(36);

 // Set the "ResolutionThreshold" property to only apply the downsampling to
 // images with a resolution that is above 128 ppi.
 options.getDownsampleOptions().setResolutionThreshold(128);

 // Only the first two images from the document will be downsampled at this stage.
 doc.save(getArtifactsDir() + "PdfSaveOptions.DownsampleOptions.LowerResolution.pdf", options);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | int | القيمة  int  المقابلة. |

