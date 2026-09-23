---
title: "Wasserzeichen"
linktitle: "Wasserzeichen"
second_title: "Aspose.Words für Java"
description: "Stellt eine Klasse dar, um mit Dokumenten‑Wasserzeichen in Java zu arbeiten."
type: docs
weight: 721
url: /de/java/com.aspose.words/watermark/
---

**Inheritance:**
java.lang.Object
```
public class Watermark
```

Stellt eine Klasse dar, um mit Dokumentwasserzeichen zu arbeiten.

Um mehr zu erfahren, besuchen Sie den [ Working with Watermark ][Working with Watermark] Dokumentationsartikel.

 **Examples:** 

Zeigt, wie man ein Textwasserzeichen erstellt.

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
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getType()](#getType) | Liest den Wasserzeichen‑Typ. |
| [remove()](#remove) | Entfernt das Wasserzeichen. |
| [setImage(BufferedImage image)](#setImage-java.awt.image.BufferedImage) | Fügt dem Dokument ein Bild‑Wasserzeichen hinzu. |
| [setImage(BufferedImage image, ImageWatermarkOptions options)](#setImage-java.awt.image.BufferedImage-com.aspose.words.ImageWatermarkOptions) | Fügt dem Dokument ein Bild‑Wasserzeichen hinzu. |
| [setImage(InputStream imageStream, ImageWatermarkOptions options)](#setImage-java.io.InputStream-com.aspose.words.ImageWatermarkOptions) | Fügt dem Dokument ein Bild‑Wasserzeichen hinzu. |
| [setImage(String imagePath, ImageWatermarkOptions options)](#setImage-java.lang.String-com.aspose.words.ImageWatermarkOptions) | Fügt dem Dokument ein Bild‑Wasserzeichen hinzu. |
| [setText(String text)](#setText-java.lang.String) | Fügt dem Dokument ein Text‑Wasserzeichen hinzu. |
| [setText(String text, TextWatermarkOptions options)](#setText-java.lang.String-com.aspose.words.TextWatermarkOptions) | Fügt dem Dokument ein Text‑Wasserzeichen hinzu. |
### getType() {#getType}
```
public int getType()
```


Liest den Wasserzeichen‑Typ.

 **Examples:** 

Zeigt, wie man ein Textwasserzeichen erstellt.

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
int – Der Wasserzeichen‑Typ. Der zurückgegebene Wert ist einer der Konstanten von [WatermarkType](../../com.aspose.words/watermarktype/).
### remove() {#remove}
```
public void remove()
```


Entfernt das Wasserzeichen.

 **Examples:** 

Zeigt, wie man ein Textwasserzeichen erstellt.

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


Fügt dem Dokument ein Bild‑Wasserzeichen hinzu.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Bild | java.awt.image.BufferedImage | Bild, das als Wasserzeichen angezeigt wird. |

### setImage(BufferedImage image, ImageWatermarkOptions options) {#setImage-java.awt.image.BufferedImage-com.aspose.words.ImageWatermarkOptions}
```
public void setImage(BufferedImage image, ImageWatermarkOptions options)
```


Fügt dem Dokument ein Bild‑Wasserzeichen hinzu.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Bild | java.awt.image.BufferedImage | Bild, das als Wasserzeichen angezeigt wird. |
| options | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) | Definiert zusätzliche Optionen für das Bildwasserzeichen. |

### setImage(InputStream imageStream, ImageWatermarkOptions options) {#setImage-java.io.InputStream-com.aspose.words.ImageWatermarkOptions}
```
public void setImage(InputStream imageStream, ImageWatermarkOptions options)
```


Fügt dem Dokument ein Bild‑Wasserzeichen hinzu.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| imageStream | java.io.InputStream | Der Stream, der die Bilddaten enthält, die als Wasserzeichen angezeigt werden. |
| options | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) | Definiert zusätzliche Optionen für das Bildwasserzeichen. |

### setImage(String imagePath, ImageWatermarkOptions options) {#setImage-java.lang.String-com.aspose.words.ImageWatermarkOptions}
```
public void setImage(String imagePath, ImageWatermarkOptions options)
```


Fügt dem Dokument ein Bild‑Wasserzeichen hinzu.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| imagePath | java.lang.String | Pfad zur Bilddatei, die als Wasserzeichen angezeigt wird. |
| options | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) | Definiert zusätzliche Optionen für das Bildwasserzeichen. |

### setText(String text) {#setText-java.lang.String}
```
public void setText(String text)
```


Fügt dem Dokument ein Text‑Wasserzeichen hinzu.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Text | java.lang.String | Text, der als Wasserzeichen angezeigt wird. |

### setText(String text, TextWatermarkOptions options) {#setText-java.lang.String-com.aspose.words.TextWatermarkOptions}
```
public void setText(String text, TextWatermarkOptions options)
```


Fügt dem Dokument ein Text‑Wasserzeichen hinzu.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Text | java.lang.String | Text, der als Wasserzeichen angezeigt wird. |
| options | [TextWatermarkOptions](../../com.aspose.words/textwatermarkoptions/) | Definiert zusätzliche Optionen für das Textwasserzeichen. |

