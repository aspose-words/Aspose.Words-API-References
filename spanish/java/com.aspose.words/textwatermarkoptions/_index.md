---
title: "TextWatermarkOptions"
linktitle: "TextWatermarkOptions"
second_title: "Aspose.Words para Java"
description: "Contiene opciones que pueden especificarse al agregar una marca de agua con texto en Java."
type: docs
weight: 678
url: /es/java/com.aspose.words/textwatermarkoptions/
---

**Inheritance:**
java.lang.Object
```
public class TextWatermarkOptions
```

Contiene opciones que pueden especificarse al agregar una marca de agua con texto.

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
| [getColor()](#getColor) | Obtiene el color de la fuente. |
| [getFontFamily()](#getFontFamily) | Obtiene el nombre de la familia de fuentes. |
| [getFontSize()](#getFontSize) | Obtiene un tamaño de fuente. |
| [getLayout()](#getLayout) | Obtiene el diseño de la marca de agua. |
| [isSemitrasparent()](#isSemitrasparent) | Obtiene un valor booleano que es responsable de la opacidad de la marca de agua. |
| [isSemitrasparent(boolean value)](#isSemitrasparent-boolean) | Establece un valor booleano que es responsable de la opacidad de la marca de agua. |
| [setColor(Color value)](#setColor-java.awt.Color) | Establece el color de la fuente. |
| [setFontFamily(String value)](#setFontFamily-java.lang.String) | Establece el nombre de la familia de fuentes. |
| [setFontSize(float value)](#setFontSize-float) | Establece un tamaño de fuente. |
| [setLayout(int value)](#setLayout-int) | Establece el diseño de la marca de agua. |
### getColor() {#getColor}
```
public Color getColor()
```


Obtiene el color de la fuente. El valor predeterminado es java.awt.Color\#getSilver().getSilver().

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
java.awt.Color - Color de la fuente.
### getFontFamily() {#getFontFamily}
```
public String getFontFamily()
```


Obtiene el nombre de la familia de fuentes. El valor predeterminado es "Calibri".

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
java.lang.String - Nombre de la familia de fuentes.
### getFontSize() {#getFontSize}
```
public float getFontSize()
```


Obtiene un tamaño de fuente. El valor predeterminado es 0 - automático.

**Returns:**
float - Un tamaño de fuente.
### getLayout() {#getLayout}
```
public int getLayout()
```


Obtiene el diseño de la marca de agua. El valor predeterminado es [WatermarkLayout.DIAGONAL](../../com.aspose.words/watermarklayout/\#DIAGONAL).

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
int - Diseño de la marca de agua. El valor devuelto es una de las constantes de [WatermarkLayout](../../com.aspose.words/watermarklayout/).
### isSemitrasparent() {#isSemitrasparent}
```
public boolean isSemitrasparent()
```


Obtiene un valor booleano que es responsable de la opacidad de la marca de agua. El valor predeterminado es true.

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
boolean - Un valor booleano que es responsable de la opacidad de la marca de agua.
### isSemitrasparent(boolean value) {#isSemitrasparent-boolean}
```
public void isSemitrasparent(boolean value)
```


Establece un valor booleano que es responsable de la opacidad de la marca de agua. El valor predeterminado es true.

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

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | Un valor booleano que es responsable de la opacidad de la marca de agua. |

### setColor(Color value) {#setColor-java.awt.Color}
```
public void setColor(Color value)
```


Establece el color de fuente. El valor predeterminado es java.awt.Color\#getSilver().getSilver().

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

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.awt.Color | Color de fuente. |

### setFontFamily(String value) {#setFontFamily-java.lang.String}
```
public void setFontFamily(String value)
```


Establece el nombre de la familia de fuentes. El valor predeterminado es "Calibri".

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

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | Nombre de la familia de fuentes. |

### setFontSize(float value) {#setFontSize-float}
```
public void setFontSize(float value)
```


Establece un tamaño de fuente. El valor predeterminado es 0 - automático.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | float | Un tamaño de fuente. |

### setLayout(int value) {#setLayout-int}
```
public void setLayout(int value)
```


Establece el diseño de la marca de agua. El valor predeterminado es [WatermarkLayout.DIAGONAL](../../com.aspose.words/watermarklayout/\#DIAGONAL).

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

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | Diseño de la marca de agua. El valor debe ser una de las constantes de [WatermarkLayout](../../com.aspose.words/watermarklayout/). |

