---
title: "ImageWatermarkOptions"
linktitle: "ImageWatermarkOptions"
second_title: "Aspose.Words per Java"
description: "Contiene opzioni che possono essere specificate quando si aggiunge una filigrana con immagine in Java."
type: docs
weight: 398
url: /it/java/com.aspose.words/imagewatermarkoptions/
---

**Inheritance:**
java.lang.Object
```
public class ImageWatermarkOptions
```

Contiene opzioni che possono essere specificate quando si aggiunge una filigrana con immagine.

Per saperne di più, visita l'articolo di documentazione [ Working with Watermark ][Working with Watermark].

 **Examples:** 

Mostra come creare una filigrana da un'immagine nel file system locale.

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
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getScale()](#getScale) | Ottiene il fattore di scala espresso come frazione dell'immagine. |
| [isWashout()](#isWashout) | Ottiene un valore booleano che è responsabile dell'effetto di sbiadimento della filigrana. |
| [isWashout(boolean value)](#isWashout-boolean) | Imposta un valore booleano che è responsabile dell'effetto di sbiadimento della filigrana. |
| [setScale(double value)](#setScale-double) | Imposta il fattore di scala espresso come frazione dell'immagine. |
### getScale() {#getScale}
```
public double getScale()
```


Ottiene il fattore di scala espresso come frazione dell'immagine. Il valore predefinito è 0 - auto.

**Returns:**
double - Il fattore di scala espresso come frazione dell'immagine.
### isWashout() {#isWashout}
```
public boolean isWashout()
```


Ottiene un valore booleano che è responsabile dell'effetto di sbiadimento della filigrana. Il valore predefinito è true.

 **Examples:** 

Mostra come creare una filigrana da un'immagine nel file system locale.

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
boolean - Un valore booleano che è responsabile dell'effetto di sbiadimento della filigrana.
### isWashout(boolean value) {#isWashout-boolean}
```
public void isWashout(boolean value)
```


Imposta un valore booleano che è responsabile dell'effetto di sbiadimento della filigrana. Il valore predefinito è true.

 **Examples:** 

Mostra come creare una filigrana da un'immagine nel file system locale.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Un valore booleano che è responsabile dell'effetto di sbiadimento della filigrana. |

### setScale(double value) {#setScale-double}
```
public void setScale(double value)
```


Imposta il fattore di scala espresso come frazione dell'immagine. Il valore predefinito è 0 - auto.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | double | Il fattore di scala espresso come frazione dell'immagine. |

