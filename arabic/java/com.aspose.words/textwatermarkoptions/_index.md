---
title: "TextWatermarkOptions"
linktitle: "TextWatermarkOptions"
second_title: "Aspose.Words لـ Java"
description: "يحتوي على خيارات يمكن تحديدها عند إضافة علامة مائية بنص في Java."
type: docs
weight: 678
url: /ar/java/com.aspose.words/textwatermarkoptions/
---

**Inheritance:**
java.lang.Object
```
public class TextWatermarkOptions
```

يحتوي على خيارات يمكن تحديدها عند إضافة علامة مائية بالنص.

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
| [getColor()](#getColor) | يحصل على لون الخط. |
| [getFontFamily()](#getFontFamily) | يحصل على اسم عائلة الخط. |
| [getFontSize()](#getFontSize) | يحصل على حجم الخط. |
| [getLayout()](#getLayout) | يحصل على تخطيط العلامة المائية. |
| [isSemitrasparent()](#isSemitrasparent) | يحصل على قيمة منطقية مسؤولة عن شفافية العلامة المائية. |
| [isSemitrasparent(boolean value)](#isSemitrasparent-boolean) | يضبط قيمة منطقية مسؤولة عن شفافية العلامة المائية. |
| [setColor(Color value)](#setColor-java.awt.Color) | يضبط لون الخط. |
| [setFontFamily(String value)](#setFontFamily-java.lang.String) | يضبط اسم عائلة الخط. |
| [setFontSize(float value)](#setFontSize-float) | يضبط حجم الخط. |
| [setLayout(int value)](#setLayout-int) | يضبط تخطيط العلامة المائية. |
### getColor() {#getColor}
```
public Color getColor()
```


يحصل على لون الخط. القيمة الافتراضية هي java.awt.Color\#getSilver().getSilver().

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
java.awt.Color - لون الخط.
### getFontFamily() {#getFontFamily}
```
public String getFontFamily()
```


يحصل على اسم عائلة الخط. القيمة الافتراضية هي "Calibri".

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
java.lang.String - اسم عائلة الخط.
### getFontSize() {#getFontSize}
```
public float getFontSize()
```


يحصل على حجم الخط. القيمة الافتراضية هي 0 - تلقائي.

**Returns:**
float - حجم الخط.
### getLayout() {#getLayout}
```
public int getLayout()
```


يحصل على تخطيط العلامة المائية. القيمة الافتراضية هي [WatermarkLayout.DIAGONAL](../../com.aspose.words/watermarklayout/\#DIAGONAL).

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
int - تخطيط العلامة المائية. القيمة المرجعة هي واحدة من ثوابت [WatermarkLayout](../../com.aspose.words/watermarklayout/).
### isSemitrasparent() {#isSemitrasparent}
```
public boolean isSemitrasparent()
```


يحصل على قيمة منطقية مسؤولة عن شفافية العلامة المائية. القيمة الافتراضية هي  true .

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
boolean - قيمة منطقية مسؤولة عن شفافية العلامة المائية.
### isSemitrasparent(boolean value) {#isSemitrasparent-boolean}
```
public void isSemitrasparent(boolean value)
```


يضبط قيمة منطقية مسؤولة عن شفافية العلامة المائية. القيمة الافتراضية هي  true .

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

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | قيمة منطقية مسؤولة عن شفافية العلامة المائية. |

### setColor(Color value) {#setColor-java.awt.Color}
```
public void setColor(Color value)
```


يضبط لون الخط. القيمة الافتراضية هي java.awt.Color\#getSilver().getSilver().

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

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.awt.Color | لون الخط. |

### setFontFamily(String value) {#setFontFamily-java.lang.String}
```
public void setFontFamily(String value)
```


يضبط اسم عائلة الخط. القيمة الافتراضية هي "Calibri".

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

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | اسم عائلة الخط. |

### setFontSize(float value) {#setFontSize-float}
```
public void setFontSize(float value)
```


يضبط حجم الخط. القيمة الافتراضية هي 0 - تلقائي.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | float | حجم الخط. |

### setLayout(int value) {#setLayout-int}
```
public void setLayout(int value)
```


يضبط تخطيط العلامة المائية. القيمة الافتراضية هي [WatermarkLayout.DIAGONAL](../../com.aspose.words/watermarklayout/\#DIAGONAL).

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

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | تخطيط العلامة المائية. يجب أن تكون القيمة واحدة من ثوابت [WatermarkLayout](../../com.aspose.words/watermarklayout/). |

