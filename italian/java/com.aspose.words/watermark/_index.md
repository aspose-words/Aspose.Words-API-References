---
title: "Filigrana"
linktitle: "Filigrana"
second_title: "Aspose.Words per Java"
description: "Rappresenta la classe per lavorare con il watermark del documento in Java."
type: docs
weight: 721
url: /it/java/com.aspose.words/watermark/
---

**Inheritance:**
java.lang.Object
```
public class Watermark
```

Rappresenta la classe per lavorare con la filigrana del documento.

Per saperne di più, visita l'articolo di documentazione [ Working with Watermark ][Working with Watermark].

 **Examples:** 

Mostra come creare una filigrana di testo.

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
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getType()](#getType) | Ottiene il tipo di watermark. |
| [remove()](#remove) | Rimuove il watermark. |
| [setImage(BufferedImage image)](#setImage-java.awt.image.BufferedImage) | Aggiunge un watermark immagine al documento. |
| [setImage(BufferedImage image, ImageWatermarkOptions options)](#setImage-java.awt.image.BufferedImage-com.aspose.words.ImageWatermarkOptions) | Aggiunge un watermark immagine al documento. |
| [setImage(InputStream imageStream, ImageWatermarkOptions options)](#setImage-java.io.InputStream-com.aspose.words.ImageWatermarkOptions) | Aggiunge un watermark immagine al documento. |
| [setImage(String imagePath, ImageWatermarkOptions options)](#setImage-java.lang.String-com.aspose.words.ImageWatermarkOptions) | Aggiunge un watermark immagine al documento. |
| [setText(String text)](#setText-java.lang.String) | Aggiunge un watermark di testo al documento. |
| [setText(String text, TextWatermarkOptions options)](#setText-java.lang.String-com.aspose.words.TextWatermarkOptions) | Aggiunge un watermark di testo al documento. |
### getType() {#getType}
```
public int getType()
```


Ottiene il tipo di watermark.

 **Examples:** 

Mostra come creare una filigrana di testo.

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
int - Il tipo di watermark. Il valore restituito è una delle costanti [WatermarkType](../../com.aspose.words/watermarktype/).
### remove() {#remove}
```
public void remove()
```


Rimuove il watermark.

 **Examples:** 

Mostra come creare una filigrana di testo.

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


Aggiunge un watermark immagine al documento.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| immagine | java.awt.image.BufferedImage | Immagine visualizzata come filigrana. |

### setImage(BufferedImage image, ImageWatermarkOptions options) {#setImage-java.awt.image.BufferedImage-com.aspose.words.ImageWatermarkOptions}
```
public void setImage(BufferedImage image, ImageWatermarkOptions options)
```


Aggiunge un watermark immagine al documento.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| immagine | java.awt.image.BufferedImage | Immagine visualizzata come filigrana. |
| options | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) | Definisce opzioni aggiuntive per la filigrana immagine. |

### setImage(InputStream imageStream, ImageWatermarkOptions options) {#setImage-java.io.InputStream-com.aspose.words.ImageWatermarkOptions}
```
public void setImage(InputStream imageStream, ImageWatermarkOptions options)
```


Aggiunge un watermark immagine al documento.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| imageStream | java.io.InputStream | Il flusso contenente i dati dell'immagine visualizzata come watermark. |
| options | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) | Definisce opzioni aggiuntive per la filigrana immagine. |

### setImage(String imagePath, ImageWatermarkOptions options) {#setImage-java.lang.String-com.aspose.words.ImageWatermarkOptions}
```
public void setImage(String imagePath, ImageWatermarkOptions options)
```


Aggiunge un watermark immagine al documento.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| imagePath | java.lang.String | Percorso al file immagine visualizzato come watermark. |
| options | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) | Definisce opzioni aggiuntive per la filigrana immagine. |

### setText(String text) {#setText-java.lang.String}
```
public void setText(String text)
```


Aggiunge un watermark di testo al documento.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| text | java.lang.String | Testo visualizzato come filigrana. |

### setText(String text, TextWatermarkOptions options) {#setText-java.lang.String-com.aspose.words.TextWatermarkOptions}
```
public void setText(String text, TextWatermarkOptions options)
```


Aggiunge un watermark di testo al documento.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| text | java.lang.String | Testo visualizzato come filigrana. |
| options | [TextWatermarkOptions](../../com.aspose.words/textwatermarkoptions/) | Definisce opzioni aggiuntive per la filigrana testo. |

