---
title: "DownsampleOptions"
linktitle: "DownsampleOptions"
second_title: "Aspose.Words Java için"
description: "Java'da downsample seçeneklerini belirtmeye izin verir."
type: docs
weight: 176
url: /tr/java/com.aspose.words/downsampleoptions/
---

**Inheritance:**
java.lang.Object
```
public class DownsampleOptions
```

Aşağı örnekleme seçeneklerini belirtmeye izin verir.

Daha fazla bilgi edinmek için [ Save a Document ][Save a Document] dokümantasyon makalesini ziyaret edin.

 **Examples:** 

PDF belgesindeki görüntülerin çözünürlüğünü nasıl değiştireceğinizi gösterir.

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
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getDownsampleImages()](#getDownsampleImages) | Görüntülerin downsample edilip edilmeyeceğini belirtir. |
| [getResolution()](#getResolution) | Görüntülerin downsample edileceği inç başına piksel (ppi) cinsinden çözünürlüğü belirtir. |
| [getResolutionThreshold()](#getResolutionThreshold) | Eşik çözünürlüğü inç başına piksel (ppi) olarak belirtir. |
| [setDownsampleImages(boolean value)](#setDownsampleImages-boolean) | Görüntülerin downsample edilip edilmeyeceğini belirtir. |
| [setResolution(int value)](#setResolution-int) | Görüntülerin downsample edileceği inç başına piksel (ppi) cinsinden çözünürlüğü belirtir. |
| [setResolutionThreshold(int value)](#setResolutionThreshold-int) | Eşik çözünürlüğü inç başına piksel (ppi) olarak belirtir. |
### getDownsampleImages() {#getDownsampleImages}
```
public boolean getDownsampleImages()
```


Görüntülerin downsample edilip edilmeyeceğini belirtir.

 **Remarks:** 

Varsayılan değer  true .

 **Examples:** 

PDF belgesindeki görüntülerin çözünürlüğünü nasıl değiştireceğinizi gösterir.

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
boolean - İlgili  boolean  değeri.
### getResolution() {#getResolution}
```
public int getResolution()
```


Görüntülerin downsample edileceği inç başına piksel (ppi) cinsinden çözünürlüğü belirtir.

 **Remarks:** 

Varsayılan değer 220 ppi.

 **Examples:** 

PDF belgesindeki görüntülerin çözünürlüğünü nasıl değiştireceğinizi gösterir.

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
int - İlgili  int  değeri.
### getResolutionThreshold() {#getResolutionThreshold}
```
public int getResolutionThreshold()
```


Eşik çözünürlüğü inç başına piksel olarak belirtir. Belgedeki bir görüntünün çözünürlüğü eşik değerinden düşükse, downsampling algoritması uygulanmaz. 0 değeri, eşik kontrolünün kullanılmadığını ve boyutu küçültülebilen tüm görüntülerin downsample edileceğini ifade eder.

 **Remarks:** 

Varsayılan değer 0.

 **Examples:** 

PDF belgesindeki görüntülerin çözünürlüğünü nasıl değiştireceğinizi gösterir.

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
int - İlgili  int  değeri.
### setDownsampleImages(boolean value) {#setDownsampleImages-boolean}
```
public void setDownsampleImages(boolean value)
```


Görüntülerin downsample edilip edilmeyeceğini belirtir.

 **Remarks:** 

Varsayılan değer  true .

 **Examples:** 

PDF belgesindeki görüntülerin çözünürlüğünü nasıl değiştireceğinizi gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setResolution(int value) {#setResolution-int}
```
public void setResolution(int value)
```


Görüntülerin downsample edileceği inç başına piksel (ppi) cinsinden çözünürlüğü belirtir.

 **Remarks:** 

Varsayılan değer 220 ppi.

 **Examples:** 

PDF belgesindeki görüntülerin çözünürlüğünü nasıl değiştireceğinizi gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | int | İlgili  int  değeri. |

### setResolutionThreshold(int value) {#setResolutionThreshold-int}
```
public void setResolutionThreshold(int value)
```


Eşik çözünürlüğü inç başına piksel olarak belirtir. Belgedeki bir görüntünün çözünürlüğü eşik değerinden düşükse, downsampling algoritması uygulanmaz. 0 değeri, eşik kontrolünün kullanılmadığını ve boyutu küçültülebilen tüm görüntülerin downsample edileceğini ifade eder.

 **Remarks:** 

Varsayılan değer 0.

 **Examples:** 

PDF belgesindeki görüntülerin çözünürlüğünü nasıl değiştireceğinizi gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | int | İlgili  int  değeri. |

