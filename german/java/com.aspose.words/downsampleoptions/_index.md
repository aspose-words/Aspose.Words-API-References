---
title: "DownsampleOptions"
linktitle: "DownsampleOptions"
second_title: "Aspose.Words für Java"
description: "Ermöglicht das Festlegen von Downsample-Optionen in Java."
type: docs
weight: 176
url: /de/java/com.aspose.words/downsampleoptions/
---

**Inheritance:**
java.lang.Object
```
public class DownsampleOptions
```

Ermöglicht das Angeben von Downsample-Optionen.

Um mehr zu erfahren, besuchen Sie den [ Save a Document ][Save a Document] Dokumentationsartikel.

 **Examples:** 

Zeigt, wie die Auflösung von Bildern im PDF-Dokument geändert wird.

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
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getDownsampleImages()](#getDownsampleImages) | Gibt an, ob Bilder downsamplet werden sollen. |
| [getResolution()](#getResolution) | Gibt die Auflösung in Pixel pro Zoll an, auf die die Bilder downsamplet werden sollen. |
| [getResolutionThreshold()](#getResolutionThreshold) | Gibt die Schwellenauflösung in Pixel pro Zoll an. |
| [setDownsampleImages(boolean value)](#setDownsampleImages-boolean) | Gibt an, ob Bilder downsamplet werden sollen. |
| [setResolution(int value)](#setResolution-int) | Gibt die Auflösung in Pixel pro Zoll an, auf die die Bilder downsamplet werden sollen. |
| [setResolutionThreshold(int value)](#setResolutionThreshold-int) | Gibt die Schwellenauflösung in Pixel pro Zoll an. |
### getDownsampleImages() {#getDownsampleImages}
```
public boolean getDownsampleImages()
```


Gibt an, ob Bilder downsamplet werden sollen.

 **Remarks:** 

Der Standardwert ist  true .

 **Examples:** 

Zeigt, wie die Auflösung von Bildern im PDF-Dokument geändert wird.

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
boolean - Der entsprechende  boolean  Wert.
### getResolution() {#getResolution}
```
public int getResolution()
```


Gibt die Auflösung in Pixel pro Zoll an, auf die die Bilder downsamplet werden sollen.

 **Remarks:** 

Der Standardwert ist 220 ppi.

 **Examples:** 

Zeigt, wie die Auflösung von Bildern im PDF-Dokument geändert wird.

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
int - Der entsprechende int-Wert.
### getResolutionThreshold() {#getResolutionThreshold}
```
public int getResolutionThreshold()
```


Gibt die Schwellenauflösung in Pixel pro Zoll an. Wenn die Auflösung eines Bildes im Dokument kleiner als der Schwellenwert ist, wird der Downsampling-Algorithmus nicht angewendet. Ein Wert von 0 bedeutet, dass die Schwellenwertprüfung nicht verwendet wird und alle Bilder, die verkleinert werden können, downsamplet werden.

 **Remarks:** 

Der Standardwert ist 0.

 **Examples:** 

Zeigt, wie die Auflösung von Bildern im PDF-Dokument geändert wird.

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
int - Der entsprechende int-Wert.
### setDownsampleImages(boolean value) {#setDownsampleImages-boolean}
```
public void setDownsampleImages(boolean value)
```


Gibt an, ob Bilder downsamplet werden sollen.

 **Remarks:** 

Der Standardwert ist  true .

 **Examples:** 

Zeigt, wie die Auflösung von Bildern im PDF-Dokument geändert wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setResolution(int value) {#setResolution-int}
```
public void setResolution(int value)
```


Gibt die Auflösung in Pixel pro Zoll an, auf die die Bilder downsamplet werden sollen.

 **Remarks:** 

Der Standardwert ist 220 ppi.

 **Examples:** 

Zeigt, wie die Auflösung von Bildern im PDF-Dokument geändert wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int | Der entsprechende  int  Wert. |

### setResolutionThreshold(int value) {#setResolutionThreshold-int}
```
public void setResolutionThreshold(int value)
```


Gibt die Schwellenauflösung in Pixel pro Zoll an. Wenn die Auflösung eines Bildes im Dokument kleiner als der Schwellenwert ist, wird der Downsampling-Algorithmus nicht angewendet. Ein Wert von 0 bedeutet, dass die Schwellenwertprüfung nicht verwendet wird und alle Bilder, die verkleinert werden können, downsamplet werden.

 **Remarks:** 

Der Standardwert ist 0.

 **Examples:** 

Zeigt, wie die Auflösung von Bildern im PDF-Dokument geändert wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int | Der entsprechende  int  Wert. |

