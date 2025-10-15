---
title: Watermarker
linktitle: Watermarker
second_title: Aspose.Words for Java
description: Provides methods intended to insert watermarks into the documents in Java.
type: docs
weight: 720
url: /java/com.aspose.words/watermarker/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Processor](../../com.aspose.words/processor/)
```
public class Watermarker extends Processor
```

Provides methods intended to insert watermarks into the documents.
## Methods

| Method | Description |
| --- | --- |
| [create(WatermarkerContext context)](#create-com.aspose.words.WatermarkerContext) | Creates new instance of the watermarker processor. |
| [execute()](#execute) | Execute the processor action. |
| [from(InputStream input)](#from-java.io.InputStream) |  |
| [from(InputStream input, LoadOptions loadOptions)](#from-java.io.InputStream-com.aspose.words.LoadOptions) | Specifies input document for processing. |
| [from(String input)](#from-java.lang.String) |  |
| [from(String input, LoadOptions loadOptions)](#from-java.lang.String-com.aspose.words.LoadOptions) | Specifies input document for processing. |
| [setImage(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, BufferedImage watermarkImage)](#setImage-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.awt.image.BufferedImage) |  |
| [setImage(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, BufferedImage watermarkImage, ImageWatermarkOptions options)](#setImage-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.awt.image.BufferedImage-com.aspose.words.ImageWatermarkOptions) |  |
| [setImage(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, InputStream watermarkImageStream)](#setImage-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.io.InputStream) |  |
| [setImage(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, InputStream watermarkImageStream, ImageWatermarkOptions options)](#setImage-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.io.InputStream-com.aspose.words.ImageWatermarkOptions) |  |
| [setImage(InputStream inputStream, OutputStream outputStream, int saveFormat, BufferedImage watermarkImage)](#setImage-java.io.InputStream-java.io.OutputStream-int-java.awt.image.BufferedImage) |  |
| [setImage(InputStream inputStream, OutputStream outputStream, int saveFormat, BufferedImage watermarkImage, ImageWatermarkOptions options)](#setImage-java.io.InputStream-java.io.OutputStream-int-java.awt.image.BufferedImage-com.aspose.words.ImageWatermarkOptions) |  |
| [setImage(InputStream inputStream, OutputStream outputStream, int saveFormat, InputStream watermarkImageStream)](#setImage-java.io.InputStream-java.io.OutputStream-int-java.io.InputStream) |  |
| [setImage(InputStream inputStream, OutputStream outputStream, int saveFormat, InputStream watermarkImageStream, ImageWatermarkOptions options)](#setImage-java.io.InputStream-java.io.OutputStream-int-java.io.InputStream-com.aspose.words.ImageWatermarkOptions) |  |
| [setImage(String inputFileName, String outputFileName, SaveOptions saveOptions, String watermarkImageFileName)](#setImage-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String) |  |
| [setImage(String inputFileName, String outputFileName, SaveOptions saveOptions, String watermarkImageFileName, ImageWatermarkOptions options)](#setImage-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String-com.aspose.words.ImageWatermarkOptions) | Adds an image watermark into the document with options and specified save format. |
| [setImage(String inputFileName, String outputFileName, int saveFormat, String watermarkImageFileName)](#setImage-java.lang.String-java.lang.String-int-java.lang.String) |  |
| [setImage(String inputFileName, String outputFileName, int saveFormat, String watermarkImageFileName, ImageWatermarkOptions options)](#setImage-java.lang.String-java.lang.String-int-java.lang.String-com.aspose.words.ImageWatermarkOptions) |  |
| [setImage(String inputFileName, String outputFileName, String watermarkImageFileName)](#setImage-java.lang.String-java.lang.String-java.lang.String) | Adds an image watermark into the document. |
| [setImage(String inputFileName, String outputFileName, String watermarkImageFileName, ImageWatermarkOptions options)](#setImage-java.lang.String-java.lang.String-java.lang.String-com.aspose.words.ImageWatermarkOptions) | Adds an image watermark into the document with options. |
| [setText(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, String watermarkText)](#setText-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.String) |  |
| [setText(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, String watermarkText, TextWatermarkOptions options)](#setText-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.String-com.aspose.words.TextWatermarkOptions) |  |
| [setText(InputStream inputStream, OutputStream outputStream, int saveFormat, String watermarkText)](#setText-java.io.InputStream-java.io.OutputStream-int-java.lang.String) |  |
| [setText(InputStream inputStream, OutputStream outputStream, int saveFormat, String watermarkText, TextWatermarkOptions options)](#setText-java.io.InputStream-java.io.OutputStream-int-java.lang.String-com.aspose.words.TextWatermarkOptions) |  |
| [setText(String inputFileName, String outputFileName, SaveOptions saveOptions, String watermarkText)](#setText-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String) |  |
| [setText(String inputFileName, String outputFileName, SaveOptions saveOptions, String watermarkText, TextWatermarkOptions options)](#setText-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String-com.aspose.words.TextWatermarkOptions) | Adds a text watermark into the document with options and specified save format. |
| [setText(String inputFileName, String outputFileName, int saveFormat, String watermarkText)](#setText-java.lang.String-java.lang.String-int-java.lang.String) |  |
| [setText(String inputFileName, String outputFileName, int saveFormat, String watermarkText, TextWatermarkOptions options)](#setText-java.lang.String-java.lang.String-int-java.lang.String-com.aspose.words.TextWatermarkOptions) |  |
| [setText(String inputFileName, String outputFileName, String watermarkText)](#setText-java.lang.String-java.lang.String-java.lang.String) | Adds a text watermark into the document. |
| [setText(String inputFileName, String outputFileName, String watermarkText, TextWatermarkOptions options)](#setText-java.lang.String-java.lang.String-java.lang.String-com.aspose.words.TextWatermarkOptions) | Adds a text watermark into the document with options. |
| [setWatermarkToImages(InputStream inputStream, ImageSaveOptions saveOptions, InputStream watermarkImageStream)](#setWatermarkToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.io.InputStream) |  |
| [setWatermarkToImages(InputStream inputStream, ImageSaveOptions saveOptions, InputStream watermarkImageStream, ImageWatermarkOptions options)](#setWatermarkToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.io.InputStream-com.aspose.words.ImageWatermarkOptions) | Adds an image watermark into the document with options. |
| [setWatermarkToImages(InputStream inputStream, ImageSaveOptions saveOptions, String watermarkText)](#setWatermarkToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String) |  |
| [setWatermarkToImages(InputStream inputStream, ImageSaveOptions saveOptions, String watermarkText, TextWatermarkOptions options)](#setWatermarkToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String-com.aspose.words.TextWatermarkOptions) | Adds a text watermark into the document with options. |
| [setWatermarkToImages(String inputFileName, ImageSaveOptions saveOptions, byte[] watermarkImageBytes)](#setWatermarkToImages-java.lang.String-com.aspose.words.ImageSaveOptions-byte) |  |
| [setWatermarkToImages(String inputFileName, ImageSaveOptions saveOptions, byte[] watermarkImageBytes, ImageWatermarkOptions options)](#setWatermarkToImages-java.lang.String-com.aspose.words.ImageSaveOptions-byte---com.aspose.words.ImageWatermarkOptions) | Adds an image watermark into the document with options. |
| [setWatermarkToImages(String inputFileName, ImageSaveOptions saveOptions, String watermarkText)](#setWatermarkToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String) |  |
| [setWatermarkToImages(String inputFileName, ImageSaveOptions saveOptions, String watermarkText, TextWatermarkOptions options)](#setWatermarkToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String-com.aspose.words.TextWatermarkOptions) | Adds a text watermark into the document with options. |
| [to(OutputStream output, SaveOptions saveOptions)](#to-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [to(OutputStream output, int saveFormat)](#to-java.io.OutputStream-int) |  |
| [to(String output)](#to-java.lang.String) |  |
| [to(String output, SaveOptions saveOptions)](#to-java.lang.String-com.aspose.words.SaveOptions) | Specifies output file for the processor. |
| [to(String output, int saveFormat)](#to-java.lang.String-int) |  |
| [to(ArrayList output, SaveOptions saveOptions)](#to-java.util.ArrayList-com.aspose.words.SaveOptions) |  |
| [to(ArrayList output, int saveFormat)](#to-java.util.ArrayList-int) |  |
| [toOutput(ArrayList output, SaveOptions saveOptions)](#toOutput-java.util.ArrayList-com.aspose.words.SaveOptions) |  |
| [toOutput(ArrayList output, int saveFormat)](#toOutput-java.util.ArrayList-int) |  |
### create(WatermarkerContext context) {#create-com.aspose.words.WatermarkerContext}
```
public static Watermarker create(WatermarkerContext context)
```


Creates new instance of the watermarker processor.

 **Examples:** 

Shows how to insert watermark text to the document using context.

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

Shows how to insert watermark image to the document using context.

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

Shows how to insert watermark text to the document from the stream using context.

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

Shows how to insert watermark image to the document from a stream using context.

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
| Parameter | Type | Description |
| --- | --- | --- |
| context | [WatermarkerContext](../../com.aspose.words/watermarkercontext/) |  |

**Returns:**
[Watermarker](../../com.aspose.words/watermarker/)
### execute() {#execute}
```
public void execute()
```


Execute the processor action.

 **Examples:** 

Shows how to convert documents with a single line of code using context.

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

Shows how to convert documents from a stream with a single line of code using context.

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

Shows how to merge documents into a single output document using context.

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

Shows how to merge documents from stream into a single output document using context.

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

### from(InputStream input) {#from-java.io.InputStream}
```
public Processor from(InputStream input)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| input | java.io.InputStream |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### from(InputStream input, LoadOptions loadOptions) {#from-java.io.InputStream-com.aspose.words.LoadOptions}
```
public Processor from(InputStream input, LoadOptions loadOptions)
```


Specifies input document for processing.

 **Remarks:** 

If the processor accepts only one file as an input, only the last specified file will be processed. [Merger](../../com.aspose.words/merger/) processor accepts multiple files as an input, as the result all the specified documents will be merged. [Converter](../../com.aspose.words/converter/) processor accepts only one file as an input, so only the last specified file will be converted.

 **Examples:** 

Shows how to convert documents from a stream with a single line of code using context.

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

Shows how to merge documents from stream into a single output document using context.

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

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| input | java.io.InputStream | Input document stream. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Optional load options used to load the document. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file stream.
### from(String input) {#from-java.lang.String}
```
public Processor from(String input)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| input | java.lang.String |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### from(String input, LoadOptions loadOptions) {#from-java.lang.String-com.aspose.words.LoadOptions}
```
public Processor from(String input, LoadOptions loadOptions)
```


Specifies input document for processing.

 **Remarks:** 

If the processor accepts only one file as an input, only the last specified file will be processed. [Merger](../../com.aspose.words/merger/) processor accepts multiple files as an input, as the result all the specified documents will be merged. [Converter](../../com.aspose.words/converter/) processor accepts only one file as an input, so only the last specified file will be converted.

 **Examples:** 

Shows how to convert documents with a single line of code using context.

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

Shows how to merge documents into a single output document using context.

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

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| input | java.lang.String | Input document file name. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Optional load options used to load the document. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file.
### setImage(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, BufferedImage watermarkImage) {#setImage-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.awt.image.BufferedImage}
```
public static void setImage(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, BufferedImage watermarkImage)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
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
| Parameter | Type | Description |
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
| Parameter | Type | Description |
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
| Parameter | Type | Description |
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
| Parameter | Type | Description |
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
| Parameter | Type | Description |
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
| Parameter | Type | Description |
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




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| watermarkImageFileName | java.lang.String |  |

### setImage(String inputFileName, String outputFileName, SaveOptions saveOptions, String watermarkImageFileName, ImageWatermarkOptions options) {#setImage-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String-com.aspose.words.ImageWatermarkOptions}
```
public static void setImage(String inputFileName, String outputFileName, SaveOptions saveOptions, String watermarkImageFileName, ImageWatermarkOptions options)
```


Adds an image watermark into the document with options and specified save format.

 **Remarks:** 

If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), each page of the output will be saved as a separate file. The specified output file name will be used to generate file names for each part following the rule: outputFile\_partIndex.extension.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF file.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | The input file name. |
| outputFileName | java.lang.String | The output file name. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | The save options. |
| watermarkImageFileName | java.lang.String | Image that is displayed as a watermark. |
| options | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) | Defines additional options for the image watermark. |

### setImage(String inputFileName, String outputFileName, int saveFormat, String watermarkImageFileName) {#setImage-java.lang.String-java.lang.String-int-java.lang.String}
```
public static void setImage(String inputFileName, String outputFileName, int saveFormat, String watermarkImageFileName)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
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


Adds an image watermark into the document.

 **Remarks:** 

If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), each page of the output will be saved as a separate file. The specified output file name will be used to generate file names for each part following the rule: outputFile\_partIndex.extension.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF file.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | The input file name. |
| outputFileName | java.lang.String | The output file name. |
| watermarkImageFileName | java.lang.String | Image that is displayed as a watermark. |

### setImage(String inputFileName, String outputFileName, String watermarkImageFileName, ImageWatermarkOptions options) {#setImage-java.lang.String-java.lang.String-java.lang.String-com.aspose.words.ImageWatermarkOptions}
```
public static void setImage(String inputFileName, String outputFileName, String watermarkImageFileName, ImageWatermarkOptions options)
```


Adds an image watermark into the document with options.

 **Remarks:** 

If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), each page of the output will be saved as a separate file. The specified output file name will be used to generate file names for each part following the rule: outputFile\_partIndex.extension.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF file.

 **Examples:** 

Shows how to insert watermark image to the document.

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
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | The input file name. |
| outputFileName | java.lang.String | The output file name. |
| watermarkImageFileName | java.lang.String | Image that is displayed as a watermark. |
| options | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) | Defines additional options for the image watermark. |

### setText(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, String watermarkText) {#setText-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.String}
```
public static void setText(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, String watermarkText)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
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
| Parameter | Type | Description |
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
| Parameter | Type | Description |
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




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| watermarkText | java.lang.String |  |

### setText(String inputFileName, String outputFileName, SaveOptions saveOptions, String watermarkText, TextWatermarkOptions options) {#setText-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String-com.aspose.words.TextWatermarkOptions}
```
public static void setText(String inputFileName, String outputFileName, SaveOptions saveOptions, String watermarkText, TextWatermarkOptions options)
```


Adds a text watermark into the document with options and specified save format.

 **Remarks:** 

If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), each page of the output will be saved as a separate file. The specified output file name will be used to generate file names for each part following the rule: outputFile\_partIndex.extension.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF file.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | The input file name. |
| outputFileName | java.lang.String | The output file name. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | The save options. |
| watermarkText | java.lang.String | Text that is displayed as a watermark. |
| options | [TextWatermarkOptions](../../com.aspose.words/textwatermarkoptions/) | Defines additional options for the text watermark. |

### setText(String inputFileName, String outputFileName, int saveFormat, String watermarkText) {#setText-java.lang.String-java.lang.String-int-java.lang.String}
```
public static void setText(String inputFileName, String outputFileName, int saveFormat, String watermarkText)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
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


Adds a text watermark into the document.

 **Remarks:** 

If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), each page of the output will be saved as a separate file. The specified output file name will be used to generate file names for each part following the rule: outputFile\_partIndex.extension.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF file.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | The input file name. |
| outputFileName | java.lang.String | The output file name. |
| watermarkText | java.lang.String | Text that is displayed as a watermark. |

### setText(String inputFileName, String outputFileName, String watermarkText, TextWatermarkOptions options) {#setText-java.lang.String-java.lang.String-java.lang.String-com.aspose.words.TextWatermarkOptions}
```
public static void setText(String inputFileName, String outputFileName, String watermarkText, TextWatermarkOptions options)
```


Adds a text watermark into the document with options.

 **Remarks:** 

If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), each page of the output will be saved as a separate file. The specified output file name will be used to generate file names for each part following the rule: outputFile\_partIndex.extension.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF file.

 **Examples:** 

Shows how to insert watermark text to the document.

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
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | The input file name. |
| outputFileName | java.lang.String | The output file name. |
| watermarkText | java.lang.String | Text that is displayed as a watermark. |
| options | [TextWatermarkOptions](../../com.aspose.words/textwatermarkoptions/) | Defines additional options for the text watermark. |

### setWatermarkToImages(InputStream inputStream, ImageSaveOptions saveOptions, InputStream watermarkImageStream) {#setWatermarkToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.io.InputStream}
```
public static OutputStream[] setWatermarkToImages(InputStream inputStream, ImageSaveOptions saveOptions, InputStream watermarkImageStream)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) |  |
| watermarkImageStream | java.io.InputStream |  |

**Returns:**
java.io.OutputStream[]
### setWatermarkToImages(InputStream inputStream, ImageSaveOptions saveOptions, InputStream watermarkImageStream, ImageWatermarkOptions options) {#setWatermarkToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.io.InputStream-com.aspose.words.ImageWatermarkOptions}
```
public static OutputStream[] setWatermarkToImages(InputStream inputStream, ImageSaveOptions saveOptions, InputStream watermarkImageStream, ImageWatermarkOptions options)
```


Adds an image watermark into the document with options. Renders the output to images.

 **Examples:** 

Shows how to insert watermark image to the document from a stream and save result to images.

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
| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream | The input stream. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | The save options. |
| watermarkImageStream | java.io.InputStream | Image stream that is displayed as a watermark. |
| options | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) | Defines additional options for the image watermark. |

**Returns:**
java.io.OutputStream[]
### setWatermarkToImages(InputStream inputStream, ImageSaveOptions saveOptions, String watermarkText) {#setWatermarkToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String}
```
public static OutputStream[] setWatermarkToImages(InputStream inputStream, ImageSaveOptions saveOptions, String watermarkText)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) |  |
| watermarkText | java.lang.String |  |

**Returns:**
java.io.OutputStream[]
### setWatermarkToImages(InputStream inputStream, ImageSaveOptions saveOptions, String watermarkText, TextWatermarkOptions options) {#setWatermarkToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String-com.aspose.words.TextWatermarkOptions}
```
public static OutputStream[] setWatermarkToImages(InputStream inputStream, ImageSaveOptions saveOptions, String watermarkText, TextWatermarkOptions options)
```


Adds a text watermark into the document with options. Renders the output to images.

 **Examples:** 

Shows how to insert watermark text to the document from the stream and save result to images.

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
| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream | The input file stream. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | The save options. |
| watermarkText | java.lang.String | Text that is displayed as a watermark. |
| options | [TextWatermarkOptions](../../com.aspose.words/textwatermarkoptions/) | Defines additional options for the text watermark. |

**Returns:**
java.io.OutputStream[]
### setWatermarkToImages(String inputFileName, ImageSaveOptions saveOptions, byte[] watermarkImageBytes) {#setWatermarkToImages-java.lang.String-com.aspose.words.ImageSaveOptions-byte}
```
public static OutputStream[] setWatermarkToImages(String inputFileName, ImageSaveOptions saveOptions, byte[] watermarkImageBytes)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) |  |
| watermarkImageBytes | byte[] |  |

**Returns:**
java.io.OutputStream[]
### setWatermarkToImages(String inputFileName, ImageSaveOptions saveOptions, byte[] watermarkImageBytes, ImageWatermarkOptions options) {#setWatermarkToImages-java.lang.String-com.aspose.words.ImageSaveOptions-byte---com.aspose.words.ImageWatermarkOptions}
```
public static OutputStream[] setWatermarkToImages(String inputFileName, ImageSaveOptions saveOptions, byte[] watermarkImageBytes, ImageWatermarkOptions options)
```


Adds an image watermark into the document with options. Renders the output to images.

 **Examples:** 

Shows how to insert watermark image to the document and save result to images.

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
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | The input file name. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | The save options. |
| watermarkImageBytes | byte[] | Image bytes that is displayed as a watermark. |
| options | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) | Defines additional options for the image watermark. |

**Returns:**
java.io.OutputStream[]
### setWatermarkToImages(String inputFileName, ImageSaveOptions saveOptions, String watermarkText) {#setWatermarkToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String}
```
public static OutputStream[] setWatermarkToImages(String inputFileName, ImageSaveOptions saveOptions, String watermarkText)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) |  |
| watermarkText | java.lang.String |  |

**Returns:**
java.io.OutputStream[]
### setWatermarkToImages(String inputFileName, ImageSaveOptions saveOptions, String watermarkText, TextWatermarkOptions options) {#setWatermarkToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String-com.aspose.words.TextWatermarkOptions}
```
public static OutputStream[] setWatermarkToImages(String inputFileName, ImageSaveOptions saveOptions, String watermarkText, TextWatermarkOptions options)
```


Adds a text watermark into the document with options. Renders the output to images.

 **Examples:** 

Shows how to insert watermark text to the document and save result to images.

```

 String doc = getMyDir() + "Big document.docx";
 String watermarkText = "This is a watermark";

 OutputStream[] images = Watermarker.setWatermarkToImages(doc, new ImageSaveOptions(SaveFormat.PNG), watermarkText);

 TextWatermarkOptions watermarkOptions = new TextWatermarkOptions();
 watermarkOptions.setColor(Color.RED);
 images = Watermarker.setWatermarkToImages(doc, new ImageSaveOptions(SaveFormat.PNG), watermarkText, watermarkOptions);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | The input file name. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | The save options. |
| watermarkText | java.lang.String | Text that is displayed as a watermark. |
| options | [TextWatermarkOptions](../../com.aspose.words/textwatermarkoptions/) | Defines additional options for the text watermark. |

**Returns:**
java.io.OutputStream[]
### to(OutputStream output, SaveOptions saveOptions) {#to-java.io.OutputStream-com.aspose.words.SaveOptions}
```
public Processor to(OutputStream output, SaveOptions saveOptions)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| output | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(OutputStream output, int saveFormat) {#to-java.io.OutputStream-int}
```
public Processor to(OutputStream output, int saveFormat)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| output | java.io.OutputStream |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(String output) {#to-java.lang.String}
```
public Processor to(String output)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| output | java.lang.String |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(String output, SaveOptions saveOptions) {#to-java.lang.String-com.aspose.words.SaveOptions}
```
public Processor to(String output, SaveOptions saveOptions)
```


Specifies output file for the processor.

 **Remarks:** 

If the output consists of multiple files, the specified output file name is used to generate the file name for each part following the rule: 'outputFile\_partIndex.extension'.

 **Examples:** 

Shows how to convert documents with a single line of code using context.

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

Shows how to merge documents into a single output document using context.

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

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| output | java.lang.String | Output file name. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Optional save options. If not specified, save format is determined by the file extension. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified output file.
### to(String output, int saveFormat) {#to-java.lang.String-int}
```
public Processor to(String output, int saveFormat)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| output | java.lang.String |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(ArrayList output, SaveOptions saveOptions) {#to-java.util.ArrayList-com.aspose.words.SaveOptions}
```
public Processor to(ArrayList output, SaveOptions saveOptions)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| output | java.util.ArrayList |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(ArrayList output, int saveFormat) {#to-java.util.ArrayList-int}
```
public Processor to(ArrayList output, int saveFormat)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| output | java.util.ArrayList |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### toOutput(ArrayList output, SaveOptions saveOptions) {#toOutput-java.util.ArrayList-com.aspose.words.SaveOptions}
```
public Processor toOutput(ArrayList output, SaveOptions saveOptions)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| output | java.util.ArrayList |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### toOutput(ArrayList output, int saveFormat) {#toOutput-java.util.ArrayList-int}
```
public Processor toOutput(ArrayList output, int saveFormat)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| output | java.util.ArrayList |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
