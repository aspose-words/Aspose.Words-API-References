---
title: "WatermarkerContext"
linktitle: "WatermarkerContext"
second_title: "Aspose.Words لـ Java"
description: "سياق وضع العلامات المائية للمستند في Java."
type: docs
weight: 725
url: /ar/java/com.aspose.words/watermarkercontext/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.ProcessorContext](../../com.aspose.words/processorcontext/)
```
public class WatermarkerContext extends ProcessorContext
```

سياق وضع العلامة المائية للمستند.

 **Examples:** 

يوضح كيفية إدراج نص العلامة المائية إلى المستند باستخدام السياق.

```

 String doc = getMyDir() + "Big document.docx";
 String watermarkText = "This is a watermark";

 WatermarkerContext watermarkerContext = new WatermarkerContext();
 watermarkerContext.setTextWatermark(watermarkText);

 watermarkerContext.getTextWatermarkOptions().setColor(Color.RED);

 Watermarker.create(watermarkerContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.WatermarkContextText.docx")
         .execute();
 
```

يعرض كيفية إدراج نص العلامة المائية إلى المستند من الدفق باستخدام السياق.

```

 String watermarkText = "This is a watermark";

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Document.docx")) {
     WatermarkerContext watermarkerContext = new WatermarkerContext();
     watermarkerContext.setTextWatermark(watermarkText);

     watermarkerContext.getTextWatermarkOptions().setColor(Color.RED);

     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.WatermarkContextTextStream.docx")) {
         Watermarker.create(watermarkerContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```

يعرض كيفية إدراج صورة العلامة المائية إلى المستند باستخدام السياق.

```

 String doc = getMyDir() + "Document.docx";
 String watermarkImage = getImageDir() + "Logo.jpg";

 WatermarkerContext watermarkerContext = new WatermarkerContext();
 watermarkerContext.setImageWatermark(Files.readAllBytes(Paths.get(watermarkImage)));

 watermarkerContext.getImageWatermarkOptions().setScale(50.0);

 Watermarker.create(watermarkerContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.WatermarkContextImage.docx")
         .execute();
 
```

يعرض كيفية إدراج صورة العلامة المائية إلى المستند من دفق باستخدام السياق.

```

 String watermarkImage = getImageDir() + "Logo.jpg";

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Document.docx")) {
     WatermarkerContext watermarkerContext = new WatermarkerContext();
     watermarkerContext.setImageWatermark(Files.readAllBytes(Paths.get(watermarkImage)));

     watermarkerContext.getImageWatermarkOptions().setScale(50.0);

     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.WatermarkContextImageStream.docx")) {
         Watermarker.create(watermarkerContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```
## المنشئات

