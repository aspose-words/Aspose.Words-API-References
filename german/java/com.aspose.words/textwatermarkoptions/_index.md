---
title: "TextWatermarkOptions"
linktitle: "TextWatermarkOptions"
second_title: "Aspose.Words für Java"
description: "Enthält Optionen, die beim Hinzufügen eines Textwasserzeichens in Java angegeben werden können."
type: docs
weight: 678
url: /de/java/com.aspose.words/textwatermarkoptions/
---

**Inheritance:**
java.lang.Object
```
public class TextWatermarkOptions
```

Enthält Optionen, die beim Hinzufügen eines Wasserzeichens mit Text angegeben werden können.

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
| [getColor()](#getColor) | Liefert die Schriftfarbe. |
| [getFontFamily()](#getFontFamily) | Liefert den Schriftfamiliennamen. |
| [getFontSize()](#getFontSize) | Liefert eine Schriftgröße. |
| [getLayout()](#getLayout) | Liefert das Layout des Wasserzeichens. |
| [isSemitrasparent()](#isSemitrasparent) | Liefert einen booleschen Wert, der für die Deckkraft des Wasserzeichens verantwortlich ist. |
| [isSemitrasparent(boolean value)](#isSemitrasparent-boolean) | Setzt einen booleschen Wert, der für die Deckkraft des Wasserzeichens verantwortlich ist. |
| [setColor(Color value)](#setColor-java.awt.Color) | Setzt die Schriftfarbe. |
| [setFontFamily(String value)](#setFontFamily-java.lang.String) | Setzt den Schriftfamiliennamen. |
| [setFontSize(float value)](#setFontSize-float) | Setzt eine Schriftgröße. |
| [setLayout(int value)](#setLayout-int) | Setzt das Layout des Wasserzeichens. |
### getColor() {#getColor}
```
public Color getColor()
```


Liefert die Schriftfarbe. Der Standardwert ist java.awt.Color\#getSilver().getSilver().

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
java.awt.Color - Schriftfarbe.
### getFontFamily() {#getFontFamily}
```
public String getFontFamily()
```


Liefert den Namen der Schriftfamilie. Der Standardwert ist "Calibri".

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
java.lang.String - Schriftfamilienname.
### getFontSize() {#getFontSize}
```
public float getFontSize()
```


Liefert eine Schriftgröße. Der Standardwert ist 0 – automatisch.

**Returns:**
float - Eine Schriftgröße.
### getLayout() {#getLayout}
```
public int getLayout()
```


Liefert das Layout des Wasserzeichens. Der Standardwert ist [WatermarkLayout.DIAGONAL](../../com.aspose.words/watermarklayout/\#DIAGONAL).

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
int - Layout des Wasserzeichens. Der zurückgegebene Wert ist einer der Konstanten von [WatermarkLayout](../../com.aspose.words/watermarklayout/).
### isSemitrasparent() {#isSemitrasparent}
```
public boolean isSemitrasparent()
```


Liefert einen booleschen Wert, der für die Deckkraft des Wasserzeichens verantwortlich ist. Der Standardwert ist true.

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
boolean - Ein boolescher Wert, der für die Deckkraft des Wasserzeichens verantwortlich ist.
### isSemitrasparent(boolean value) {#isSemitrasparent-boolean}
```
public void isSemitrasparent(boolean value)
```


Setzt einen booleschen Wert, der für die Deckkraft des Wasserzeichens verantwortlich ist. Der Standardwert ist true.

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

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Ein boolescher Wert, der für die Deckkraft des Wasserzeichens verantwortlich ist. |

### setColor(Color value) {#setColor-java.awt.Color}
```
public void setColor(Color value)
```


Setzt die Schriftfarbe. Der Standardwert ist java.awt.Color\#getSilver().getSilver().

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

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.awt.Color | Schriftfarbe. |

### setFontFamily(String value) {#setFontFamily-java.lang.String}
```
public void setFontFamily(String value)
```


Setzt den Namen der Schriftfamilie. Der Standardwert ist "Calibri".

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

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Schriftfamilienname. |

### setFontSize(float value) {#setFontSize-float}
```
public void setFontSize(float value)
```


Setzt eine Schriftgröße. Der Standardwert ist 0 – automatisch.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | float | Eine Schriftgröße. |

### setLayout(int value) {#setLayout-int}
```
public void setLayout(int value)
```


Setzt das Layout des Wasserzeichens. Der Standardwert ist [WatermarkLayout.DIAGONAL](../../com.aspose.words/watermarklayout/\#DIAGONAL).

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

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Layout des Wasserzeichens. Der Wert muss einer der Konstanten von [WatermarkLayout](../../com.aspose.words/watermarklayout/) sein. |

