---
title: "DownsampleOptions"
linktitle: "DownsampleOptions"
second_title: "Aspose.Words para Java"
description: "Permite especificar opciones de submuestreo en Java."
type: docs
weight: 176
url: /es/java/com.aspose.words/downsampleoptions/
---

**Inheritance:**
java.lang.Object
```
public class DownsampleOptions
```

Permite especificar opciones de submuestreo.

Para obtener más información, visite el artículo de documentación [ Save a Document ][Save a Document].

 **Examples:** 

Muestra cómo cambiar la resolución de las imágenes en el documento PDF.

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
## Métodos

| Método | Descripción |
| --- | --- |
| [getDownsampleImages()](#getDownsampleImages) | Especifica si las imágenes deben ser submuestreadas. |
| [getResolution()](#getResolution) | Especifica la resolución en píxeles por pulgada a la que deben submuestrearse las imágenes. |
| [getResolutionThreshold()](#getResolutionThreshold) | Especifica la resolución umbral en píxeles por pulgada. |
| [setDownsampleImages(boolean value)](#setDownsampleImages-boolean) | Especifica si las imágenes deben ser submuestreadas. |
| [setResolution(int value)](#setResolution-int) | Especifica la resolución en píxeles por pulgada a la que deben submuestrearse las imágenes. |
| [setResolutionThreshold(int value)](#setResolutionThreshold-int) | Especifica la resolución umbral en píxeles por pulgada. |
### getDownsampleImages() {#getDownsampleImages}
```
public boolean getDownsampleImages()
```


Especifica si las imágenes deben ser submuestreadas.

 **Remarks:** 

El valor predeterminado es  true .

 **Examples:** 

Muestra cómo cambiar la resolución de las imágenes en el documento PDF.

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
boolean - El valor  boolean  correspondiente.
### getResolution() {#getResolution}
```
public int getResolution()
```


Especifica la resolución en píxeles por pulgada a la que deben submuestrearse las imágenes.

 **Remarks:** 

El valor predeterminado es 220 ppi.

 **Examples:** 

Muestra cómo cambiar la resolución de las imágenes en el documento PDF.

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
int - El valor  int  correspondiente.
### getResolutionThreshold() {#getResolutionThreshold}
```
public int getResolutionThreshold()
```


Especifica la resolución umbral en píxeles por pulgada. Si la resolución de una imagen en el documento es inferior al valor umbral, no se aplicará el algoritmo de submuestreo. Un valor de 0 significa que la verificación del umbral no se utiliza y todas las imágenes que pueden reducirse de tamaño se submuestrean.

 **Remarks:** 

El valor predeterminado es 0.

 **Examples:** 

Muestra cómo cambiar la resolución de las imágenes en el documento PDF.

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
int - El valor  int  correspondiente.
### setDownsampleImages(boolean value) {#setDownsampleImages-boolean}
```
public void setDownsampleImages(boolean value)
```


Especifica si las imágenes deben ser submuestreadas.

 **Remarks:** 

El valor predeterminado es  true .

 **Examples:** 

Muestra cómo cambiar la resolución de las imágenes en el documento PDF.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setResolution(int value) {#setResolution-int}
```
public void setResolution(int value)
```


Especifica la resolución en píxeles por pulgada a la que deben submuestrearse las imágenes.

 **Remarks:** 

El valor predeterminado es 220 ppi.

 **Examples:** 

Muestra cómo cambiar la resolución de las imágenes en el documento PDF.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | int | El valor  int  correspondiente. |

### setResolutionThreshold(int value) {#setResolutionThreshold-int}
```
public void setResolutionThreshold(int value)
```


Especifica la resolución umbral en píxeles por pulgada. Si la resolución de una imagen en el documento es inferior al valor umbral, no se aplicará el algoritmo de submuestreo. Un valor de 0 significa que la verificación del umbral no se utiliza y todas las imágenes que pueden reducirse de tamaño se submuestrean.

 **Remarks:** 

El valor predeterminado es 0.

 **Examples:** 

Muestra cómo cambiar la resolución de las imágenes en el documento PDF.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | int | El valor  int  correspondiente. |