| المنشئ | الوصف |
| --- | --- |
| [WatermarkerContext()](#WatermarkerContext) | يقوم بتهيئة نسخة جديدة من هذه الفئة. |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getFontSettings()](#getFontSettings) | إعدادات الخط المستخدمة بواسطة المعالج. |
| [getImageWatermark()](#getImageWatermark) | بايتات الصورة لاستخدامها كعلامة مائية. |
| [getImageWatermarkOptions()](#getImageWatermarkOptions) | خيارات العلامة المائية النصية. |
| [getLayoutOptions()](#getLayoutOptions) | خيارات تخطيط المستند المستخدمة بواسطة المعالج. |
| [getTextWatermark()](#getTextWatermark) | نص لاستخدامه كعلامة مائية. |
| [getTextWatermarkOptions()](#getTextWatermarkOptions) | خيارات العلامة المائية الصورية. |
| [getWarningCallback()](#getWarningCallback) | دالة رد النداء للتحذير المستخدمة بواسطة المعالج. |
| [setFontSettings(FontSettings value)](#setFontSettings-com.aspose.words.FontSettings) | إعدادات الخط المستخدمة بواسطة المعالج. |
| [setImageWatermark(byte[] value)](#setImageWatermark-byte) | بايتات الصورة لاستخدامها كعلامة مائية. |
| [setTextWatermark(String value)](#setTextWatermark-java.lang.String) | نص لاستخدامه كعلامة مائية. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | دالة رد النداء للتحذير المستخدمة بواسطة المعالج. |
### WatermarkerContext() {#WatermarkerContext}
```
public WatermarkerContext()
```


يقوم بتهيئة نسخة جديدة من هذه الفئة.

### getFontSettings() {#getFontSettings}
```
public FontSettings getFontSettings()
```


إعدادات الخط المستخدمة بواسطة المعالج.

**Returns:**
[FontSettings](../../com.aspose.words/fontsettings/) - The corresponding [FontSettings](../../com.aspose.words/fontsettings/) value.
### getImageWatermark() {#getImageWatermark}
```
public byte[] getImageWatermark()
```


بايتات الصورة لاستخدامها كعلامة مائية.

 **Remarks:** 

إذا تم تحديد كل من [getImageWatermark()](../../com.aspose.words/watermarkercontext/\#getImageWatermark) / [setImageWatermark(byte[])](../../com.aspose.words/watermarkercontext/\#setImageWatermark-byte) و [getTextWatermark()](../../com.aspose.words/watermarkercontext/\#getTextWatermark) / [setTextWatermark(java.lang.String)](../../com.aspose.words/watermarkercontext/\#setTextWatermark-java.lang.String) ، فإن العلامة المائية النصية تتجاوز العلامة المائية الصورية.

 **Examples:** 

يعرض كيفية إدراج صورة العلامة المائية إلى المستند باستخدام السياق.

```

 String doc = getMyDir() + "Document.docx";
 String watermarkImage = getImageDir() + "Logo.jpg";

 WatermarkerContext watermarkerContext = new WatermarkerContext();
 watermarkerContext.setImageWatermark(Files.readAllBytes(Paths.get(watermarkImage)));

 watermarkerContext.getImageWatermarkOptions().setScale(50.0);

 Watermarker.create(watermarkerContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.WatermarkContextImage.docx")
         .execute();
 
```

يعرض كيفية إدراج صورة العلامة المائية إلى المستند من دفق باستخدام السياق.

```

 String watermarkImage = getImageDir() + "Logo.jpg";

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Document.docx")) {
     WatermarkerContext watermarkerContext = new WatermarkerContext();
     watermarkerContext.setImageWatermark(Files.readAllBytes(Paths.get(watermarkImage)));

     watermarkerContext.getImageWatermarkOptions().setScale(50.0);

     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.WatermarkContextImageStream.docx")) {
         Watermarker.create(watermarkerContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```

**Returns:**
byte[] - القيمة المقابلة من نوع byte[] .
### getImageWatermarkOptions() {#getImageWatermarkOptions}
```
public ImageWatermarkOptions getImageWatermarkOptions()
```


خيارات العلامة المائية النصية.

 **Examples:** 

يعرض كيفية إدراج صورة العلامة المائية إلى المستند باستخدام السياق.

```

 String doc = getMyDir() + "Document.docx";
 String watermarkImage = getImageDir() + "Logo.jpg";

 WatermarkerContext watermarkerContext = new WatermarkerContext();
 watermarkerContext.setImageWatermark(Files.readAllBytes(Paths.get(watermarkImage)));

 watermarkerContext.getImageWatermarkOptions().setScale(50.0);

 Watermarker.create(watermarkerContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.WatermarkContextImage.docx")
         .execute();
 
```

يعرض كيفية إدراج صورة العلامة المائية إلى المستند من دفق باستخدام السياق.

```

 String watermarkImage = getImageDir() + "Logo.jpg";

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Document.docx")) {
     WatermarkerContext watermarkerContext = new WatermarkerContext();
     watermarkerContext.setImageWatermark(Files.readAllBytes(Paths.get(watermarkImage)));

     watermarkerContext.getImageWatermarkOptions().setScale(50.0);

     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.WatermarkContextImageStream.docx")) {
         Watermarker.create(watermarkerContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```

**Returns:**
[ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) - The corresponding [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) value.
### getLayoutOptions() {#getLayoutOptions}
```
public LayoutOptions getLayoutOptions()
```


خيارات تخطيط المستند المستخدمة بواسطة المعالج.

**Returns:**
[LayoutOptions](../../com.aspose.words/layoutoptions/) - The corresponding [LayoutOptions](../../com.aspose.words/layoutoptions/) value.
### getTextWatermark() {#getTextWatermark}
```
public String getTextWatermark()
```


نص لاستخدامه كعلامة مائية.

 **Remarks:** 

إذا تم تحديد كل من [getImageWatermark()](../../com.aspose.words/watermarkercontext/\#getImageWatermark) / [setImageWatermark(byte[])](../../com.aspose.words/watermarkercontext/\#setImageWatermark-byte) و [getTextWatermark()](../../com.aspose.words/watermarkercontext/\#getTextWatermark) / [setTextWatermark(java.lang.String)](../../com.aspose.words/watermarkercontext/\#setTextWatermark-java.lang.String) ، فإن العلامة المائية النصية تتجاوز العلامة المائية الصورية.

 **Examples:** 

يوضح كيفية إدراج نص العلامة المائية إلى المستند باستخدام السياق.

```

 String doc = getMyDir() + "Big document.docx";
 String watermarkText = "This is a watermark";

 WatermarkerContext watermarkerContext = new WatermarkerContext();
 watermarkerContext.setTextWatermark(watermarkText);

 watermarkerContext.getTextWatermarkOptions().setColor(Color.RED);

 Watermarker.create(watermarkerContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.WatermarkContextText.docx")
         .execute();
 
```

يعرض كيفية إدراج نص العلامة المائية إلى المستند من الدفق باستخدام السياق.

```

 String watermarkText = "This is a watermark";

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Document.docx")) {
     WatermarkerContext watermarkerContext = new WatermarkerContext();
     watermarkerContext.setTextWatermark(watermarkText);

     watermarkerContext.getTextWatermarkOptions().setColor(Color.RED);

     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.WatermarkContextTextStream.docx")) {
         Watermarker.create(watermarkerContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```

**Returns:**
java.lang.String - القيمة المقابلة من نوع java.lang.String.
### getTextWatermarkOptions() {#getTextWatermarkOptions}
```
public TextWatermarkOptions getTextWatermarkOptions()
```


خيارات العلامة المائية الصورية.

 **Examples:** 

يوضح كيفية إدراج نص العلامة المائية إلى المستند باستخدام السياق.

```

 String doc = getMyDir() + "Big document.docx";
 String watermarkText = "This is a watermark";

 WatermarkerContext watermarkerContext = new WatermarkerContext();
 watermarkerContext.setTextWatermark(watermarkText);

 watermarkerContext.getTextWatermarkOptions().setColor(Color.RED);

 Watermarker.create(watermarkerContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.WatermarkContextText.docx")
         .execute();
 
```

يعرض كيفية إدراج نص العلامة المائية إلى المستند من الدفق باستخدام السياق.

```

 String watermarkText = "This is a watermark";

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Document.docx")) {
     WatermarkerContext watermarkerContext = new WatermarkerContext();
     watermarkerContext.setTextWatermark(watermarkText);

     watermarkerContext.getTextWatermarkOptions().setColor(Color.RED);

     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.WatermarkContextTextStream.docx")) {
         Watermarker.create(watermarkerContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```

**Returns:**
[TextWatermarkOptions](../../com.aspose.words/textwatermarkoptions/) - The corresponding [TextWatermarkOptions](../../com.aspose.words/textwatermarkoptions/) value.
### getWarningCallback() {#getWarningCallback}
```
public IWarningCallback getWarningCallback()
```


دالة رد النداء للتحذير المستخدمة بواسطة المعالج.

**Returns:**
[IWarningCallback](../../com.aspose.words/iwarningcallback/) - The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback/) value.
### setFontSettings(FontSettings value) {#setFontSettings-com.aspose.words.FontSettings}
```
public void setFontSettings(FontSettings value)
```


إعدادات الخط المستخدمة بواسطة المعالج.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | [FontSettings](../../com.aspose.words/fontsettings/) | القيمة المقابلة لـ [FontSettings](../../com.aspose.words/fontsettings/). |

### setImageWatermark(byte[] value) {#setImageWatermark-byte}
```
public void setImageWatermark(byte[] value)
```


بايتات الصورة لاستخدامها كعلامة مائية.

 **Remarks:** 

إذا تم تحديد كل من [getImageWatermark()](../../com.aspose.words/watermarkercontext/\#getImageWatermark) / [setImageWatermark(byte[])](../../com.aspose.words/watermarkercontext/\#setImageWatermark-byte) و [getTextWatermark()](../../com.aspose.words/watermarkercontext/\#getTextWatermark) / [setTextWatermark(java.lang.String)](../../com.aspose.words/watermarkercontext/\#setTextWatermark-java.lang.String) ، فإن العلامة المائية النصية تتجاوز العلامة المائية الصورية.

 **Examples:** 

يعرض كيفية إدراج صورة العلامة المائية إلى المستند باستخدام السياق.

```

 String doc = getMyDir() + "Document.docx";
 String watermarkImage = getImageDir() + "Logo.jpg";

 WatermarkerContext watermarkerContext = new WatermarkerContext();
 watermarkerContext.setImageWatermark(Files.readAllBytes(Paths.get(watermarkImage)));

 watermarkerContext.getImageWatermarkOptions().setScale(50.0);

 Watermarker.create(watermarkerContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.WatermarkContextImage.docx")
         .execute();
 
```

يعرض كيفية إدراج صورة العلامة المائية إلى المستند من دفق باستخدام السياق.

```

 String watermarkImage = getImageDir() + "Logo.jpg";

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Document.docx")) {
     WatermarkerContext watermarkerContext = new WatermarkerContext();
     watermarkerContext.setImageWatermark(Files.readAllBytes(Paths.get(watermarkImage)));

     watermarkerContext.getImageWatermarkOptions().setScale(50.0);

     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.WatermarkContextImageStream.docx")) {
         Watermarker.create(watermarkerContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | byte[] | القيمة المقابلة من نوع byte[] . |

### setTextWatermark(String value) {#setTextWatermark-java.lang.String}
```
public void setTextWatermark(String value)
```


نص لاستخدامه كعلامة مائية.

 **Remarks:** 

إذا تم تحديد كل من [getImageWatermark()](../../com.aspose.words/watermarkercontext/\#getImageWatermark) / [setImageWatermark(byte[])](../../com.aspose.words/watermarkercontext/\#setImageWatermark-byte) و [getTextWatermark()](../../com.aspose.words/watermarkercontext/\#getTextWatermark) / [setTextWatermark(java.lang.String)](../../com.aspose.words/watermarkercontext/\#setTextWatermark-java.lang.String) ، فإن العلامة المائية النصية تتجاوز العلامة المائية الصورية.

 **Examples:** 

يوضح كيفية إدراج نص العلامة المائية إلى المستند باستخدام السياق.

```

 String doc = getMyDir() + "Big document.docx";
 String watermarkText = "This is a watermark";

 WatermarkerContext watermarkerContext = new WatermarkerContext();
 watermarkerContext.setTextWatermark(watermarkText);

 watermarkerContext.getTextWatermarkOptions().setColor(Color.RED);

 Watermarker.create(watermarkerContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.WatermarkContextText.docx")
         .execute();
 
```

يعرض كيفية إدراج نص العلامة المائية إلى المستند من الدفق باستخدام السياق.

```

 String watermarkText = "This is a watermark";

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Document.docx")) {
     WatermarkerContext watermarkerContext = new WatermarkerContext();
     watermarkerContext.setTextWatermark(watermarkText);

     watermarkerContext.getTextWatermarkOptions().setColor(Color.RED);

     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.WatermarkContextTextStream.docx")) {
         Watermarker.create(watermarkerContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | القيمة المقابلة من نوع java.lang.String. |

### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback}
```
public void setWarningCallback(IWarningCallback value)
```


دالة رد النداء للتحذير المستخدمة بواسطة المعالج.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback/) | القيمة المقابلة لـ [IWarningCallback](../../com.aspose.words/iwarningcallback/). |

