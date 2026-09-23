---
title: "Filigrane"
linktitle: "Filigrane"
second_title: "Aspose.Words pour Java"
description: "Représente la classe permettant de travailler avec le filigrane de document en Java."
type: docs
weight: 721
url: /fr/java/com.aspose.words/watermark/
---

**Inheritance:**
java.lang.Object
```
public class Watermark
```

Représente la classe permettant de travailler avec le filigrane du document.

Pour en savoir plus, consultez l'article de documentation [ Working with Watermark ][Working with Watermark].

 **Examples:** 

Montre comment créer un filigrane texte.

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
## Méthodes

| Méthode | Description |
| --- | --- |
| [getType()](#getType) | Obtient le type de filigrane. |
| [remove()](#remove) | Supprime le filigrane. |
| [setImage(BufferedImage image)](#setImage-java.awt.image.BufferedImage) | Ajoute un filigrane d'image dans le document. |
| [setImage(BufferedImage image, ImageWatermarkOptions options)](#setImage-java.awt.image.BufferedImage-com.aspose.words.ImageWatermarkOptions) | Ajoute un filigrane d'image dans le document. |
| [setImage(InputStream imageStream, ImageWatermarkOptions options)](#setImage-java.io.InputStream-com.aspose.words.ImageWatermarkOptions) | Ajoute un filigrane d'image dans le document. |
| [setImage(String imagePath, ImageWatermarkOptions options)](#setImage-java.lang.String-com.aspose.words.ImageWatermarkOptions) | Ajoute un filigrane d'image dans le document. |
| [setText(String text)](#setText-java.lang.String) | Ajoute un filigrane de texte dans le document. |
| [setText(String text, TextWatermarkOptions options)](#setText-java.lang.String-com.aspose.words.TextWatermarkOptions) | Ajoute un filigrane de texte dans le document. |
### getType() {#getType}
```
public int getType()
```


Obtient le type de filigrane.

 **Examples:** 

Montre comment créer un filigrane texte.

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
int - Le type de filigrane. La valeur retournée est l'une des constantes [WatermarkType](../../com.aspose.words/watermarktype/).
### remove() {#remove}
```
public void remove()
```


Supprime le filigrane.

 **Examples:** 

Montre comment créer un filigrane texte.

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


Ajoute un filigrane d'image dans le document.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| image | java.awt.image.BufferedImage | Image affichée comme filigrane. |

### setImage(BufferedImage image, ImageWatermarkOptions options) {#setImage-java.awt.image.BufferedImage-com.aspose.words.ImageWatermarkOptions}
```
public void setImage(BufferedImage image, ImageWatermarkOptions options)
```


Ajoute un filigrane d'image dans le document.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| image | java.awt.image.BufferedImage | Image affichée comme filigrane. |
| options | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) | Définit des options supplémentaires pour le filigrane image. |

### setImage(InputStream imageStream, ImageWatermarkOptions options) {#setImage-java.io.InputStream-com.aspose.words.ImageWatermarkOptions}
```
public void setImage(InputStream imageStream, ImageWatermarkOptions options)
```


Ajoute un filigrane d'image dans le document.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| imageStream | java.io.InputStream | Le flux contenant les données d'image affichées comme filigrane. |
| options | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) | Définit des options supplémentaires pour le filigrane image. |

### setImage(String imagePath, ImageWatermarkOptions options) {#setImage-java.lang.String-com.aspose.words.ImageWatermarkOptions}
```
public void setImage(String imagePath, ImageWatermarkOptions options)
```


Ajoute un filigrane d'image dans le document.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| imagePath | java.lang.String | Chemin du fichier image affiché comme filigrane. |
| options | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) | Définit des options supplémentaires pour le filigrane image. |

### setText(String text) {#setText-java.lang.String}
```
public void setText(String text)
```


Ajoute un filigrane de texte dans le document.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| text | java.lang.String | Texte affiché comme filigrane. |

### setText(String text, TextWatermarkOptions options) {#setText-java.lang.String-com.aspose.words.TextWatermarkOptions}
```
public void setText(String text, TextWatermarkOptions options)
```


Ajoute un filigrane de texte dans le document.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| text | java.lang.String | Texte affiché comme filigrane. |
| options | [TextWatermarkOptions](../../com.aspose.words/textwatermarkoptions/) | Définit des options supplémentaires pour le filigrane texte. |

