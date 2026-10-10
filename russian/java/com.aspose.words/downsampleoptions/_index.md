---
title: "DownsampleOptions"
linktitle: "DownsampleOptions"
second_title: "Aspose.Words для Java"
description: "Позволяет задавать параметры понижения дискретизации в Java."
type: docs
weight: 176
url: /ru/java/com.aspose.words/downsampleoptions/
---

**Inheritance:**
java.lang.Object
```
public class DownsampleOptions
```

Позволяет указать параметры понижения дискретизации.

Чтобы узнать больше, посетите статью документации [ Save a Document ][Save a Document].

 **Examples:** 

Показывает, как изменить разрешение изображений в PDF‑документе.

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
## Методы

| Метод | Описание |
| --- | --- |
| [getDownsampleImages()](#getDownsampleImages) | Указывает, следует ли понижать дискретизацию изображений. |
| [getResolution()](#getResolution) | Указывает разрешение в пикселях на дюйм, до которого следует понижать дискретизацию изображений. |
| [getResolutionThreshold()](#getResolutionThreshold) | Указывает пороговое разрешение в пикселях на дюйм. |
| [setDownsampleImages(boolean value)](#setDownsampleImages-boolean) | Указывает, следует ли понижать дискретизацию изображений. |
| [setResolution(int value)](#setResolution-int) | Указывает разрешение в пикселях на дюйм, до которого следует понижать дискретизацию изображений. |
| [setResolutionThreshold(int value)](#setResolutionThreshold-int) | Указывает пороговое разрешение в пикселях на дюйм. |
### getDownsampleImages() {#getDownsampleImages}
```
public boolean getDownsampleImages()
```


Указывает, следует ли понижать дискретизацию изображений.

 **Remarks:** 

Значение по умолчанию —  true .

 **Examples:** 

Показывает, как изменить разрешение изображений в PDF‑документе.

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
boolean - Соответствующее  boolean  значение.
### getResolution() {#getResolution}
```
public int getResolution()
```


Указывает разрешение в пикселях на дюйм, до которого следует понижать дискретизацию изображений.

 **Remarks:** 

Значение по умолчанию — 220 ppi.

 **Examples:** 

Показывает, как изменить разрешение изображений в PDF‑документе.

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
int — соответствующее значение  int .
### getResolutionThreshold() {#getResolutionThreshold}
```
public int getResolutionThreshold()
```


Указывает пороговое разрешение в пикселях на дюйм. Если разрешение изображения в документе меньше порогового значения, алгоритм понижения дискретизации не будет применён. Значение 0 означает, что проверка порога не используется, и все изображения, которые можно уменьшить в размере, будут понижены.

 **Remarks:** 

Значение по умолчанию — 0.

 **Examples:** 

Показывает, как изменить разрешение изображений в PDF‑документе.

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
int — соответствующее значение  int .
### setDownsampleImages(boolean value) {#setDownsampleImages-boolean}
```
public void setDownsampleImages(boolean value)
```


Указывает, следует ли понижать дискретизацию изображений.

 **Remarks:** 

Значение по умолчанию —  true .

 **Examples:** 

Показывает, как изменить разрешение изображений в PDF‑документе.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### setResolution(int value) {#setResolution-int}
```
public void setResolution(int value)
```


Указывает разрешение в пикселях на дюйм, до которого следует понижать дискретизацию изображений.

 **Remarks:** 

Значение по умолчанию — 220 ppi.

 **Examples:** 

Показывает, как изменить разрешение изображений в PDF‑документе.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | int | Соответствующее  int  значение. |

### setResolutionThreshold(int value) {#setResolutionThreshold-int}
```
public void setResolutionThreshold(int value)
```


Указывает пороговое разрешение в пикселях на дюйм. Если разрешение изображения в документе меньше порогового значения, алгоритм понижения дискретизации не будет применён. Значение 0 означает, что проверка порога не используется, и все изображения, которые можно уменьшить в размере, будут понижены.

 **Remarks:** 

Значение по умолчанию — 0.

 **Examples:** 

Показывает, как изменить разрешение изображений в PDF‑документе.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | int | Соответствующее  int  значение. |

