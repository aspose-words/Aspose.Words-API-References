---
title: "ImageWatermarkOptions"
linktitle: "ImageWatermarkOptions"
second_title: "Aspose.Words para Java"
description: "Contiene opciones que pueden especificarse al agregar una marca de agua con imagen en Java."
type: docs
weight: 398
url: /es/java/com.aspose.words/imagewatermarkoptions/
---

**Inheritance:**
java.lang.Object
```
public class ImageWatermarkOptions
```

Contiene opciones que pueden especificarse al agregar una marca de agua con imagen.

Para obtener más información, visite el artículo de documentación [ Working with Watermark ][Working with Watermark].

 **Examples:** 

Muestra cómo crear una marca de agua a partir de una imagen en el sistema de archivos local.

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
## Métodos

| Método | Descripción |
| --- | --- |
| [getScale()](#getScale) | Obtiene el factor de escala expresado como una fracción de la imagen. |
| [isWashout()](#isWashout) | Obtiene un valor booleano que es responsable del efecto de desvanecimiento de la marca de agua. |
| [isWashout(boolean value)](#isWashout-boolean) | Establece un valor booleano que es responsable del efecto de desvanecimiento de la marca de agua. |
| [setScale(double value)](#setScale-double) | Establece el factor de escala expresado como una fracción de la imagen. |
### getScale() {#getScale}
```
public double getScale()
```


Obtiene el factor de escala expresado como una fracción de la imagen. El valor predeterminado es 0 - automático.

**Returns:**
double - El factor de escala expresado como una fracción de la imagen.
### isWashout() {#isWashout}
```
public boolean isWashout()
```


Obtiene un valor booleano que es responsable del efecto de desvanecimiento de la marca de agua. El valor predeterminado es true.

 **Examples:** 

Muestra cómo crear una marca de agua a partir de una imagen en el sistema de archivos local.

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
boolean - Un valor booleano que es responsable del efecto de desvanecimiento de la marca de agua.
### isWashout(boolean value) {#isWashout-boolean}
```
public void isWashout(boolean value)
```


Establece un valor booleano que es responsable del efecto de desvanecimiento de la marca de agua. El valor predeterminado es true.

 **Examples:** 

Muestra cómo crear una marca de agua a partir de una imagen en el sistema de archivos local.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | Un valor booleano que es responsable del efecto de desvanecimiento de la marca de agua. |

### setScale(double value) {#setScale-double}
```
public void setScale(double value)
```


Establece el factor de escala expresado como una fracción de la imagen. El valor predeterminado es 0 - automático.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double | El factor de escala expresado como una fracción de la imagen. |

