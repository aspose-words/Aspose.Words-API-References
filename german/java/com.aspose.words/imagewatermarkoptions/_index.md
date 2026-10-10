---
title: "ImageWatermarkOptions"
linktitle: "ImageWatermarkOptions"
second_title: "Aspose.Words für Java"
description: "Enthält Optionen, die beim Hinzufügen eines Wasserzeichens mit Bild in Java angegeben werden können."
type: docs
weight: 398
url: /de/java/com.aspose.words/imagewatermarkoptions/
---

**Inheritance:**
java.lang.Object
```
public class ImageWatermarkOptions
```

Enthält Optionen, die beim Hinzufügen eines Wasserzeichens mit Bild angegeben werden können.

Um mehr zu erfahren, besuchen Sie den [ Working with Watermark ][Working with Watermark] Dokumentationsartikel.

 **Examples:** 

Zeigt, wie man ein Wasserzeichen aus einem Bild im lokalen Dateisystem erstellt.

```

 Document doc = new Document();

 // Modify the image watermark's appearance with an ImageWatermarkOptions object,
 // then pass it while creating a watermark from an image file.
 ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
 imageWatermarkOptions.setScale(5.0);
 imageWatermarkOptions.isWashout(false);

 // We have a different options to insert image:
 doc.getWatermark().setImage(ImageIO.read(new File(getImageDir() + "Logo.jpg")), imageWatermarkOptions);

 doc.getWatermark().setImage(ImageIO.read(new File(getImageDir() + "Logo.jpg")));

 doc.getWatermark().setImage(getImageDir() + "Logo.jpg", imageWatermarkOptions);

 doc.save(getArtifactsDir() + "Document.ImageWatermark.docx");
 
```


[Working with Watermark]: https://docs.aspose.com/words/java/working-with-watermark/
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getScale()](#getScale) | Ruft den Skalierungsfaktor ab, ausgedrückt als Bruchteil des Bildes. |
| [isWashout()](#isWashout) | Ruft einen booleschen Wert ab, der für den Auswasch-Effekt des Wasserzeichens verantwortlich ist. |
| [isWashout(boolean value)](#isWashout-boolean) | Setzt einen booleschen Wert, der für den Auswasch-Effekt des Wasserzeichens verantwortlich ist. |
| [setScale(double value)](#setScale-double) | Setzt den Skalierungsfaktor, ausgedrückt als Bruchteil des Bildes. |
### getScale() {#getScale}
```
public double getScale()
```


Ruft den Skalierungsfaktor ab, ausgedrückt als Bruchteil des Bildes. Der Standardwert ist 0 – automatisch.

**Returns:**
double – Der Skalierungsfaktor, ausgedrückt als Bruchteil des Bildes.
### isWashout() {#isWashout}
```
public boolean isWashout()
```


Ruft einen booleschen Wert ab, der für den Auswasch-Effekt des Wasserzeichens verantwortlich ist. Der Standardwert ist  true .

 **Examples:** 

Zeigt, wie man ein Wasserzeichen aus einem Bild im lokalen Dateisystem erstellt.

```

 Document doc = new Document();

 // Modify the image watermark's appearance with an ImageWatermarkOptions object,
 // then pass it while creating a watermark from an image file.
 ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
 imageWatermarkOptions.setScale(5.0);
 imageWatermarkOptions.isWashout(false);

 // We have a different options to insert image:
 doc.getWatermark().setImage(ImageIO.read(new File(getImageDir() + "Logo.jpg")), imageWatermarkOptions);

 doc.getWatermark().setImage(ImageIO.read(new File(getImageDir() + "Logo.jpg")));

 doc.getWatermark().setImage(getImageDir() + "Logo.jpg", imageWatermarkOptions);

 doc.save(getArtifactsDir() + "Document.ImageWatermark.docx");
 
```

**Returns:**
boolean – Ein boolescher Wert, der für den Auswasch-Effekt des Wasserzeichens verantwortlich ist.
### isWashout(boolean value) {#isWashout-boolean}
```
public void isWashout(boolean value)
```


Setzt einen booleschen Wert, der für den Auswasch-Effekt des Wasserzeichens verantwortlich ist. Der Standardwert ist  true .

 **Examples:** 

Zeigt, wie man ein Wasserzeichen aus einem Bild im lokalen Dateisystem erstellt.

```

 Document doc = new Document();

 // Modify the image watermark's appearance with an ImageWatermarkOptions object,
 // then pass it while creating a watermark from an image file.
 ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
 imageWatermarkOptions.setScale(5.0);
 imageWatermarkOptions.isWashout(false);

 // We have a different options to insert image:
 doc.getWatermark().setImage(ImageIO.read(new File(getImageDir() + "Logo.jpg")), imageWatermarkOptions);

 doc.getWatermark().setImage(ImageIO.read(new File(getImageDir() + "Logo.jpg")));

 doc.getWatermark().setImage(getImageDir() + "Logo.jpg", imageWatermarkOptions);

 doc.save(getArtifactsDir() + "Document.ImageWatermark.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Ein boolescher Wert, der für den Auswasch-Effekt des Wasserzeichens verantwortlich ist. |

### setScale(double value) {#setScale-double}
```
public void setScale(double value)
```


Setzt den Skalierungsfaktor, ausgedrückt als Bruchteil des Bildes. Der Standardwert ist 0 – automatisch.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | double | Der Skalierungsfaktor, ausgedrückt als Bruchteil des Bildes. |

