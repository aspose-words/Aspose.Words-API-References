---
title: TextWatermarkOptions
linktitle: TextWatermarkOptions
second_title: Aspose.Words for Java
description: Contains options that can be specified when adding a watermark with text in Java.
type: docs
weight: 629
url: /java/com.aspose.words/textwatermarkoptions/
---

**Inheritance:**
java.lang.Object
```
public class TextWatermarkOptions
```

Contains options that can be specified when adding a watermark with text.

To learn more, visit the [ Working with Watermark ][Working with Watermark] documentation article.

 **Examples:** 

Shows how to create a text watermark.

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
## Methods

| Method | Description |
| --- | --- |
| [getColor()](#getColor) | Gets font color. |
| [getFontFamily()](#getFontFamily) | Gets font family name. |
| [getFontSize()](#getFontSize) | Gets a font size. |
| [getLayout()](#getLayout) | Gets layout of the watermark. |
| [isSemitrasparent()](#isSemitrasparent) | Gets a boolean value which is responsible for opacity of the watermark. |
| [isSemitrasparent(boolean value)](#isSemitrasparent-boolean) | Sets a boolean value which is responsible for opacity of the watermark. |
| [setColor(Color value)](#setColor-java.awt.Color) | Sets font color. |
| [setFontFamily(String value)](#setFontFamily-java.lang.String) | Sets font family name. |
| [setFontSize(float value)](#setFontSize-float) | Sets a font size. |
| [setLayout(int value)](#setLayout-int) | Sets layout of the watermark. |
### getColor() {#getColor}
```
public Color getColor()
```


Gets font color. The default value is java.awt.Color\#getSilver().getSilver().

 **Examples:** 

Shows how to create a text watermark.

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
java.awt.Color - Font color.
### getFontFamily() {#getFontFamily}
```
public String getFontFamily()
```


Gets font family name. The default value is "Calibri".

 **Examples:** 

Shows how to create a text watermark.

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
java.lang.String - Font family name.
### getFontSize() {#getFontSize}
```
public float getFontSize()
```


Gets a font size. The default value is 0 - auto.

**Returns:**
float - A font size.
### getLayout() {#getLayout}
```
public int getLayout()
```


Gets layout of the watermark. The default value is [WatermarkLayout.DIAGONAL](../../com.aspose.words/watermarklayout/\#DIAGONAL).

 **Examples:** 

Shows how to create a text watermark.

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
int - Layout of the watermark. The returned value is one of [WatermarkLayout](../../com.aspose.words/watermarklayout/) constants.
### isSemitrasparent() {#isSemitrasparent}
```
public boolean isSemitrasparent()
```


Gets a boolean value which is responsible for opacity of the watermark. The default value is  true .

 **Examples:** 

Shows how to create a text watermark.

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
boolean - A boolean value which is responsible for opacity of the watermark.
### isSemitrasparent(boolean value) {#isSemitrasparent-boolean}
```
public void isSemitrasparent(boolean value)
```


Sets a boolean value which is responsible for opacity of the watermark. The default value is  true .

 **Examples:** 

Shows how to create a text watermark.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A boolean value which is responsible for opacity of the watermark. |

### setColor(Color value) {#setColor-java.awt.Color}
```
public void setColor(Color value)
```


Sets font color. The default value is java.awt.Color\#getSilver().getSilver().

 **Examples:** 

Shows how to create a text watermark.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Color | Font color. |

### setFontFamily(String value) {#setFontFamily-java.lang.String}
```
public void setFontFamily(String value)
```


Sets font family name. The default value is "Calibri".

 **Examples:** 

Shows how to create a text watermark.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | Font family name. |

### setFontSize(float value) {#setFontSize-float}
```
public void setFontSize(float value)
```


Sets a font size. The default value is 0 - auto.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | float | A font size. |

### setLayout(int value) {#setLayout-int}
```
public void setLayout(int value)
```


Sets layout of the watermark. The default value is [WatermarkLayout.DIAGONAL](../../com.aspose.words/watermarklayout/\#DIAGONAL).

 **Examples:** 

Shows how to create a text watermark.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | Layout of the watermark. The value must be one of [WatermarkLayout](../../com.aspose.words/watermarklayout/) constants. |

