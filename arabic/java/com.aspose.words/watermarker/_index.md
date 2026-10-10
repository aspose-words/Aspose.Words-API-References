---
title: "مُضيف العلامات المائية"
linktitle: "مُضيف العلامات المائية"
second_title: "Aspose.Words لـ Java"
description: "يوفر طرقًا مخصصة لإدراج العلامات المائية في المستندات باستخدام Java."
type: docs
weight: 724
url: /ar/java/com.aspose.words/watermarker/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Processor](../../com.aspose.words/processor/)
```
public class Watermarker extends Processor
```

يوفر طرقًا مخصصة لإدراج العلامات المائية في المستندات.
## الطرق

| طريقة | الوصف |
| --- | --- |
| [create(WatermarkerContext context)](#create-com.aspose.words.WatermarkerContext) | ينشئ مثيلًا جديدًا لمعالج العلامات المائية. |
| [execute()](#execute) | نفّذ إجراء المعالج. |
| [from(InputStream input)](#from-java.io.InputStream) | يحدد المستند الإدخالي للمعالجة. |
| [from(InputStream input, LoadOptions loadOptions)](#from-java.io.InputStream-com.aspose.words.LoadOptions) | يحدد المستند الإدخالي للمعالجة. |
| [from(String input)](#from-java.lang.String) | يحدد المستند الإدخالي للمعالجة. |
| [from(String input, LoadOptions loadOptions)](#from-java.lang.String-com.aspose.words.LoadOptions) | يحدد المستند الإدخالي للمعالجة. |
| [setImage(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, BufferedImage watermarkImage)](#setImage-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.awt.image.BufferedImage) |  |
| [setImage(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, BufferedImage watermarkImage, ImageWatermarkOptions options)](#setImage-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.awt.image.BufferedImage-com.aspose.words.ImageWatermarkOptions) |  |
| [setImage(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, InputStream watermarkImageStream)](#setImage-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.io.InputStream) |  |
| [setImage(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, InputStream watermarkImageStream, ImageWatermarkOptions options)](#setImage-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.io.InputStream-com.aspose.words.ImageWatermarkOptions) |  |
| [setImage(InputStream inputStream, OutputStream outputStream, int saveFormat, BufferedImage watermarkImage)](#setImage-java.io.InputStream-java.io.OutputStream-int-java.awt.image.BufferedImage) |  |
| [setImage(InputStream inputStream, OutputStream outputStream, int saveFormat, BufferedImage watermarkImage, ImageWatermarkOptions options)](#setImage-java.io.InputStream-java.io.OutputStream-int-java.awt.image.BufferedImage-com.aspose.words.ImageWatermarkOptions) |  |
| [setImage(InputStream inputStream, OutputStream outputStream, int saveFormat, InputStream watermarkImageStream)](#setImage-java.io.InputStream-java.io.OutputStream-int-java.io.InputStream) |  |
| [setImage(InputStream inputStream, OutputStream outputStream, int saveFormat, InputStream watermarkImageStream, ImageWatermarkOptions options)](#setImage-java.io.InputStream-java.io.OutputStream-int-java.io.InputStream-com.aspose.words.ImageWatermarkOptions) |  |
| [setImage(String inputFileName, String outputFileName, SaveOptions saveOptions, String watermarkImageFileName)](#setImage-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String) | يضيف علامة مائية صورة إلى المستند مع خيارات وتنسيق حفظ محدد. |
| [setImage(String inputFileName, String outputFileName, SaveOptions saveOptions, String watermarkImageFileName, ImageWatermarkOptions options)](#setImage-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String-com.aspose.words.ImageWatermarkOptions) | يضيف علامة مائية صورة إلى المستند مع خيارات وتنسيق حفظ محدد. |
| [setImage(String inputFileName, String outputFileName, int saveFormat, String watermarkImageFileName)](#setImage-java.lang.String-java.lang.String-int-java.lang.String) |  |
| [setImage(String inputFileName, String outputFileName, int saveFormat, String watermarkImageFileName, ImageWatermarkOptions options)](#setImage-java.lang.String-java.lang.String-int-java.lang.String-com.aspose.words.ImageWatermarkOptions) |  |
| [setImage(String inputFileName, String outputFileName, String watermarkImageFileName)](#setImage-java.lang.String-java.lang.String-java.lang.String) | يضيف علامة مائية صورة إلى المستند. |
| [setImage(String inputFileName, String outputFileName, String watermarkImageFileName, ImageWatermarkOptions options)](#setImage-java.lang.String-java.lang.String-java.lang.String-com.aspose.words.ImageWatermarkOptions) | يضيف علامة مائية صورة إلى المستند مع خيارات. |
| [setText(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, String watermarkText)](#setText-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.String) |  |
| [setText(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, String watermarkText, TextWatermarkOptions options)](#setText-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.String-com.aspose.words.TextWatermarkOptions) |  |
| [setText(InputStream inputStream, OutputStream outputStream, int saveFormat, String watermarkText)](#setText-java.io.InputStream-java.io.OutputStream-int-java.lang.String) |  |
| [setText(InputStream inputStream, OutputStream outputStream, int saveFormat, String watermarkText, TextWatermarkOptions options)](#setText-java.io.InputStream-java.io.OutputStream-int-java.lang.String-com.aspose.words.TextWatermarkOptions) |  |
| [setText(String inputFileName, String outputFileName, SaveOptions saveOptions, String watermarkText)](#setText-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String) | يضيف علامة مائية نصية إلى المستند مع خيارات وتنسيق حفظ محدد. |
| [setText(String inputFileName, String outputFileName, SaveOptions saveOptions, String watermarkText, TextWatermarkOptions options)](#setText-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String-com.aspose.words.TextWatermarkOptions) | يضيف علامة مائية نصية إلى المستند مع خيارات وتنسيق حفظ محدد. |
| [setText(String inputFileName, String outputFileName, int saveFormat, String watermarkText)](#setText-java.lang.String-java.lang.String-int-java.lang.String) |  |
| [setText(String inputFileName, String outputFileName, int saveFormat, String watermarkText, TextWatermarkOptions options)](#setText-java.lang.String-java.lang.String-int-java.lang.String-com.aspose.words.TextWatermarkOptions) |  |
| [setText(String inputFileName, String outputFileName, String watermarkText)](#setText-java.lang.String-java.lang.String-java.lang.String) | يضيف علامة مائية نصية إلى المستند. |
| [setText(String inputFileName, String outputFileName, String watermarkText, TextWatermarkOptions options)](#setText-java.lang.String-java.lang.String-java.lang.String-com.aspose.words.TextWatermarkOptions) | يضيف علامة مائية نصية إلى المستند مع خيارات. |
| [setWatermarkToImages(InputStream inputStream, ImageSaveOptions saveOptions, InputStream watermarkImageStream)](#setWatermarkToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.io.InputStream) | يضيف علامة مائية صورة إلى المستند مع خيارات. |
| [setWatermarkToImages(InputStream inputStream, ImageSaveOptions saveOptions, InputStream watermarkImageStream, ImageWatermarkOptions options)](#setWatermarkToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.io.InputStream-com.aspose.words.ImageWatermarkOptions) | يضيف علامة مائية صورة إلى المستند مع خيارات. |
| [setWatermarkToImages(InputStream inputStream, ImageSaveOptions saveOptions, String watermarkText)](#setWatermarkToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String) | يضيف علامة مائية نصية إلى المستند مع خيارات. |
| [setWatermarkToImages(InputStream inputStream, ImageSaveOptions saveOptions, String watermarkText, TextWatermarkOptions options)](#setWatermarkToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String-com.aspose.words.TextWatermarkOptions) | يضيف علامة مائية نصية إلى المستند مع خيارات. |
| [setWatermarkToImages(String inputFileName, ImageSaveOptions saveOptions, byte[] watermarkImageBytes)](#setWatermarkToImages-java.lang.String-com.aspose.words.ImageSaveOptions-byte) | يضيف علامة مائية صورة إلى المستند مع خيارات. |
| [setWatermarkToImages(String inputFileName, ImageSaveOptions saveOptions, byte[] watermarkImageBytes, ImageWatermarkOptions options)](#setWatermarkToImages-java.lang.String-com.aspose.words.ImageSaveOptions-byte---com.aspose.words.ImageWatermarkOptions) | يضيف علامة مائية صورة إلى المستند مع خيارات. |
| [setWatermarkToImages(String inputFileName, ImageSaveOptions saveOptions, String watermarkText)](#setWatermarkToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String) | يضيف علامة مائية نصية إلى المستند مع خيارات. |
| [setWatermarkToImages(String inputFileName, ImageSaveOptions saveOptions, String watermarkText, TextWatermarkOptions options)](#setWatermarkToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String-com.aspose.words.TextWatermarkOptions) | يضيف علامة مائية نصية إلى المستند مع خيارات. |
| [to(OutputStream output, SaveOptions saveOptions)](#to-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [to(OutputStream output, int saveFormat)](#to-java.io.OutputStream-int) |  |
| [to(String output)](#to-java.lang.String) | يحدد ملف الإخراج للمعالج. |
| [to(String output, SaveOptions saveOptions)](#to-java.lang.String-com.aspose.words.SaveOptions) | يحدد ملف الإخراج للمعالج. |
| [to(String output, int saveFormat)](#to-java.lang.String-int) |  |
| [to(ArrayList output, SaveOptions saveOptions)](#to-java.util.ArrayList-com.aspose.words.SaveOptions) |  |
| [to(ArrayList output, int saveFormat)](#to-java.util.ArrayList-int) |  |
| [toOutput(ArrayList output, SaveOptions saveOptions)](#toOutput-java.util.ArrayList-com.aspose.words.SaveOptions) |  |
| [toOutput(ArrayList output, int saveFormat)](#toOutput-java.util.ArrayList-int) |  |
### create(WatermarkerContext context) {#create-com.aspose.words.WatermarkerContext}
```
public static Watermarker create(WatermarkerContext context)
```


ينشئ مثيلًا جديدًا لمعالج العلامات المائية.

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

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| context | [WatermarkerContext](../../com.aspose.words/watermarkercontext/) |  |

**Returns:**
[Watermarker](../../com.aspose.words/watermarker/)
### execute() {#execute}
```
public void execute()
```


نفّذ إجراء المعالج.

 **Examples:** 

يعرض كيفية دمج المستندات في مستند إخراج واحد باستخدام السياق.

```

 //There is a several ways to merge documents:
 String inputDoc1 = getMyDir() + "Big document.docx";
 String inputDoc2 = getMyDir() + "Tables.docx";

 MergerContext mergerContext = new MergerContext();
 mergerContext.setMergeFormatMode(MergeFormatMode.KEEP_SOURCE_FORMATTING);

 Merger.create(mergerContext)
         .from(inputDoc1)
         .from(inputDoc2)
         .to(getArtifactsDir() + "LowCode.MergeContextDocuments.1.docx")
         .execute();

 LoadOptions firstLoadOptions = new LoadOptions();
 {
     firstLoadOptions.setIgnoreOleData(true);
 }
 LoadOptions secondLoadOptions = new LoadOptions();
 {
     secondLoadOptions.setIgnoreOleData(false);
 }
 Merger.create(mergerContext)
         .from(inputDoc1, firstLoadOptions)
         .from(inputDoc2, secondLoadOptions)
         .to(getArtifactsDir() + "LowCode.MergeContextDocuments.2.docx", SaveFormat.DOCX)
         .execute();

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 {
     saveOptions.setPassword("Aspose.Words");
 }
 Merger.create(mergerContext)
         .from(inputDoc1)
         .from(inputDoc2)
         .to(getArtifactsDir() + "LowCode.MergeContextDocuments.3.docx", saveOptions)
         .execute();
 
```

يعرض كيفية دمج المستندات من الدفق في مستند إخراج واحد باستخدام السياق.

```

 //There is a several ways to merge documents:
 String inputDoc1 = getMyDir() + "Big document.docx";
 String inputDoc2 = getMyDir() + "Tables.docx";

 MergerContext mergerContext = new MergerContext();
 mergerContext.setMergeFormatMode(MergeFormatMode.KEEP_SOURCE_FORMATTING);

 try (FileInputStream firstStreamIn = new FileInputStream(inputDoc1)) {
     try (FileInputStream secondStreamIn = new FileInputStream(inputDoc2)) {
         OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
         {
             saveOptions.setPassword("Aspose.Words");
         }
         try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.MergeStreamContextDocuments.1.docx")) {
             Merger.create(mergerContext)
                     .from(firstStreamIn)
                     .from(secondStreamIn)
                     .to(streamOut, saveOptions)
                     .execute();
         }

         LoadOptions firstLoadOptions = new LoadOptions();
         {
             firstLoadOptions.setIgnoreOleData(true);
         }
         LoadOptions secondLoadOptions = new LoadOptions();
         {
             secondLoadOptions.setIgnoreOleData(false);
         }
         try (FileOutputStream streamOut1 = new FileOutputStream(getArtifactsDir() + "LowCode.MergeStreamContextDocuments.2.docx")) {
             Merger.create(mergerContext)
                     .from(firstStreamIn, firstLoadOptions)
                     .from(secondStreamIn, secondLoadOptions)
                     .to(streamOut1, SaveFormat.DOCX)
                     .execute();
         }
     }
 }
 
```

يعرض كيفية تحويل المستندات بسطر واحد من الشيفرة باستخدام السياق.

```

 String doc = getMyDir() + "Big document.docx";

 ConverterContext converterContext = new ConverterContext();

 Converter.create(converterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ConvertContext.1.pdf")
         .execute();

 Converter.create(converterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ConvertContext.2.pdf", SaveFormat.RTF)
         .execute();

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 {
     saveOptions.setPassword("Aspose.Words");
 }
 LoadOptions loadOptions = new LoadOptions();
 {
     loadOptions.setIgnoreOleData(true);
 }
 Converter.create(converterContext)
         .from(doc, loadOptions)
         .to(getArtifactsDir() + "LowCode.ConvertContext.3.docx", saveOptions)
         .execute();

 Converter.create(converterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ConvertContext.4.png", new ImageSaveOptions(SaveFormat.PNG))
         .execute();
 
```

يعرض كيفية تحويل المستندات من الدفق بسطر واحد من الشيفرة باستخدام السياق.

```

 String doc = getMyDir() + "Document.docx";
 ConverterContext converterContext = new ConverterContext();

 try (FileInputStream streamIn = new FileInputStream(doc)) {
     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.ConvertContextStream.1.docx")) {
         Converter.create(converterContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.RTF)
                 .execute();
     }

     OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
     {
         saveOptions.setPassword("Aspose.Words");
     }
     LoadOptions loadOptions = new LoadOptions();
     {
         loadOptions.setIgnoreOleData(true);
     }
     try (FileOutputStream streamOut1 = new FileOutputStream(getArtifactsDir() + "LowCode.ConvertContextStream.2.docx")) {
         Converter.create(converterContext)
                 .from(streamIn, loadOptions)
                 .to(streamOut1, saveOptions)
                 .execute();
     }
 }
 
```

### from(InputStream input) {#from-java.io.InputStream}
```
public Processor from(InputStream input)
```


يحدد المستند الإدخالي للمعالجة.

 **Remarks:** 

إذا كان المعالج يقبل ملفًا واحدًا فقط كإدخال، فسيتم معالجة الملف الأخير المحدد فقط. معالج [Merger](../../com.aspose.words/merger/) يقبل ملفات متعددة كإدخال، وبالتالي سيتم دمج جميع المستندات المحددة. معالج [Converter](../../com.aspose.words/converter/) يقبل ملفًا واحدًا فقط كإدخال، لذا سيتم تحويل الملف الأخير المحدد فقط.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| إدخال | java.io.InputStream | دفق مستند الإدخال. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file stream.
### from(InputStream input, LoadOptions loadOptions) {#from-java.io.InputStream-com.aspose.words.LoadOptions}
```
public Processor from(InputStream input, LoadOptions loadOptions)
```


يحدد المستند الإدخالي للمعالجة.

 **Remarks:** 

إذا كان المعالج يقبل ملفًا واحدًا فقط كإدخال، فسيتم معالجة الملف الأخير المحدد فقط. معالج [Merger](../../com.aspose.words/merger/) يقبل ملفات متعددة كإدخال، وبالتالي سيتم دمج جميع المستندات المحددة. معالج [Converter](../../com.aspose.words/converter/) يقبل ملفًا واحدًا فقط كإدخال، لذا سيتم تحويل الملف الأخير المحدد فقط.

 **Examples:** 

يعرض كيفية دمج المستندات من الدفق في مستند إخراج واحد باستخدام السياق.

```

 //There is a several ways to merge documents:
 String inputDoc1 = getMyDir() + "Big document.docx";
 String inputDoc2 = getMyDir() + "Tables.docx";

 MergerContext mergerContext = new MergerContext();
 mergerContext.setMergeFormatMode(MergeFormatMode.KEEP_SOURCE_FORMATTING);

 try (FileInputStream firstStreamIn = new FileInputStream(inputDoc1)) {
     try (FileInputStream secondStreamIn = new FileInputStream(inputDoc2)) {
         OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
         {
             saveOptions.setPassword("Aspose.Words");
         }
         try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.MergeStreamContextDocuments.1.docx")) {
             Merger.create(mergerContext)
                     .from(firstStreamIn)
                     .from(secondStreamIn)
                     .to(streamOut, saveOptions)
                     .execute();
         }

         LoadOptions firstLoadOptions = new LoadOptions();
         {
             firstLoadOptions.setIgnoreOleData(true);
         }
         LoadOptions secondLoadOptions = new LoadOptions();
         {
             secondLoadOptions.setIgnoreOleData(false);
         }
         try (FileOutputStream streamOut1 = new FileOutputStream(getArtifactsDir() + "LowCode.MergeStreamContextDocuments.2.docx")) {
             Merger.create(mergerContext)
                     .from(firstStreamIn, firstLoadOptions)
                     .from(secondStreamIn, secondLoadOptions)
                     .to(streamOut1, SaveFormat.DOCX)
                     .execute();
         }
     }
 }
 
```

يعرض كيفية تحويل المستندات من الدفق بسطر واحد من الشيفرة باستخدام السياق.

```

 String doc = getMyDir() + "Document.docx";
 ConverterContext converterContext = new ConverterContext();

 try (FileInputStream streamIn = new FileInputStream(doc)) {
     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.ConvertContextStream.1.docx")) {
         Converter.create(converterContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.RTF)
                 .execute();
     }

     OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
     {
         saveOptions.setPassword("Aspose.Words");
     }
     LoadOptions loadOptions = new LoadOptions();
     {
         loadOptions.setIgnoreOleData(true);
     }
     try (FileOutputStream streamOut1 = new FileOutputStream(getArtifactsDir() + "LowCode.ConvertContextStream.2.docx")) {
         Converter.create(converterContext)
                 .from(streamIn, loadOptions)
                 .to(streamOut1, saveOptions)
                 .execute();
     }
 }
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| إدخال | java.io.InputStream | دفق مستند الإدخال. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | خيارات التحميل الاختيارية المستخدمة لتحميل المستند. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file stream.
### from(String input) {#from-java.lang.String}
```
public Processor from(String input)
```


يحدد المستند الإدخالي للمعالجة.

 **Remarks:** 

إذا كان المعالج يقبل ملفًا واحدًا فقط كإدخال، فسيتم معالجة الملف الأخير المحدد فقط. معالج [Merger](../../com.aspose.words/merger/) يقبل ملفات متعددة كإدخال، وبالتالي سيتم دمج جميع المستندات المحددة. معالج [Converter](../../com.aspose.words/converter/) يقبل ملفًا واحدًا فقط كإدخال، لذا سيتم تحويل الملف الأخير المحدد فقط.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| إدخال | java.lang.String | اسم ملف مستند الإدخال. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file.
### from(String input, LoadOptions loadOptions) {#from-java.lang.String-com.aspose.words.LoadOptions}
```
public Processor from(String input, LoadOptions loadOptions)
```


يحدد المستند الإدخالي للمعالجة.

 **Remarks:** 

إذا كان المعالج يقبل ملفًا واحدًا فقط كإدخال، فسيتم معالجة الملف الأخير المحدد فقط. معالج [Merger](../../com.aspose.words/merger/) يقبل ملفات متعددة كإدخال، وبالتالي سيتم دمج جميع المستندات المحددة. معالج [Converter](../../com.aspose.words/converter/) يقبل ملفًا واحدًا فقط كإدخال، لذا سيتم تحويل الملف الأخير المحدد فقط.

 **Examples:** 

يعرض كيفية دمج المستندات في مستند إخراج واحد باستخدام السياق.

```

 //There is a several ways to merge documents:
 String inputDoc1 = getMyDir() + "Big document.docx";
 String inputDoc2 = getMyDir() + "Tables.docx";

 MergerContext mergerContext = new MergerContext();
 mergerContext.setMergeFormatMode(MergeFormatMode.KEEP_SOURCE_FORMATTING);

 Merger.create(mergerContext)
         .from(inputDoc1)
         .from(inputDoc2)
         .to(getArtifactsDir() + "LowCode.MergeContextDocuments.1.docx")
         .execute();

 LoadOptions firstLoadOptions = new LoadOptions();
 {
     firstLoadOptions.setIgnoreOleData(true);
 }
 LoadOptions secondLoadOptions = new LoadOptions();
 {
     secondLoadOptions.setIgnoreOleData(false);
 }
 Merger.create(mergerContext)
         .from(inputDoc1, firstLoadOptions)
         .from(inputDoc2, secondLoadOptions)
         .to(getArtifactsDir() + "LowCode.MergeContextDocuments.2.docx", SaveFormat.DOCX)
         .execute();

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 {
     saveOptions.setPassword("Aspose.Words");
 }
 Merger.create(mergerContext)
         .from(inputDoc1)
         .from(inputDoc2)
         .to(getArtifactsDir() + "LowCode.MergeContextDocuments.3.docx", saveOptions)
         .execute();
 
```

يعرض كيفية تحويل المستندات بسطر واحد من الشيفرة باستخدام السياق.

```

 String doc = getMyDir() + "Big document.docx";

 ConverterContext converterContext = new ConverterContext();

 Converter.create(converterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ConvertContext.1.pdf")
         .execute();

 Converter.create(converterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ConvertContext.2.pdf", SaveFormat.RTF)
         .execute();

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 {
     saveOptions.setPassword("Aspose.Words");
 }
 LoadOptions loadOptions = new LoadOptions();
 {
     loadOptions.setIgnoreOleData(true);
 }
 Converter.create(converterContext)
         .from(doc, loadOptions)
         .to(getArtifactsDir() + "LowCode.ConvertContext.3.docx", saveOptions)
         .execute();

 Converter.create(converterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ConvertContext.4.png", new ImageSaveOptions(SaveFormat.PNG))
         .execute();
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| إدخال | java.lang.String | اسم ملف مستند الإدخال. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | خيارات التحميل الاختيارية المستخدمة لتحميل المستند. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file.
### setImage(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, BufferedImage watermarkImage) {#setImage-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.awt.image.BufferedImage}
```
public static void setImage(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, BufferedImage watermarkImage)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| watermarkImage | java.awt.image.BufferedImage |  |

### setImage(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, BufferedImage watermarkImage, ImageWatermarkOptions options) {#setImage-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.awt.image.BufferedImage-com.aspose.words.ImageWatermarkOptions}
```
public static void setImage(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, BufferedImage watermarkImage, ImageWatermarkOptions options)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| watermarkImage | java.awt.image.BufferedImage |  |
| options | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) |  |

### setImage(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, InputStream watermarkImageStream) {#setImage-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.io.InputStream}
```
public static void setImage(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, InputStream watermarkImageStream)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| watermarkImageStream | java.io.InputStream |  |

### setImage(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, InputStream watermarkImageStream, ImageWatermarkOptions options) {#setImage-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.io.InputStream-com.aspose.words.ImageWatermarkOptions}
```
public static void setImage(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, InputStream watermarkImageStream, ImageWatermarkOptions options)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| watermarkImageStream | java.io.InputStream |  |
| options | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) |  |

### setImage(InputStream inputStream, OutputStream outputStream, int saveFormat, BufferedImage watermarkImage) {#setImage-java.io.InputStream-java.io.OutputStream-int-java.awt.image.BufferedImage}
```
public static void setImage(InputStream inputStream, OutputStream outputStream, int saveFormat, BufferedImage watermarkImage)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| watermarkImage | java.awt.image.BufferedImage |  |

### setImage(InputStream inputStream, OutputStream outputStream, int saveFormat, BufferedImage watermarkImage, ImageWatermarkOptions options) {#setImage-java.io.InputStream-java.io.OutputStream-int-java.awt.image.BufferedImage-com.aspose.words.ImageWatermarkOptions}
```
public static void setImage(InputStream inputStream, OutputStream outputStream, int saveFormat, BufferedImage watermarkImage, ImageWatermarkOptions options)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| watermarkImage | java.awt.image.BufferedImage |  |
| options | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) |  |

### setImage(InputStream inputStream, OutputStream outputStream, int saveFormat, InputStream watermarkImageStream) {#setImage-java.io.InputStream-java.io.OutputStream-int-java.io.InputStream}
```
public static void setImage(InputStream inputStream, OutputStream outputStream, int saveFormat, InputStream watermarkImageStream)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| watermarkImageStream | java.io.InputStream |  |

### setImage(InputStream inputStream, OutputStream outputStream, int saveFormat, InputStream watermarkImageStream, ImageWatermarkOptions options) {#setImage-java.io.InputStream-java.io.OutputStream-int-java.io.InputStream-com.aspose.words.ImageWatermarkOptions}
```
public static void setImage(InputStream inputStream, OutputStream outputStream, int saveFormat, InputStream watermarkImageStream, ImageWatermarkOptions options)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| watermarkImageStream | java.io.InputStream |  |
| options | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) |  |

### setImage(String inputFileName, String outputFileName, SaveOptions saveOptions, String watermarkImageFileName) {#setImage-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String}
```
public static void setImage(String inputFileName, String outputFileName, SaveOptions saveOptions, String watermarkImageFileName)
```


يضيف علامة مائية صورة إلى المستند مع خيارات وتنسيق حفظ محدد.

 **Remarks:** 

إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ كل صفحة من الإخراج كملف منفصل. سيُستخدم اسم ملف الإخراج المحدد لتوليد أسماء الملفات لكل جزء وفق القاعدة: outputFile\_partIndex.extension.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFileName | java.lang.String | اسم ملف الإدخال. |
| outputFileName | java.lang.String | اسم ملف الإخراج. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | خيارات الحفظ. |
| watermarkImageFileName | java.lang.String | الصورة التي تُعرض كعلامة مائية. |

### setImage(String inputFileName, String outputFileName, SaveOptions saveOptions, String watermarkImageFileName, ImageWatermarkOptions options) {#setImage-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String-com.aspose.words.ImageWatermarkOptions}
```
public static void setImage(String inputFileName, String outputFileName, SaveOptions saveOptions, String watermarkImageFileName, ImageWatermarkOptions options)
```


يضيف علامة مائية صورة إلى المستند مع خيارات وتنسيق حفظ محدد.

 **Remarks:** 

إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ كل صفحة من الإخراج كملف منفصل. سيُستخدم اسم ملف الإخراج المحدد لتوليد أسماء الملفات لكل جزء وفق القاعدة: outputFile\_partIndex.extension.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFileName | java.lang.String | اسم ملف الإدخال. |
| outputFileName | java.lang.String | اسم ملف الإخراج. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | خيارات الحفظ. |
| watermarkImageFileName | java.lang.String | الصورة التي تُعرض كعلامة مائية. |
| options | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) | يحدد خيارات إضافية لعلامة الماء الصورية. |

### setImage(String inputFileName, String outputFileName, int saveFormat, String watermarkImageFileName) {#setImage-java.lang.String-java.lang.String-int-java.lang.String}
```
public static void setImage(String inputFileName, String outputFileName, int saveFormat, String watermarkImageFileName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| watermarkImageFileName | java.lang.String |  |

### setImage(String inputFileName, String outputFileName, int saveFormat, String watermarkImageFileName, ImageWatermarkOptions options) {#setImage-java.lang.String-java.lang.String-int-java.lang.String-com.aspose.words.ImageWatermarkOptions}
```
public static void setImage(String inputFileName, String outputFileName, int saveFormat, String watermarkImageFileName, ImageWatermarkOptions options)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| watermarkImageFileName | java.lang.String |  |
| options | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) |  |

### setImage(String inputFileName, String outputFileName, String watermarkImageFileName) {#setImage-java.lang.String-java.lang.String-java.lang.String}
```
public static void setImage(String inputFileName, String outputFileName, String watermarkImageFileName)
```


يضيف علامة مائية صورة إلى المستند.

 **Remarks:** 

إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ كل صفحة من الإخراج كملف منفصل. سيُستخدم اسم ملف الإخراج المحدد لتوليد أسماء الملفات لكل جزء وفق القاعدة: outputFile\_partIndex.extension.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFileName | java.lang.String | اسم ملف الإدخال. |
| outputFileName | java.lang.String | اسم ملف الإخراج. |
| watermarkImageFileName | java.lang.String | الصورة التي تُعرض كعلامة مائية. |

### setImage(String inputFileName, String outputFileName, String watermarkImageFileName, ImageWatermarkOptions options) {#setImage-java.lang.String-java.lang.String-java.lang.String-com.aspose.words.ImageWatermarkOptions}
```
public static void setImage(String inputFileName, String outputFileName, String watermarkImageFileName, ImageWatermarkOptions options)
```


يضيف علامة مائية صورة إلى المستند مع خيارات.

 **Remarks:** 

إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ كل صفحة من الإخراج كملف منفصل. سيُستخدم اسم ملف الإخراج المحدد لتوليد أسماء الملفات لكل جزء وفق القاعدة: outputFile\_partIndex.extension.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد.

 **Examples:** 

يعرض كيفية إدراج صورة العلامة المائية إلى المستند.

```

 String doc = getMyDir() + "Document.docx";
 String watermarkImage = getImageDir() + "Logo.jpg";

 Watermarker.setImage(doc, getArtifactsDir() + "LowCode.SetWatermarkImage.1.docx", watermarkImage);
 Watermarker.setImage(doc, getArtifactsDir() + "LowCode.SetWatermarkText.2.docx", SaveFormat.DOCX, watermarkImage);
 ImageWatermarkOptions options = new ImageWatermarkOptions();
 options.setScale(50.0);
 Watermarker.setImage(doc, getArtifactsDir() + "LowCode.SetWatermarkText.3.docx", watermarkImage, options);
 Watermarker.setImage(doc, getArtifactsDir() + "LowCode.SetWatermarkText.4.docx", SaveFormat.DOCX, watermarkImage, options);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFileName | java.lang.String | اسم ملف الإدخال. |
| outputFileName | java.lang.String | اسم ملف الإخراج. |
| watermarkImageFileName | java.lang.String | الصورة التي تُعرض كعلامة مائية. |
| options | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) | يحدد خيارات إضافية لعلامة الماء الصورية. |

### setText(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, String watermarkText) {#setText-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.String}
```
public static void setText(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, String watermarkText)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| watermarkText | java.lang.String |  |

### setText(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, String watermarkText, TextWatermarkOptions options) {#setText-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.String-com.aspose.words.TextWatermarkOptions}
```
public static void setText(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, String watermarkText, TextWatermarkOptions options)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| watermarkText | java.lang.String |  |
| options | [TextWatermarkOptions](../../com.aspose.words/textwatermarkoptions/) |  |

### setText(InputStream inputStream, OutputStream outputStream, int saveFormat, String watermarkText) {#setText-java.io.InputStream-java.io.OutputStream-int-java.lang.String}
```
public static void setText(InputStream inputStream, OutputStream outputStream, int saveFormat, String watermarkText)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| watermarkText | java.lang.String |  |

### setText(InputStream inputStream, OutputStream outputStream, int saveFormat, String watermarkText, TextWatermarkOptions options) {#setText-java.io.InputStream-java.io.OutputStream-int-java.lang.String-com.aspose.words.TextWatermarkOptions}
```
public static void setText(InputStream inputStream, OutputStream outputStream, int saveFormat, String watermarkText, TextWatermarkOptions options)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| watermarkText | java.lang.String |  |
| options | [TextWatermarkOptions](../../com.aspose.words/textwatermarkoptions/) |  |

### setText(String inputFileName, String outputFileName, SaveOptions saveOptions, String watermarkText) {#setText-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String}
```
public static void setText(String inputFileName, String outputFileName, SaveOptions saveOptions, String watermarkText)
```


يضيف علامة مائية نصية إلى المستند مع خيارات وتنسيق حفظ محدد.

 **Remarks:** 

إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ كل صفحة من الإخراج كملف منفصل. سيُستخدم اسم ملف الإخراج المحدد لتوليد أسماء الملفات لكل جزء وفق القاعدة: outputFile\_partIndex.extension.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFileName | java.lang.String | اسم ملف الإدخال. |
| outputFileName | java.lang.String | اسم ملف الإخراج. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | خيارات الحفظ. |
| watermarkText | java.lang.String | النص الذي يُعرض كعلامة مائية. |

### setText(String inputFileName, String outputFileName, SaveOptions saveOptions, String watermarkText, TextWatermarkOptions options) {#setText-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String-com.aspose.words.TextWatermarkOptions}
```
public static void setText(String inputFileName, String outputFileName, SaveOptions saveOptions, String watermarkText, TextWatermarkOptions options)
```


يضيف علامة مائية نصية إلى المستند مع خيارات وتنسيق حفظ محدد.

 **Remarks:** 

إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ كل صفحة من الإخراج كملف منفصل. سيُستخدم اسم ملف الإخراج المحدد لتوليد أسماء الملفات لكل جزء وفق القاعدة: outputFile\_partIndex.extension.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFileName | java.lang.String | اسم ملف الإدخال. |
| outputFileName | java.lang.String | اسم ملف الإخراج. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | خيارات الحفظ. |
| watermarkText | java.lang.String | النص الذي يُعرض كعلامة مائية. |
| options | [TextWatermarkOptions](../../com.aspose.words/textwatermarkoptions/) | يحدد خيارات إضافية لعلامة الماء النصية. |

### setText(String inputFileName, String outputFileName, int saveFormat, String watermarkText) {#setText-java.lang.String-java.lang.String-int-java.lang.String}
```
public static void setText(String inputFileName, String outputFileName, int saveFormat, String watermarkText)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| watermarkText | java.lang.String |  |

### setText(String inputFileName, String outputFileName, int saveFormat, String watermarkText, TextWatermarkOptions options) {#setText-java.lang.String-java.lang.String-int-java.lang.String-com.aspose.words.TextWatermarkOptions}
```
public static void setText(String inputFileName, String outputFileName, int saveFormat, String watermarkText, TextWatermarkOptions options)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| watermarkText | java.lang.String |  |
| options | [TextWatermarkOptions](../../com.aspose.words/textwatermarkoptions/) |  |

### setText(String inputFileName, String outputFileName, String watermarkText) {#setText-java.lang.String-java.lang.String-java.lang.String}
```
public static void setText(String inputFileName, String outputFileName, String watermarkText)
```


يضيف علامة مائية نصية إلى المستند.

 **Remarks:** 

إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ كل صفحة من الإخراج كملف منفصل. سيُستخدم اسم ملف الإخراج المحدد لتوليد أسماء الملفات لكل جزء وفق القاعدة: outputFile\_partIndex.extension.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFileName | java.lang.String | اسم ملف الإدخال. |
| outputFileName | java.lang.String | اسم ملف الإخراج. |
| watermarkText | java.lang.String | النص الذي يُعرض كعلامة مائية. |

### setText(String inputFileName, String outputFileName, String watermarkText, TextWatermarkOptions options) {#setText-java.lang.String-java.lang.String-java.lang.String-com.aspose.words.TextWatermarkOptions}
```
public static void setText(String inputFileName, String outputFileName, String watermarkText, TextWatermarkOptions options)
```


يضيف علامة مائية نصية إلى المستند مع خيارات.

 **Remarks:** 

إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ كل صفحة من الإخراج كملف منفصل. سيُستخدم اسم ملف الإخراج المحدد لتوليد أسماء الملفات لكل جزء وفق القاعدة: outputFile\_partIndex.extension.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد.

 **Examples:** 

يعرض كيفية إدراج نص العلامة المائية إلى المستند.

```

 String doc = getMyDir() + "Big document.docx";
 String watermarkText = "This is a watermark";

 Watermarker.setText(doc, getArtifactsDir() + "LowCode.WatermarkText.1.docx", watermarkText);
 Watermarker.setText(doc, getArtifactsDir() + "LowCode.WatermarkText.2.docx", SaveFormat.DOCX, watermarkText);
 TextWatermarkOptions options = new TextWatermarkOptions();
 options.setColor(Color.RED);
 Watermarker.setText(doc, getArtifactsDir() + "LowCode.WatermarkText.3.docx", watermarkText, options);
 Watermarker.setText(doc, getArtifactsDir() + "LowCode.WatermarkText.4.docx", SaveFormat.DOCX, watermarkText, options);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFileName | java.lang.String | اسم ملف الإدخال. |
| outputFileName | java.lang.String | اسم ملف الإخراج. |
| watermarkText | java.lang.String | النص الذي يُعرض كعلامة مائية. |
| options | [TextWatermarkOptions](../../com.aspose.words/textwatermarkoptions/) | يحدد خيارات إضافية لعلامة الماء النصية. |

### setWatermarkToImages(InputStream inputStream, ImageSaveOptions saveOptions, InputStream watermarkImageStream) {#setWatermarkToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.io.InputStream}
```
public static OutputStream[] setWatermarkToImages(InputStream inputStream, ImageSaveOptions saveOptions, InputStream watermarkImageStream)
```


يضيف علامة مائية صورية إلى المستند مع الخيارات. يُعيد إنتاج المخرجات كصور.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputStream | java.io.InputStream | دفق الإدخال. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | خيارات الحفظ. |
| watermarkImageStream | java.io.InputStream | دفق الصورة الذي يُعرض كعلامة مائية. |

**Returns:**
java.io.OutputStream[]
### setWatermarkToImages(InputStream inputStream, ImageSaveOptions saveOptions, InputStream watermarkImageStream, ImageWatermarkOptions options) {#setWatermarkToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.io.InputStream-com.aspose.words.ImageWatermarkOptions}
```
public static OutputStream[] setWatermarkToImages(InputStream inputStream, ImageSaveOptions saveOptions, InputStream watermarkImageStream, ImageWatermarkOptions options)
```


يضيف علامة مائية صورية إلى المستند مع الخيارات. يُعيد إنتاج المخرجات كصور.

 **Examples:** 

يعرض كيفية إدراج صورة العلامة المائية إلى المستند من دفق وحفظ النتيجة كصور.

```

 String watermarkImage = getImageDir() + "Logo.jpg";

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Document.docx")) {
     try (FileInputStream imageStream = new FileInputStream(watermarkImage)) {
         Watermarker.setWatermarkToImages(streamIn, new ImageSaveOptions(SaveFormat.PNG), imageStream);
         ImageWatermarkOptions options = new ImageWatermarkOptions();
         options.setScale(50.0);
         Watermarker.setWatermarkToImages(streamIn, new ImageSaveOptions(SaveFormat.PNG), imageStream, options);
     }
 }
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputStream | java.io.InputStream | دفق الإدخال. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | خيارات الحفظ. |
| watermarkImageStream | java.io.InputStream | دفق الصورة الذي يُعرض كعلامة مائية. |
| options | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) | يحدد خيارات إضافية لعلامة الماء الصورية. |

**Returns:**
java.io.OutputStream[]
### setWatermarkToImages(InputStream inputStream, ImageSaveOptions saveOptions, String watermarkText) {#setWatermarkToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String}
```
public static OutputStream[] setWatermarkToImages(InputStream inputStream, ImageSaveOptions saveOptions, String watermarkText)
```


يضيف علامة مائية نصية إلى المستند مع الخيارات. يُعيد إنتاج المخرجات كصور.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputStream | java.io.InputStream | دفق ملف الإدخال. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | خيارات الحفظ. |
| watermarkText | java.lang.String | النص الذي يُعرض كعلامة مائية. |

**Returns:**
java.io.OutputStream[]
### setWatermarkToImages(InputStream inputStream, ImageSaveOptions saveOptions, String watermarkText, TextWatermarkOptions options) {#setWatermarkToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String-com.aspose.words.TextWatermarkOptions}
```
public static OutputStream[] setWatermarkToImages(InputStream inputStream, ImageSaveOptions saveOptions, String watermarkText, TextWatermarkOptions options)
```


يضيف علامة مائية نصية إلى المستند مع الخيارات. يُعيد إنتاج المخرجات كصور.

 **Examples:** 

يعرض كيفية إدراج نص العلامة المائية إلى المستند من الدفق وحفظ النتيجة كصور.

```

 String watermarkText = "This is a watermark";

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Document.docx")) {
     OutputStream[] images = Watermarker.setWatermarkToImages(streamIn, new ImageSaveOptions(SaveFormat.PNG), watermarkText);

     TextWatermarkOptions watermarkOptions = new TextWatermarkOptions();
     watermarkOptions.setColor(Color.RED);
     images = Watermarker.setWatermarkToImages(streamIn, new ImageSaveOptions(SaveFormat.PNG), watermarkText, watermarkOptions);
 }
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputStream | java.io.InputStream | دفق ملف الإدخال. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | خيارات الحفظ. |
| watermarkText | java.lang.String | النص الذي يُعرض كعلامة مائية. |
| options | [TextWatermarkOptions](../../com.aspose.words/textwatermarkoptions/) | يحدد خيارات إضافية لعلامة الماء النصية. |

**Returns:**
java.io.OutputStream[]
### setWatermarkToImages(String inputFileName, ImageSaveOptions saveOptions, byte[] watermarkImageBytes) {#setWatermarkToImages-java.lang.String-com.aspose.words.ImageSaveOptions-byte}
```
public static OutputStream[] setWatermarkToImages(String inputFileName, ImageSaveOptions saveOptions, byte[] watermarkImageBytes)
```


يضيف علامة مائية صورية إلى المستند مع الخيارات. يُعيد إنتاج المخرجات كصور.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFileName | java.lang.String | اسم ملف الإدخال. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | خيارات الحفظ. |
| watermarkImageBytes | byte[] | بايتات الصورة التي تُعرض كعلامة مائية. |

**Returns:**
java.io.OutputStream[]
### setWatermarkToImages(String inputFileName, ImageSaveOptions saveOptions, byte[] watermarkImageBytes, ImageWatermarkOptions options) {#setWatermarkToImages-java.lang.String-com.aspose.words.ImageSaveOptions-byte---com.aspose.words.ImageWatermarkOptions}
```
public static OutputStream[] setWatermarkToImages(String inputFileName, ImageSaveOptions saveOptions, byte[] watermarkImageBytes, ImageWatermarkOptions options)
```


يضيف علامة مائية صورية إلى المستند مع الخيارات. يُعيد إنتاج المخرجات كصور.

 **Examples:** 

يعرض كيفية إدراج صورة العلامة المائية إلى المستند وحفظ النتيجة كصور.

```

 String doc = getMyDir() + "Document.docx";
 String watermarkImage = getImageDir() + "Logo.jpg";
 Path watermarkImagePath = Paths.get(watermarkImage);

 Watermarker.setWatermarkToImages(doc, new ImageSaveOptions(SaveFormat.PNG), Files.readAllBytes(watermarkImagePath));

 ImageWatermarkOptions options = new ImageWatermarkOptions();
 options.setScale(50.0);
 Watermarker.setWatermarkToImages(doc, new ImageSaveOptions(SaveFormat.PNG), Files.readAllBytes(watermarkImagePath), options);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFileName | java.lang.String | اسم ملف الإدخال. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | خيارات الحفظ. |
| watermarkImageBytes | byte[] | بايتات الصورة التي تُعرض كعلامة مائية. |
| options | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) | يحدد خيارات إضافية لعلامة الماء الصورية. |

**Returns:**
java.io.OutputStream[]
### setWatermarkToImages(String inputFileName, ImageSaveOptions saveOptions, String watermarkText) {#setWatermarkToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String}
```
public static OutputStream[] setWatermarkToImages(String inputFileName, ImageSaveOptions saveOptions, String watermarkText)
```


يضيف علامة مائية نصية إلى المستند مع الخيارات. يُعيد إنتاج المخرجات كصور.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFileName | java.lang.String | اسم ملف الإدخال. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | خيارات الحفظ. |
| watermarkText | java.lang.String | النص الذي يُعرض كعلامة مائية. |

**Returns:**
java.io.OutputStream[]
### setWatermarkToImages(String inputFileName, ImageSaveOptions saveOptions, String watermarkText, TextWatermarkOptions options) {#setWatermarkToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String-com.aspose.words.TextWatermarkOptions}
```
public static OutputStream[] setWatermarkToImages(String inputFileName, ImageSaveOptions saveOptions, String watermarkText, TextWatermarkOptions options)
```


يضيف علامة مائية نصية إلى المستند مع الخيارات. يُعيد إنتاج المخرجات كصور.

 **Examples:** 

يعرض كيفية إدراج نص العلامة المائية إلى المستند وحفظ النتيجة كصور.

```

 String doc = getMyDir() + "Big document.docx";
 String watermarkText = "This is a watermark";

 OutputStream[] images = Watermarker.setWatermarkToImages(doc, new ImageSaveOptions(SaveFormat.PNG), watermarkText);

 TextWatermarkOptions watermarkOptions = new TextWatermarkOptions();
 watermarkOptions.setColor(Color.RED);
 images = Watermarker.setWatermarkToImages(doc, new ImageSaveOptions(SaveFormat.PNG), watermarkText, watermarkOptions);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFileName | java.lang.String | اسم ملف الإدخال. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | خيارات الحفظ. |
| watermarkText | java.lang.String | النص الذي يُعرض كعلامة مائية. |
| options | [TextWatermarkOptions](../../com.aspose.words/textwatermarkoptions/) | يحدد خيارات إضافية لعلامة الماء النصية. |

**Returns:**
java.io.OutputStream[]
### to(OutputStream output, SaveOptions saveOptions) {#to-java.io.OutputStream-com.aspose.words.SaveOptions}
```
public Processor to(OutputStream output, SaveOptions saveOptions)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| إخراج | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(OutputStream output, int saveFormat) {#to-java.io.OutputStream-int}
```
public Processor to(OutputStream output, int saveFormat)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| إخراج | java.io.OutputStream |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(String output) {#to-java.lang.String}
```
public Processor to(String output)
```


يحدد ملف الإخراج للمعالج.

 **Remarks:** 

إذا كان الإخراج يتكون من ملفات متعددة، يتم استخدام اسم ملف الإخراج المحدد لتوليد اسم الملف لكل جزء وفق القاعدة: 'outputFile\_partIndex.extension'.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| إخراج | java.lang.String | اسم ملف الإخراج. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified output file.
### to(String output, SaveOptions saveOptions) {#to-java.lang.String-com.aspose.words.SaveOptions}
```
public Processor to(String output, SaveOptions saveOptions)
```


يحدد ملف الإخراج للمعالج.

 **Remarks:** 

إذا كان الإخراج يتكون من ملفات متعددة، يتم استخدام اسم ملف الإخراج المحدد لتوليد اسم الملف لكل جزء وفق القاعدة: 'outputFile\_partIndex.extension'.

 **Examples:** 

يعرض كيفية دمج المستندات في مستند إخراج واحد باستخدام السياق.

```

 //There is a several ways to merge documents:
 String inputDoc1 = getMyDir() + "Big document.docx";
 String inputDoc2 = getMyDir() + "Tables.docx";

 MergerContext mergerContext = new MergerContext();
 mergerContext.setMergeFormatMode(MergeFormatMode.KEEP_SOURCE_FORMATTING);

 Merger.create(mergerContext)
         .from(inputDoc1)
         .from(inputDoc2)
         .to(getArtifactsDir() + "LowCode.MergeContextDocuments.1.docx")
         .execute();

 LoadOptions firstLoadOptions = new LoadOptions();
 {
     firstLoadOptions.setIgnoreOleData(true);
 }
 LoadOptions secondLoadOptions = new LoadOptions();
 {
     secondLoadOptions.setIgnoreOleData(false);
 }
 Merger.create(mergerContext)
         .from(inputDoc1, firstLoadOptions)
         .from(inputDoc2, secondLoadOptions)
         .to(getArtifactsDir() + "LowCode.MergeContextDocuments.2.docx", SaveFormat.DOCX)
         .execute();

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 {
     saveOptions.setPassword("Aspose.Words");
 }
 Merger.create(mergerContext)
         .from(inputDoc1)
         .from(inputDoc2)
         .to(getArtifactsDir() + "LowCode.MergeContextDocuments.3.docx", saveOptions)
         .execute();
 
```

يعرض كيفية تحويل المستندات بسطر واحد من الشيفرة باستخدام السياق.

```

 String doc = getMyDir() + "Big document.docx";

 ConverterContext converterContext = new ConverterContext();

 Converter.create(converterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ConvertContext.1.pdf")
         .execute();

 Converter.create(converterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ConvertContext.2.pdf", SaveFormat.RTF)
         .execute();

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 {
     saveOptions.setPassword("Aspose.Words");
 }
 LoadOptions loadOptions = new LoadOptions();
 {
     loadOptions.setIgnoreOleData(true);
 }
 Converter.create(converterContext)
         .from(doc, loadOptions)
         .to(getArtifactsDir() + "LowCode.ConvertContext.3.docx", saveOptions)
         .execute();

 Converter.create(converterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ConvertContext.4.png", new ImageSaveOptions(SaveFormat.PNG))
         .execute();
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| إخراج | java.lang.String | اسم ملف الإخراج. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | خيارات الحفظ الاختيارية. إذا لم يتم تحديدها، يتم تحديد تنسيق الحفظ بناءً على امتداد الملف. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified output file.
### to(String output, int saveFormat) {#to-java.lang.String-int}
```
public Processor to(String output, int saveFormat)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| إخراج | java.lang.String |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(ArrayList output, SaveOptions saveOptions) {#to-java.util.ArrayList-com.aspose.words.SaveOptions}
```
public Processor to(ArrayList output, SaveOptions saveOptions)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| إخراج | java.util.ArrayList |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(ArrayList output, int saveFormat) {#to-java.util.ArrayList-int}
```
public Processor to(ArrayList output, int saveFormat)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| إخراج | java.util.ArrayList |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### toOutput(ArrayList output, SaveOptions saveOptions) {#toOutput-java.util.ArrayList-com.aspose.words.SaveOptions}
```
public Processor toOutput(ArrayList output, SaveOptions saveOptions)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| إخراج | java.util.ArrayList |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### toOutput(ArrayList output, int saveFormat) {#toOutput-java.util.ArrayList-int}
```
public Processor toOutput(ArrayList output, int saveFormat)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| إخراج | java.util.ArrayList |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
