---
title: "علامة مائية"
linktitle: "علامة مائية"
second_title: "Aspose.Words لـ Java"
description: "يمثل الصنف للعمل مع علامة مائية للمستند في Java."
type: docs
weight: 721
url: /ar/java/com.aspose.words/watermark/
---

**Inheritance:**
java.lang.Object
```
public class Watermark
```

يمثل الفئة للعمل مع علامة مائية للمستند.

لمزيد من المعلومات، زر [ Working with Watermark ][Working with Watermark] مقالة الوثائق.

 **Examples:** 

يوضح كيفية إنشاء علامة مائية نصية.

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
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getType()](#getType) | يحصل على نوع العلامة المائية. |
| [remove()](#remove) | يزيل العلامة المائية. |
| [setImage(BufferedImage image)](#setImage-java.awt.image.BufferedImage) | يضيف علامة مائية صورة إلى المستند. |
| [setImage(BufferedImage image, ImageWatermarkOptions options)](#setImage-java.awt.image.BufferedImage-com.aspose.words.ImageWatermarkOptions) | يضيف علامة مائية صورة إلى المستند. |
| [setImage(InputStream imageStream, ImageWatermarkOptions options)](#setImage-java.io.InputStream-com.aspose.words.ImageWatermarkOptions) | يضيف علامة مائية صورة إلى المستند. |
| [setImage(String imagePath, ImageWatermarkOptions options)](#setImage-java.lang.String-com.aspose.words.ImageWatermarkOptions) | يضيف علامة مائية صورة إلى المستند. |
| [setText(String text)](#setText-java.lang.String) | يضيف علامة مائية نصية إلى المستند. |
| [setText(String text, TextWatermarkOptions options)](#setText-java.lang.String-com.aspose.words.TextWatermarkOptions) | يضيف علامة مائية نصية إلى المستند. |
### getType() {#getType}
```
public int getType()
```


يحصل على نوع العلامة المائية.

 **Examples:** 

يوضح كيفية إنشاء علامة مائية نصية.

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
int - نوع العلامة المائية. القيمة المرجعة هي واحدة من ثوابت [WatermarkType](../../com.aspose.words/watermarktype/).
### remove() {#remove}
```
public void remove()
```


يزيل العلامة المائية.

 **Examples:** 

يوضح كيفية إنشاء علامة مائية نصية.

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


يضيف علامة مائية صورة إلى المستند.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| صورة | java.awt.image.BufferedImage | الصورة التي تُعرض كعلامة مائية. |

### setImage(BufferedImage image, ImageWatermarkOptions options) {#setImage-java.awt.image.BufferedImage-com.aspose.words.ImageWatermarkOptions}
```
public void setImage(BufferedImage image, ImageWatermarkOptions options)
```


يضيف علامة مائية صورة إلى المستند.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| صورة | java.awt.image.BufferedImage | الصورة التي تُعرض كعلامة مائية. |
| options | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) | يحدد خيارات إضافية لعلامة الماء الصورية. |

### setImage(InputStream imageStream, ImageWatermarkOptions options) {#setImage-java.io.InputStream-com.aspose.words.ImageWatermarkOptions}
```
public void setImage(InputStream imageStream, ImageWatermarkOptions options)
```


يضيف علامة مائية صورة إلى المستند.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| imageStream | java.io.InputStream | الدفق الذي يحتوي على بيانات الصورة المعروضة كعلامة مائية. |
| options | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) | يحدد خيارات إضافية لعلامة الماء الصورية. |

### setImage(String imagePath, ImageWatermarkOptions options) {#setImage-java.lang.String-com.aspose.words.ImageWatermarkOptions}
```
public void setImage(String imagePath, ImageWatermarkOptions options)
```


يضيف علامة مائية صورة إلى المستند.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| imagePath | java.lang.String | المسار إلى ملف الصورة المعروض كعلامة مائية. |
| options | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) | يحدد خيارات إضافية لعلامة الماء الصورية. |

### setText(String text) {#setText-java.lang.String}
```
public void setText(String text)
```


يضيف علامة مائية نصية إلى المستند.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| نص | java.lang.String | النص الذي يُعرض كعلامة مائية. |

### setText(String text, TextWatermarkOptions options) {#setText-java.lang.String-com.aspose.words.TextWatermarkOptions}
```
public void setText(String text, TextWatermarkOptions options)
```


يضيف علامة مائية نصية إلى المستند.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| نص | java.lang.String | النص الذي يُعرض كعلامة مائية. |
| options | [TextWatermarkOptions](../../com.aspose.words/textwatermarkoptions/) | يحدد خيارات إضافية لعلامة الماء النصية. |

