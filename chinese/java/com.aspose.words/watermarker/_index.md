---
title: "水印器"
linktitle: "水印器"
second_title: "Aspose.Words for Java"
description: "提供用于在 Java 中向文档插入水印的方法。"
type: docs
weight: 724
url: /zh/java/com.aspose.words/watermarker/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Processor](../../com.aspose.words/processor/)
```
public class Watermarker extends Processor
```

提供用于向文档插入水印的方法。
## 方法

| 方法 | 描述 |
| --- | --- |
| [create(WatermarkerContext context)](#create-com.aspose.words.WatermarkerContext) | 创建水印处理器的新实例。 |
| [execute()](#execute) | 执行处理器操作。 |
| [from(InputStream input)](#from-java.io.InputStream) | 指定用于处理的输入文档。 |
| [from(InputStream input, LoadOptions loadOptions)](#from-java.io.InputStream-com.aspose.words.LoadOptions) | 指定用于处理的输入文档。 |
| [from(String input)](#from-java.lang.String) | 指定用于处理的输入文档。 |
| [from(String input, LoadOptions loadOptions)](#from-java.lang.String-com.aspose.words.LoadOptions) | 指定用于处理的输入文档。 |
| [setImage(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, BufferedImage watermarkImage)](#setImage-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.awt.image.BufferedImage) |  |
| [setImage(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, BufferedImage watermarkImage, ImageWatermarkOptions options)](#setImage-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.awt.image.BufferedImage-com.aspose.words.ImageWatermarkOptions) |  |
| [setImage(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, InputStream watermarkImageStream)](#setImage-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.io.InputStream) |  |
| [setImage(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, InputStream watermarkImageStream, ImageWatermarkOptions options)](#setImage-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.io.InputStream-com.aspose.words.ImageWatermarkOptions) |  |
| [setImage(InputStream inputStream, OutputStream outputStream, int saveFormat, BufferedImage watermarkImage)](#setImage-java.io.InputStream-java.io.OutputStream-int-java.awt.image.BufferedImage) |  |
| [setImage(InputStream inputStream, OutputStream outputStream, int saveFormat, BufferedImage watermarkImage, ImageWatermarkOptions options)](#setImage-java.io.InputStream-java.io.OutputStream-int-java.awt.image.BufferedImage-com.aspose.words.ImageWatermarkOptions) |  |
| [setImage(InputStream inputStream, OutputStream outputStream, int saveFormat, InputStream watermarkImageStream)](#setImage-java.io.InputStream-java.io.OutputStream-int-java.io.InputStream) |  |
| [setImage(InputStream inputStream, OutputStream outputStream, int saveFormat, InputStream watermarkImageStream, ImageWatermarkOptions options)](#setImage-java.io.InputStream-java.io.OutputStream-int-java.io.InputStream-com.aspose.words.ImageWatermarkOptions) |  |
| [setImage(String inputFileName, String outputFileName, SaveOptions saveOptions, String watermarkImageFileName)](#setImage-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String) | 在文档中添加图像水印，可使用选项并指定保存格式。 |
| [setImage(String inputFileName, String outputFileName, SaveOptions saveOptions, String watermarkImageFileName, ImageWatermarkOptions options)](#setImage-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String-com.aspose.words.ImageWatermarkOptions) | 在文档中添加图像水印，可使用选项并指定保存格式。 |
| [setImage(String inputFileName, String outputFileName, int saveFormat, String watermarkImageFileName)](#setImage-java.lang.String-java.lang.String-int-java.lang.String) |  |
| [setImage(String inputFileName, String outputFileName, int saveFormat, String watermarkImageFileName, ImageWatermarkOptions options)](#setImage-java.lang.String-java.lang.String-int-java.lang.String-com.aspose.words.ImageWatermarkOptions) |  |
| [setImage(String inputFileName, String outputFileName, String watermarkImageFileName)](#setImage-java.lang.String-java.lang.String-java.lang.String) | 在文档中添加图像水印。 |
| [setImage(String inputFileName, String outputFileName, String watermarkImageFileName, ImageWatermarkOptions options)](#setImage-java.lang.String-java.lang.String-java.lang.String-com.aspose.words.ImageWatermarkOptions) | 在文档中添加图像水印，并可使用选项。 |
| [setText(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, String watermarkText)](#setText-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.String) |  |
| [setText(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, String watermarkText, TextWatermarkOptions options)](#setText-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.String-com.aspose.words.TextWatermarkOptions) |  |
| [setText(InputStream inputStream, OutputStream outputStream, int saveFormat, String watermarkText)](#setText-java.io.InputStream-java.io.OutputStream-int-java.lang.String) |  |
| [setText(InputStream inputStream, OutputStream outputStream, int saveFormat, String watermarkText, TextWatermarkOptions options)](#setText-java.io.InputStream-java.io.OutputStream-int-java.lang.String-com.aspose.words.TextWatermarkOptions) |  |
| [setText(String inputFileName, String outputFileName, SaveOptions saveOptions, String watermarkText)](#setText-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String) | 在文档中添加文本水印，可使用选项并指定保存格式。 |
| [setText(String inputFileName, String outputFileName, SaveOptions saveOptions, String watermarkText, TextWatermarkOptions options)](#setText-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String-com.aspose.words.TextWatermarkOptions) | 在文档中添加文本水印，可使用选项并指定保存格式。 |
| [setText(String inputFileName, String outputFileName, int saveFormat, String watermarkText)](#setText-java.lang.String-java.lang.String-int-java.lang.String) |  |
| [setText(String inputFileName, String outputFileName, int saveFormat, String watermarkText, TextWatermarkOptions options)](#setText-java.lang.String-java.lang.String-int-java.lang.String-com.aspose.words.TextWatermarkOptions) |  |
| [setText(String inputFileName, String outputFileName, String watermarkText)](#setText-java.lang.String-java.lang.String-java.lang.String) | 在文档中添加文本水印。 |
| [setText(String inputFileName, String outputFileName, String watermarkText, TextWatermarkOptions options)](#setText-java.lang.String-java.lang.String-java.lang.String-com.aspose.words.TextWatermarkOptions) | 在文档中添加文本水印，并可使用选项。 |
| [setWatermarkToImages(InputStream inputStream, ImageSaveOptions saveOptions, InputStream watermarkImageStream)](#setWatermarkToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.io.InputStream) | 在文档中添加图像水印，并可使用选项。 |
| [setWatermarkToImages(InputStream inputStream, ImageSaveOptions saveOptions, InputStream watermarkImageStream, ImageWatermarkOptions options)](#setWatermarkToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.io.InputStream-com.aspose.words.ImageWatermarkOptions) | 在文档中添加图像水印，并可使用选项。 |
| [setWatermarkToImages(InputStream inputStream, ImageSaveOptions saveOptions, String watermarkText)](#setWatermarkToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String) | 在文档中添加文本水印，并可使用选项。 |
| [setWatermarkToImages(InputStream inputStream, ImageSaveOptions saveOptions, String watermarkText, TextWatermarkOptions options)](#setWatermarkToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String-com.aspose.words.TextWatermarkOptions) | 在文档中添加文本水印，并可使用选项。 |
| [setWatermarkToImages(String inputFileName, ImageSaveOptions saveOptions, byte[] watermarkImageBytes)](#setWatermarkToImages-java.lang.String-com.aspose.words.ImageSaveOptions-byte) | 在文档中添加图像水印，并可使用选项。 |
| [setWatermarkToImages(String inputFileName, ImageSaveOptions saveOptions, byte[] watermarkImageBytes, ImageWatermarkOptions options)](#setWatermarkToImages-java.lang.String-com.aspose.words.ImageSaveOptions-byte---com.aspose.words.ImageWatermarkOptions) | 在文档中添加图像水印，并可使用选项。 |
| [setWatermarkToImages(String inputFileName, ImageSaveOptions saveOptions, String watermarkText)](#setWatermarkToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String) | 在文档中添加文本水印，并可使用选项。 |
| [setWatermarkToImages(String inputFileName, ImageSaveOptions saveOptions, String watermarkText, TextWatermarkOptions options)](#setWatermarkToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String-com.aspose.words.TextWatermarkOptions) | 在文档中添加文本水印，并可使用选项。 |
| [to(OutputStream output, SaveOptions saveOptions)](#to-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [to(OutputStream output, int saveFormat)](#to-java.io.OutputStream-int) |  |
| [to(String output)](#to-java.lang.String) | 指定处理器的输出文件。 |
| [to(String output, SaveOptions saveOptions)](#to-java.lang.String-com.aspose.words.SaveOptions) | 指定处理器的输出文件。 |
| [to(String output, int saveFormat)](#to-java.lang.String-int) |  |
| [to(ArrayList output, SaveOptions saveOptions)](#to-java.util.ArrayList-com.aspose.words.SaveOptions) |  |
| [to(ArrayList output, int saveFormat)](#to-java.util.ArrayList-int) |  |
| [toOutput(ArrayList output, SaveOptions saveOptions)](#toOutput-java.util.ArrayList-com.aspose.words.SaveOptions) |  |
| [toOutput(ArrayList output, int saveFormat)](#toOutput-java.util.ArrayList-int) |  |
### create(WatermarkerContext context) {#create-com.aspose.words.WatermarkerContext}
```
public static Watermarker create(WatermarkerContext context)
```


创建水印处理器的新实例。

 **Examples:** 

展示如何使用上下文向文档插入水印文本。

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

展示如何使用上下文从流中向文档插入水印文本。

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

展示如何使用上下文向文档插入水印图像。

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

展示如何使用上下文从流中向文档插入水印图像。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| context | [WatermarkerContext](../../com.aspose.words/watermarkercontext/) |  |

**Returns:**
[Watermarker](../../com.aspose.words/watermarker/)
### execute() {#execute}
```
public void execute()
```


执行处理器操作。

 **Examples:** 

展示如何在上下文中将文档合并为单个输出文档。

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

展示如何在上下文中将来自流的文档合并为单个输出文档。

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

展示如何在上下文中使用一行代码转换文档。

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

展示如何在上下文中使用一行代码将来自流的文档转换。

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


指定用于处理的输入文档。

 **Remarks:** 

如果处理器仅接受单个文件作为输入，则只会处理最后指定的文件。 [Merger](../../com.aspose.words/merger/) 处理器接受多个文件作为输入，结果是所有指定的文档将被合并。 [Converter](../../com.aspose.words/converter/) 处理器仅接受单个文件作为输入，因此只会转换最后指定的文件。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 输入 | java.io.InputStream | 输入文档流。 |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file stream.
### from(InputStream input, LoadOptions loadOptions) {#from-java.io.InputStream-com.aspose.words.LoadOptions}
```
public Processor from(InputStream input, LoadOptions loadOptions)
```


指定用于处理的输入文档。

 **Remarks:** 

如果处理器仅接受单个文件作为输入，则只会处理最后指定的文件。 [Merger](../../com.aspose.words/merger/) 处理器接受多个文件作为输入，结果是所有指定的文档将被合并。 [Converter](../../com.aspose.words/converter/) 处理器仅接受单个文件作为输入，因此只会转换最后指定的文件。

 **Examples:** 

展示如何在上下文中将来自流的文档合并为单个输出文档。

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

展示如何在上下文中使用一行代码将来自流的文档转换。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 输入 | java.io.InputStream | 输入文档流。 |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | 用于加载文档的可选加载选项。 |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file stream.
### from(String input) {#from-java.lang.String}
```
public Processor from(String input)
```


指定用于处理的输入文档。

 **Remarks:** 

如果处理器仅接受单个文件作为输入，则只会处理最后指定的文件。 [Merger](../../com.aspose.words/merger/) 处理器接受多个文件作为输入，结果是所有指定的文档将被合并。 [Converter](../../com.aspose.words/converter/) 处理器仅接受单个文件作为输入，因此只会转换最后指定的文件。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 输入 | java.lang.String | 输入文档文件名。 |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file.
### from(String input, LoadOptions loadOptions) {#from-java.lang.String-com.aspose.words.LoadOptions}
```
public Processor from(String input, LoadOptions loadOptions)
```


指定用于处理的输入文档。

 **Remarks:** 

如果处理器仅接受单个文件作为输入，则只会处理最后指定的文件。 [Merger](../../com.aspose.words/merger/) 处理器接受多个文件作为输入，结果是所有指定的文档将被合并。 [Converter](../../com.aspose.words/converter/) 处理器仅接受单个文件作为输入，因此只会转换最后指定的文件。

 **Examples:** 

展示如何在上下文中将文档合并为单个输出文档。

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

展示如何在上下文中使用一行代码转换文档。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 输入 | java.lang.String | 输入文档文件名。 |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | 用于加载文档的可选加载选项。 |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file.
### setImage(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, BufferedImage watermarkImage) {#setImage-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.awt.image.BufferedImage}
```
public static void setImage(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, BufferedImage watermarkImage)
```




**Parameters:**
| 参数 | 类型 | 描述 |
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
| 参数 | 类型 | 描述 |
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
| 参数 | 类型 | 描述 |
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
| 参数 | 类型 | 描述 |
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
| 参数 | 类型 | 描述 |
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
| 参数 | 类型 | 描述 |
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
| 参数 | 类型 | 描述 |
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
| 参数 | 类型 | 描述 |
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


在文档中添加图像水印，可使用选项并指定保存格式。

 **Remarks:** 

如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则 outputFile\_partIndex.extension 为每个部分生成文件名。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String | 输入文件名。 |
| outputFileName | java.lang.String | 输出文件名。 |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | 保存选项。 |
| watermarkImageFileName | java.lang.String | 作为水印显示的图像。 |

### setImage(String inputFileName, String outputFileName, SaveOptions saveOptions, String watermarkImageFileName, ImageWatermarkOptions options) {#setImage-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String-com.aspose.words.ImageWatermarkOptions}
```
public static void setImage(String inputFileName, String outputFileName, SaveOptions saveOptions, String watermarkImageFileName, ImageWatermarkOptions options)
```


在文档中添加图像水印，可使用选项并指定保存格式。

 **Remarks:** 

如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则 outputFile\_partIndex.extension 为每个部分生成文件名。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String | 输入文件名。 |
| outputFileName | java.lang.String | 输出文件名。 |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | 保存选项。 |
| watermarkImageFileName | java.lang.String | 作为水印显示的图像。 |
| options | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) | 定义图像水印的附加选项。 |

### setImage(String inputFileName, String outputFileName, int saveFormat, String watermarkImageFileName) {#setImage-java.lang.String-java.lang.String-int-java.lang.String}
```
public static void setImage(String inputFileName, String outputFileName, int saveFormat, String watermarkImageFileName)
```




**Parameters:**
| 参数 | 类型 | 描述 |
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
| 参数 | 类型 | 描述 |
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


在文档中添加图像水印。

 **Remarks:** 

如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则 outputFile\_partIndex.extension 为每个部分生成文件名。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String | 输入文件名。 |
| outputFileName | java.lang.String | 输出文件名。 |
| watermarkImageFileName | java.lang.String | 作为水印显示的图像。 |

### setImage(String inputFileName, String outputFileName, String watermarkImageFileName, ImageWatermarkOptions options) {#setImage-java.lang.String-java.lang.String-java.lang.String-com.aspose.words.ImageWatermarkOptions}
```
public static void setImage(String inputFileName, String outputFileName, String watermarkImageFileName, ImageWatermarkOptions options)
```


在文档中添加图像水印，并可使用选项。

 **Remarks:** 

如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则 outputFile\_partIndex.extension 为每个部分生成文件名。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

 **Examples:** 

展示如何向文档插入水印图像。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String | 输入文件名。 |
| outputFileName | java.lang.String | 输出文件名。 |
| watermarkImageFileName | java.lang.String | 作为水印显示的图像。 |
| options | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) | 定义图像水印的附加选项。 |

### setText(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, String watermarkText) {#setText-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.String}
```
public static void setText(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, String watermarkText)
```




**Parameters:**
| 参数 | 类型 | 描述 |
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
| 参数 | 类型 | 描述 |
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
| 参数 | 类型 | 描述 |
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
| 参数 | 类型 | 描述 |
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


在文档中添加文本水印，可使用选项并指定保存格式。

 **Remarks:** 

如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则 outputFile\_partIndex.extension 为每个部分生成文件名。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String | 输入文件名。 |
| outputFileName | java.lang.String | 输出文件名。 |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | 保存选项。 |
| watermarkText | java.lang.String | 显示为水印的文本。 |

### setText(String inputFileName, String outputFileName, SaveOptions saveOptions, String watermarkText, TextWatermarkOptions options) {#setText-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String-com.aspose.words.TextWatermarkOptions}
```
public static void setText(String inputFileName, String outputFileName, SaveOptions saveOptions, String watermarkText, TextWatermarkOptions options)
```


在文档中添加文本水印，可使用选项并指定保存格式。

 **Remarks:** 

如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则 outputFile\_partIndex.extension 为每个部分生成文件名。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String | 输入文件名。 |
| outputFileName | java.lang.String | 输出文件名。 |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | 保存选项。 |
| watermarkText | java.lang.String | 显示为水印的文本。 |
| options | [TextWatermarkOptions](../../com.aspose.words/textwatermarkoptions/) | 定义文本水印的其他选项。 |

### setText(String inputFileName, String outputFileName, int saveFormat, String watermarkText) {#setText-java.lang.String-java.lang.String-int-java.lang.String}
```
public static void setText(String inputFileName, String outputFileName, int saveFormat, String watermarkText)
```




**Parameters:**
| 参数 | 类型 | 描述 |
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
| 参数 | 类型 | 描述 |
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


在文档中添加文本水印。

 **Remarks:** 

如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则 outputFile\_partIndex.extension 为每个部分生成文件名。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String | 输入文件名。 |
| outputFileName | java.lang.String | 输出文件名。 |
| watermarkText | java.lang.String | 显示为水印的文本。 |

### setText(String inputFileName, String outputFileName, String watermarkText, TextWatermarkOptions options) {#setText-java.lang.String-java.lang.String-java.lang.String-com.aspose.words.TextWatermarkOptions}
```
public static void setText(String inputFileName, String outputFileName, String watermarkText, TextWatermarkOptions options)
```


在文档中添加文本水印，并可使用选项。

 **Remarks:** 

如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则 outputFile\_partIndex.extension 为每个部分生成文件名。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

 **Examples:** 

展示如何向文档插入水印文本。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String | 输入文件名。 |
| outputFileName | java.lang.String | 输出文件名。 |
| watermarkText | java.lang.String | 显示为水印的文本。 |
| options | [TextWatermarkOptions](../../com.aspose.words/textwatermarkoptions/) | 定义文本水印的其他选项。 |

### setWatermarkToImages(InputStream inputStream, ImageSaveOptions saveOptions, InputStream watermarkImageStream) {#setWatermarkToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.io.InputStream}
```
public static OutputStream[] setWatermarkToImages(InputStream inputStream, ImageSaveOptions saveOptions, InputStream watermarkImageStream)
```


向文档添加带有选项的图像水印。将输出渲染为图像。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream | 输入流。 |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | 保存选项。 |
| watermarkImageStream | java.io.InputStream | 显示为水印的图像流。 |

**Returns:**
java.io.OutputStream[]
### setWatermarkToImages(InputStream inputStream, ImageSaveOptions saveOptions, InputStream watermarkImageStream, ImageWatermarkOptions options) {#setWatermarkToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.io.InputStream-com.aspose.words.ImageWatermarkOptions}
```
public static OutputStream[] setWatermarkToImages(InputStream inputStream, ImageSaveOptions saveOptions, InputStream watermarkImageStream, ImageWatermarkOptions options)
```


向文档添加带有选项的图像水印。将输出渲染为图像。

 **Examples:** 

展示如何从流向文档插入水印图像并将结果保存为图像。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream | 输入流。 |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | 保存选项。 |
| watermarkImageStream | java.io.InputStream | 显示为水印的图像流。 |
| options | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) | 定义图像水印的附加选项。 |

**Returns:**
java.io.OutputStream[]
### setWatermarkToImages(InputStream inputStream, ImageSaveOptions saveOptions, String watermarkText) {#setWatermarkToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String}
```
public static OutputStream[] setWatermarkToImages(InputStream inputStream, ImageSaveOptions saveOptions, String watermarkText)
```


向文档添加带有选项的文本水印。将输出渲染为图像。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream | 输入文件流。 |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | 保存选项。 |
| watermarkText | java.lang.String | 显示为水印的文本。 |

**Returns:**
java.io.OutputStream[]
### setWatermarkToImages(InputStream inputStream, ImageSaveOptions saveOptions, String watermarkText, TextWatermarkOptions options) {#setWatermarkToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String-com.aspose.words.TextWatermarkOptions}
```
public static OutputStream[] setWatermarkToImages(InputStream inputStream, ImageSaveOptions saveOptions, String watermarkText, TextWatermarkOptions options)
```


向文档添加带有选项的文本水印。将输出渲染为图像。

 **Examples:** 

展示如何从流向文档插入水印文本并将结果保存为图像。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream | 输入文件流。 |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | 保存选项。 |
| watermarkText | java.lang.String | 显示为水印的文本。 |
| options | [TextWatermarkOptions](../../com.aspose.words/textwatermarkoptions/) | 定义文本水印的其他选项。 |

**Returns:**
java.io.OutputStream[]
### setWatermarkToImages(String inputFileName, ImageSaveOptions saveOptions, byte[] watermarkImageBytes) {#setWatermarkToImages-java.lang.String-com.aspose.words.ImageSaveOptions-byte}
```
public static OutputStream[] setWatermarkToImages(String inputFileName, ImageSaveOptions saveOptions, byte[] watermarkImageBytes)
```


向文档添加带有选项的图像水印。将输出渲染为图像。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String | 输入文件名。 |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | 保存选项。 |
| watermarkImageBytes | byte[] | 显示为水印的图像字节。 |

**Returns:**
java.io.OutputStream[]
### setWatermarkToImages(String inputFileName, ImageSaveOptions saveOptions, byte[] watermarkImageBytes, ImageWatermarkOptions options) {#setWatermarkToImages-java.lang.String-com.aspose.words.ImageSaveOptions-byte---com.aspose.words.ImageWatermarkOptions}
```
public static OutputStream[] setWatermarkToImages(String inputFileName, ImageSaveOptions saveOptions, byte[] watermarkImageBytes, ImageWatermarkOptions options)
```


向文档添加带有选项的图像水印。将输出渲染为图像。

 **Examples:** 

展示如何向文档插入水印图像并将结果保存为图像。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String | 输入文件名。 |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | 保存选项。 |
| watermarkImageBytes | byte[] | 显示为水印的图像字节。 |
| options | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) | 定义图像水印的附加选项。 |

**Returns:**
java.io.OutputStream[]
### setWatermarkToImages(String inputFileName, ImageSaveOptions saveOptions, String watermarkText) {#setWatermarkToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String}
```
public static OutputStream[] setWatermarkToImages(String inputFileName, ImageSaveOptions saveOptions, String watermarkText)
```


向文档添加带有选项的文本水印。将输出渲染为图像。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String | 输入文件名。 |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | 保存选项。 |
| watermarkText | java.lang.String | 显示为水印的文本。 |

**Returns:**
java.io.OutputStream[]
### setWatermarkToImages(String inputFileName, ImageSaveOptions saveOptions, String watermarkText, TextWatermarkOptions options) {#setWatermarkToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String-com.aspose.words.TextWatermarkOptions}
```
public static OutputStream[] setWatermarkToImages(String inputFileName, ImageSaveOptions saveOptions, String watermarkText, TextWatermarkOptions options)
```


向文档添加带有选项的文本水印。将输出渲染为图像。

 **Examples:** 

展示如何向文档插入水印文本并将结果保存为图像。

```

 String doc = getMyDir() + "Big document.docx";
 String watermarkText = "This is a watermark";

 OutputStream[] images = Watermarker.setWatermarkToImages(doc, new ImageSaveOptions(SaveFormat.PNG), watermarkText);

 TextWatermarkOptions watermarkOptions = new TextWatermarkOptions();
 watermarkOptions.setColor(Color.RED);
 images = Watermarker.setWatermarkToImages(doc, new ImageSaveOptions(SaveFormat.PNG), watermarkText, watermarkOptions);
 
```

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String | 输入文件名。 |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | 保存选项。 |
| watermarkText | java.lang.String | 显示为水印的文本。 |
| options | [TextWatermarkOptions](../../com.aspose.words/textwatermarkoptions/) | 定义文本水印的其他选项。 |

**Returns:**
java.io.OutputStream[]
### to(OutputStream output, SaveOptions saveOptions) {#to-java.io.OutputStream-com.aspose.words.SaveOptions}
```
public Processor to(OutputStream output, SaveOptions saveOptions)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 输出 | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(OutputStream output, int saveFormat) {#to-java.io.OutputStream-int}
```
public Processor to(OutputStream output, int saveFormat)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 输出 | java.io.OutputStream |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(String output) {#to-java.lang.String}
```
public Processor to(String output)
```


指定处理器的输出文件。

 **Remarks:** 

如果输出包含多个文件，则使用指定的输出文件名按照规则 'outputFile\\_partIndex.extension' 为每个部分生成文件名。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 输出 | java.lang.String | 输出文件名。 |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified output file.
### to(String output, SaveOptions saveOptions) {#to-java.lang.String-com.aspose.words.SaveOptions}
```
public Processor to(String output, SaveOptions saveOptions)
```


指定处理器的输出文件。

 **Remarks:** 

如果输出包含多个文件，则使用指定的输出文件名按照规则 'outputFile\\_partIndex.extension' 为每个部分生成文件名。

 **Examples:** 

展示如何在上下文中将文档合并为单个输出文档。

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

展示如何在上下文中使用一行代码转换文档。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 输出 | java.lang.String | 输出文件名。 |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | 可选的保存选项。如果未指定，保存格式将由文件扩展名决定。 |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified output file.
### to(String output, int saveFormat) {#to-java.lang.String-int}
```
public Processor to(String output, int saveFormat)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 输出 | java.lang.String |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(ArrayList output, SaveOptions saveOptions) {#to-java.util.ArrayList-com.aspose.words.SaveOptions}
```
public Processor to(ArrayList output, SaveOptions saveOptions)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 输出 | java.util.ArrayList |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(ArrayList output, int saveFormat) {#to-java.util.ArrayList-int}
```
public Processor to(ArrayList output, int saveFormat)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 输出 | java.util.ArrayList |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### toOutput(ArrayList output, SaveOptions saveOptions) {#toOutput-java.util.ArrayList-com.aspose.words.SaveOptions}
```
public Processor toOutput(ArrayList output, SaveOptions saveOptions)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 输出 | java.util.ArrayList |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### toOutput(ArrayList output, int saveFormat) {#toOutput-java.util.ArrayList-int}
```
public Processor toOutput(ArrayList output, int saveFormat)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 输出 | java.util.ArrayList |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
