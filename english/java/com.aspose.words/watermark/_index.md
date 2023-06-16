---
title: Watermark
linktitle: Watermark
second_title: Aspose.Words for Java
description: Represents class to work with document watermark in Java.
type: docs
weight: 631
url: /java/com.aspose.words/watermark/
---

**Inheritance:**
java.lang.Object
```
public class Watermark
```

Represents class to work with document watermark.

To learn more, visit the [ Working with Watermark ][Working with Watermark] documentation article.


[Working with Watermark]: https://docs.aspose.com/words/java/working-with-watermark/
## Methods

| Method | Description |
| --- | --- |
| [getType()](#getType) | Gets the watermark type. |
| [remove()](#remove) | Removes the watermark. |
| [setImage(BufferedImage image)](#setImage-java.awt.image.BufferedImage) | Adds Image watermark into the document. |
| [setImage(BufferedImage image, ImageWatermarkOptions options)](#setImage-java.awt.image.BufferedImage-com.aspose.words.ImageWatermarkOptions) | Adds Image watermark into the document. |
| [setImage(String imagePath, ImageWatermarkOptions options)](#setImage-java.lang.String-com.aspose.words.ImageWatermarkOptions) | Adds Image watermark into the document. |
| [setText(String text)](#setText-java.lang.String) | Adds Text watermark into the document. |
| [setText(String text, TextWatermarkOptions options)](#setText-java.lang.String-com.aspose.words.TextWatermarkOptions) | Adds Text watermark into the document. |
### getType() {#getType}
```
public int getType()
```


Gets the watermark type.

**Returns:**
int - The watermark type. The returned value is one of [WatermarkType](../../com.aspose.words/watermarktype/) constants.
### remove() {#remove}
```
public void remove()
```


Removes the watermark.

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

### setImage(BufferedImage image) {#setImage-java.awt.image.BufferedImage}
```
public void setImage(BufferedImage image)
```


Adds Image watermark into the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| image | java.awt.image.BufferedImage | Image that is displayed as a watermark. |

### setImage(BufferedImage image, ImageWatermarkOptions options) {#setImage-java.awt.image.BufferedImage-com.aspose.words.ImageWatermarkOptions}
```
public void setImage(BufferedImage image, ImageWatermarkOptions options)
```


Adds Image watermark into the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| image | java.awt.image.BufferedImage | Image that is displayed as a watermark. |
| options | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) | Defines additional options for the image watermark. |

### setImage(String imagePath, ImageWatermarkOptions options) {#setImage-java.lang.String-com.aspose.words.ImageWatermarkOptions}
```
public void setImage(String imagePath, ImageWatermarkOptions options)
```


Adds Image watermark into the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| imagePath | java.lang.String | Path to the image file that is displayed as a watermark. |
| options | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) | Defines additional options for the image watermark. |

### setText(String text) {#setText-java.lang.String}
```
public void setText(String text)
```


Adds Text watermark into the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| text | java.lang.String | Text that is displayed as a watermark. |

### setText(String text, TextWatermarkOptions options) {#setText-java.lang.String-com.aspose.words.TextWatermarkOptions}
```
public void setText(String text, TextWatermarkOptions options)
```


Adds Text watermark into the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| text | java.lang.String | Text that is displayed as a watermark. |
| options | [TextWatermarkOptions](../../com.aspose.words/textwatermarkoptions/) | Defines additional options for the text watermark. |

