---
title: "Marca de agua"
linktitle: "Marca de agua"
second_title: "Aspose.Words para Java"
description: "Representa una clase para trabajar con marcas de agua de documentos en Java."
type: docs
weight: 721
url: /es/java/com.aspose.words/watermark/
---

**Inheritance:**
java.lang.Object
```
public class Watermark
```

Representa la clase para trabajar con la marca de agua del documento.

Para obtener más información, visite el artículo de documentación [ Working with Watermark ][Working with Watermark].

 **Examples:** 

Muestra cómo crear una marca de agua de texto.

```

 Document doc = new Document();

 // Add a plain text watermark.
 doc.getWatermark().setText("Aspose Watermark");

 // If we wish to edit the text formatting using it as a watermark,
 // we can do so by passing a TextWatermarkOptions object when creating the watermark.
 TextWatermarkOptions textWatermarkOptions = new TextWatermarkOptions();
 textWatermarkOptions.setFontFamily("Arial");
 textWatermarkOptions.setFontSize(36f);
 textWatermarkOptions.setColor(Color.BLACK);
 textWatermarkOptions.setLayout(WatermarkLayout.DIAGONAL);
 textWatermarkOptions.isSemitrasparent(false);

 doc.getWatermark().setText("Aspose Watermark", textWatermarkOptions);

 doc.save(getArtifactsDir() + "Document.TextWatermark.docx");

 // We can remove a watermark from a document like this.
 if (doc.getWatermark().getType() == WatermarkType.TEXT)
     doc.getWatermark().remove();
 
```


[Working with Watermark]: https://docs.aspose.com/words/java/working-with-watermark/
## Métodos

| Método | Descripción |
| --- | --- |
| [getType()](#getType) | Obtiene el tipo de marca de agua. |
| [remove()](#remove) | Elimina la marca de agua. |
| [setImage(BufferedImage image)](#setImage-java.awt.image.BufferedImage) | Agrega una marca de agua de Imagen al documento. |
| [setImage(BufferedImage image, ImageWatermarkOptions options)](#setImage-java.awt.image.BufferedImage-com.aspose.words.ImageWatermarkOptions) | Agrega una marca de agua de Imagen al documento. |
| [setImage(InputStream imageStream, ImageWatermarkOptions options)](#setImage-java.io.InputStream-com.aspose.words.ImageWatermarkOptions) | Agrega una marca de agua de Imagen al documento. |
| [setImage(String imagePath, ImageWatermarkOptions options)](#setImage-java.lang.String-com.aspose.words.ImageWatermarkOptions) | Agrega una marca de agua de Imagen al documento. |
| [setText(String text)](#setText-java.lang.String) | Agrega una marca de agua de Texto al documento. |
| [setText(String text, TextWatermarkOptions options)](#setText-java.lang.String-com.aspose.words.TextWatermarkOptions) | Agrega una marca de agua de Texto al documento. |
### getType() {#getType}
```
public int getType()
```


Obtiene el tipo de marca de agua.

 **Examples:** 

Muestra cómo crear una marca de agua de texto.

```

 Document doc = new Document();

 // Add a plain text watermark.
 doc.getWatermark().setText("Aspose Watermark");

 // If we wish to edit the text formatting using it as a watermark,
 // we can do so by passing a TextWatermarkOptions object when creating the watermark.
 TextWatermarkOptions textWatermarkOptions = new TextWatermarkOptions();
 textWatermarkOptions.setFontFamily("Arial");
 textWatermarkOptions.setFontSize(36f);
 textWatermarkOptions.setColor(Color.BLACK);
 textWatermarkOptions.setLayout(WatermarkLayout.DIAGONAL);
 textWatermarkOptions.isSemitrasparent(false);

 doc.getWatermark().setText("Aspose Watermark", textWatermarkOptions);

 doc.save(getArtifactsDir() + "Document.TextWatermark.docx");

 // We can remove a watermark from a document like this.
 if (doc.getWatermark().getType() == WatermarkType.TEXT)
     doc.getWatermark().remove();
 
```

**Returns:**
int - El tipo de marca de agua. El valor devuelto es una de las constantes de [WatermarkType](../../com.aspose.words/watermarktype/).
### remove() {#remove}
```
public void remove()
```


Elimina la marca de agua.

 **Examples:** 

Muestra cómo crear una marca de agua de texto.

```

 Document doc = new Document();

 // Add a plain text watermark.
 doc.getWatermark().setText("Aspose Watermark");

 // If we wish to edit the text formatting using it as a watermark,
 // we can do so by passing a TextWatermarkOptions object when creating the watermark.
 TextWatermarkOptions textWatermarkOptions = new TextWatermarkOptions();
 textWatermarkOptions.setFontFamily("Arial");
 textWatermarkOptions.setFontSize(36f);
 textWatermarkOptions.setColor(Color.BLACK);
 textWatermarkOptions.setLayout(WatermarkLayout.DIAGONAL);
 textWatermarkOptions.isSemitrasparent(false);

 doc.getWatermark().setText("Aspose Watermark", textWatermarkOptions);

 doc.save(getArtifactsDir() + "Document.TextWatermark.docx");

 // We can remove a watermark from a document like this.
 if (doc.getWatermark().getType() == WatermarkType.TEXT)
     doc.getWatermark().remove();
 
```

### setImage(BufferedImage image) {#setImage-java.awt.image.BufferedImage}
```
public void setImage(BufferedImage image)
```


Agrega una marca de agua de Imagen al documento.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| imagen | java.awt.image.BufferedImage | Imagen que se muestra como marca de agua. |

### setImage(BufferedImage image, ImageWatermarkOptions options) {#setImage-java.awt.image.BufferedImage-com.aspose.words.ImageWatermarkOptions}
```
public void setImage(BufferedImage image, ImageWatermarkOptions options)
```


Agrega una marca de agua de Imagen al documento.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| imagen | java.awt.image.BufferedImage | Imagen que se muestra como marca de agua. |
| options | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) | Define opciones adicionales para la marca de agua de imagen. |

### setImage(InputStream imageStream, ImageWatermarkOptions options) {#setImage-java.io.InputStream-com.aspose.words.ImageWatermarkOptions}
```
public void setImage(InputStream imageStream, ImageWatermarkOptions options)
```


Agrega una marca de agua de Imagen al documento.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| imageStream | java.io.InputStream | El flujo que contiene los datos de la imagen que se muestra como marca de agua. |
| options | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) | Define opciones adicionales para la marca de agua de imagen. |

### setImage(String imagePath, ImageWatermarkOptions options) {#setImage-java.lang.String-com.aspose.words.ImageWatermarkOptions}
```
public void setImage(String imagePath, ImageWatermarkOptions options)
```


Agrega una marca de agua de Imagen al documento.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| imagePath | java.lang.String | Ruta al archivo de imagen que se muestra como marca de agua. |
| options | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) | Define opciones adicionales para la marca de agua de imagen. |

### setText(String text) {#setText-java.lang.String}
```
public void setText(String text)
```


Agrega una marca de agua de Texto al documento.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| text | java.lang.String | Texto que se muestra como marca de agua. |

### setText(String text, TextWatermarkOptions options) {#setText-java.lang.String-com.aspose.words.TextWatermarkOptions}
```
public void setText(String text, TextWatermarkOptions options)
```


Agrega una marca de agua de Texto al documento.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| text | java.lang.String | Texto que se muestra como marca de agua. |
| options | [TextWatermarkOptions](../../com.aspose.words/textwatermarkoptions/) | Define opciones adicionales para la marca de agua de texto. |

