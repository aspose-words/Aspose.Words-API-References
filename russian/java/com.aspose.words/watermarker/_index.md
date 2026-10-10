---
title: "Watermarker"
linktitle: "Watermarker"
second_title: "Aspose.Words для Java"
description: "Предоставляет методы, предназначенные для вставки водяных знаков в документы на Java."
type: docs
weight: 724
url: /ru/java/com.aspose.words/watermarker/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Processor](../../com.aspose.words/processor/)
```
public class Watermarker extends Processor
```

Предоставляет методы, предназначенные для вставки водяных знаков в документы.
## Методы

| Метод | Описание |
| --- | --- |
| [create(WatermarkerContext context)](#create-com.aspose.words.WatermarkerContext) | Создаёт новый экземпляр процессора watermarker. |
| [execute()](#execute) | Выполнить действие процессора. |
| [from(InputStream input)](#from-java.io.InputStream) | Указывает входной документ для обработки. |
| [from(InputStream input, LoadOptions loadOptions)](#from-java.io.InputStream-com.aspose.words.LoadOptions) | Указывает входной документ для обработки. |
| [from(String input)](#from-java.lang.String) | Указывает входной документ для обработки. |
| [from(String input, LoadOptions loadOptions)](#from-java.lang.String-com.aspose.words.LoadOptions) | Указывает входной документ для обработки. |
| [setImage(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, BufferedImage watermarkImage)](#setImage-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.awt.image.BufferedImage) |  |
| [setImage(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, BufferedImage watermarkImage, ImageWatermarkOptions options)](#setImage-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.awt.image.BufferedImage-com.aspose.words.ImageWatermarkOptions) |  |
| [setImage(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, InputStream watermarkImageStream)](#setImage-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.io.InputStream) |  |
| [setImage(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, InputStream watermarkImageStream, ImageWatermarkOptions options)](#setImage-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.io.InputStream-com.aspose.words.ImageWatermarkOptions) |  |
| [setImage(InputStream inputStream, OutputStream outputStream, int saveFormat, BufferedImage watermarkImage)](#setImage-java.io.InputStream-java.io.OutputStream-int-java.awt.image.BufferedImage) |  |
| [setImage(InputStream inputStream, OutputStream outputStream, int saveFormat, BufferedImage watermarkImage, ImageWatermarkOptions options)](#setImage-java.io.InputStream-java.io.OutputStream-int-java.awt.image.BufferedImage-com.aspose.words.ImageWatermarkOptions) |  |
| [setImage(InputStream inputStream, OutputStream outputStream, int saveFormat, InputStream watermarkImageStream)](#setImage-java.io.InputStream-java.io.OutputStream-int-java.io.InputStream) |  |
| [setImage(InputStream inputStream, OutputStream outputStream, int saveFormat, InputStream watermarkImageStream, ImageWatermarkOptions options)](#setImage-java.io.InputStream-java.io.OutputStream-int-java.io.InputStream-com.aspose.words.ImageWatermarkOptions) |  |
| [setImage(String inputFileName, String outputFileName, SaveOptions saveOptions, String watermarkImageFileName)](#setImage-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String) | Добавляет изображение‑водяной знак в документ с параметрами и указанным форматом сохранения. |
| [setImage(String inputFileName, String outputFileName, SaveOptions saveOptions, String watermarkImageFileName, ImageWatermarkOptions options)](#setImage-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String-com.aspose.words.ImageWatermarkOptions) | Добавляет изображение‑водяной знак в документ с параметрами и указанным форматом сохранения. |
| [setImage(String inputFileName, String outputFileName, int saveFormat, String watermarkImageFileName)](#setImage-java.lang.String-java.lang.String-int-java.lang.String) |  |
| [setImage(String inputFileName, String outputFileName, int saveFormat, String watermarkImageFileName, ImageWatermarkOptions options)](#setImage-java.lang.String-java.lang.String-int-java.lang.String-com.aspose.words.ImageWatermarkOptions) |  |
| [setImage(String inputFileName, String outputFileName, String watermarkImageFileName)](#setImage-java.lang.String-java.lang.String-java.lang.String) | Добавляет изображение‑водяной знак в документ. |
| [setImage(String inputFileName, String outputFileName, String watermarkImageFileName, ImageWatermarkOptions options)](#setImage-java.lang.String-java.lang.String-java.lang.String-com.aspose.words.ImageWatermarkOptions) | Добавляет изображение‑водяной знак в документ с параметрами. |
| [setText(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, String watermarkText)](#setText-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.String) |  |
| [setText(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, String watermarkText, TextWatermarkOptions options)](#setText-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.String-com.aspose.words.TextWatermarkOptions) |  |
| [setText(InputStream inputStream, OutputStream outputStream, int saveFormat, String watermarkText)](#setText-java.io.InputStream-java.io.OutputStream-int-java.lang.String) |  |
| [setText(InputStream inputStream, OutputStream outputStream, int saveFormat, String watermarkText, TextWatermarkOptions options)](#setText-java.io.InputStream-java.io.OutputStream-int-java.lang.String-com.aspose.words.TextWatermarkOptions) |  |
| [setText(String inputFileName, String outputFileName, SaveOptions saveOptions, String watermarkText)](#setText-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String) | Добавляет текстовый водяной знак в документ с параметрами и указанным форматом сохранения. |
| [setText(String inputFileName, String outputFileName, SaveOptions saveOptions, String watermarkText, TextWatermarkOptions options)](#setText-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String-com.aspose.words.TextWatermarkOptions) | Добавляет текстовый водяной знак в документ с параметрами и указанным форматом сохранения. |
| [setText(String inputFileName, String outputFileName, int saveFormat, String watermarkText)](#setText-java.lang.String-java.lang.String-int-java.lang.String) |  |
| [setText(String inputFileName, String outputFileName, int saveFormat, String watermarkText, TextWatermarkOptions options)](#setText-java.lang.String-java.lang.String-int-java.lang.String-com.aspose.words.TextWatermarkOptions) |  |
| [setText(String inputFileName, String outputFileName, String watermarkText)](#setText-java.lang.String-java.lang.String-java.lang.String) | Добавляет текстовый водяной знак в документ. |
| [setText(String inputFileName, String outputFileName, String watermarkText, TextWatermarkOptions options)](#setText-java.lang.String-java.lang.String-java.lang.String-com.aspose.words.TextWatermarkOptions) | Добавляет текстовый водяной знак в документ с параметрами. |
| [setWatermarkToImages(InputStream inputStream, ImageSaveOptions saveOptions, InputStream watermarkImageStream)](#setWatermarkToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.io.InputStream) | Добавляет изображение‑водяной знак в документ с параметрами. |
| [setWatermarkToImages(InputStream inputStream, ImageSaveOptions saveOptions, InputStream watermarkImageStream, ImageWatermarkOptions options)](#setWatermarkToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.io.InputStream-com.aspose.words.ImageWatermarkOptions) | Добавляет изображение‑водяной знак в документ с параметрами. |
| [setWatermarkToImages(InputStream inputStream, ImageSaveOptions saveOptions, String watermarkText)](#setWatermarkToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String) | Добавляет текстовый водяной знак в документ с параметрами. |
| [setWatermarkToImages(InputStream inputStream, ImageSaveOptions saveOptions, String watermarkText, TextWatermarkOptions options)](#setWatermarkToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String-com.aspose.words.TextWatermarkOptions) | Добавляет текстовый водяной знак в документ с параметрами. |
| [setWatermarkToImages(String inputFileName, ImageSaveOptions saveOptions, byte[] watermarkImageBytes)](#setWatermarkToImages-java.lang.String-com.aspose.words.ImageSaveOptions-byte) | Добавляет изображение‑водяной знак в документ с параметрами. |
| [setWatermarkToImages(String inputFileName, ImageSaveOptions saveOptions, byte[] watermarkImageBytes, ImageWatermarkOptions options)](#setWatermarkToImages-java.lang.String-com.aspose.words.ImageSaveOptions-byte---com.aspose.words.ImageWatermarkOptions) | Добавляет изображение‑водяной знак в документ с параметрами. |
| [setWatermarkToImages(String inputFileName, ImageSaveOptions saveOptions, String watermarkText)](#setWatermarkToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String) | Добавляет текстовый водяной знак в документ с параметрами. |
| [setWatermarkToImages(String inputFileName, ImageSaveOptions saveOptions, String watermarkText, TextWatermarkOptions options)](#setWatermarkToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String-com.aspose.words.TextWatermarkOptions) | Добавляет текстовый водяной знак в документ с параметрами. |
| [to(OutputStream output, SaveOptions saveOptions)](#to-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [to(OutputStream output, int saveFormat)](#to-java.io.OutputStream-int) |  |
| [to(String output)](#to-java.lang.String) | Указывает выходной файл для процессора. |
| [to(String output, SaveOptions saveOptions)](#to-java.lang.String-com.aspose.words.SaveOptions) | Указывает выходной файл для процессора. |
| [to(String output, int saveFormat)](#to-java.lang.String-int) |  |
| [to(ArrayList output, SaveOptions saveOptions)](#to-java.util.ArrayList-com.aspose.words.SaveOptions) |  |
| [to(ArrayList output, int saveFormat)](#to-java.util.ArrayList-int) |  |
| [toOutput(ArrayList output, SaveOptions saveOptions)](#toOutput-java.util.ArrayList-com.aspose.words.SaveOptions) |  |
| [toOutput(ArrayList output, int saveFormat)](#toOutput-java.util.ArrayList-int) |  |
### create(WatermarkerContext context) {#create-com.aspose.words.WatermarkerContext}
```
public static Watermarker create(WatermarkerContext context)
```


Создаёт новый экземпляр процессора watermarker.

 **Examples:** 

Показывает, как вставить текст водяного знака в документ, используя контекст.

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

Показывает, как вставить текст водяного знака в документ из потока, используя контекст.

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

Показывает, как вставить изображение водяного знака в документ, используя контекст.

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

Показывает, как вставить изображение водяного знака в документ из потока, используя контекст.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| context | [WatermarkerContext](../../com.aspose.words/watermarkercontext/) |  |

**Returns:**
[Watermarker](../../com.aspose.words/watermarker/)
### execute() {#execute}
```
public void execute()
```


Выполнить действие процессора.

 **Examples:** 

Показывает, как объединить документы в один результирующий документ, используя контекст.

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

Показывает, как объединить документы из потока в один результирующий документ, используя контекст.

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

Показывает, как конвертировать документы одной строкой кода, используя контекст.

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

Показывает, как конвертировать документы из потока одной строкой кода, используя контекст.

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


Указывает входной документ для обработки.

 **Remarks:** 

Если процессор принимает в качестве входа только один файл, будет обработан только последний указанный файл. Процессор [Merger](../../com.aspose.words/merger/) принимает несколько файлов в качестве входа, в результате все указанные документы будут объединены. Процессор [Converter](../../com.aspose.words/converter/) принимает в качестве входа только один файл, поэтому будет преобразован только последний указанный файл.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| ввод | java.io.InputStream | Поток входного документа. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file stream.
### from(InputStream input, LoadOptions loadOptions) {#from-java.io.InputStream-com.aspose.words.LoadOptions}
```
public Processor from(InputStream input, LoadOptions loadOptions)
```


Указывает входной документ для обработки.

 **Remarks:** 

Если процессор принимает в качестве входа только один файл, будет обработан только последний указанный файл. Процессор [Merger](../../com.aspose.words/merger/) принимает несколько файлов в качестве входа, в результате все указанные документы будут объединены. Процессор [Converter](../../com.aspose.words/converter/) принимает в качестве входа только один файл, поэтому будет преобразован только последний указанный файл.

 **Examples:** 

Показывает, как объединить документы из потока в один результирующий документ, используя контекст.

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

Показывает, как конвертировать документы из потока одной строкой кода, используя контекст.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| ввод | java.io.InputStream | Поток входного документа. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Необязательные параметры загрузки, используемые для загрузки документа. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file stream.
### from(String input) {#from-java.lang.String}
```
public Processor from(String input)
```


Указывает входной документ для обработки.

 **Remarks:** 

Если процессор принимает в качестве входа только один файл, будет обработан только последний указанный файл. Процессор [Merger](../../com.aspose.words/merger/) принимает несколько файлов в качестве входа, в результате все указанные документы будут объединены. Процессор [Converter](../../com.aspose.words/converter/) принимает в качестве входа только один файл, поэтому будет преобразован только последний указанный файл.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| ввод | java.lang.String | Имя файла входного документа. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file.
### from(String input, LoadOptions loadOptions) {#from-java.lang.String-com.aspose.words.LoadOptions}
```
public Processor from(String input, LoadOptions loadOptions)
```


Указывает входной документ для обработки.

 **Remarks:** 

Если процессор принимает в качестве входа только один файл, будет обработан только последний указанный файл. Процессор [Merger](../../com.aspose.words/merger/) принимает несколько файлов в качестве входа, в результате все указанные документы будут объединены. Процессор [Converter](../../com.aspose.words/converter/) принимает в качестве входа только один файл, поэтому будет преобразован только последний указанный файл.

 **Examples:** 

Показывает, как объединить документы в один результирующий документ, используя контекст.

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

Показывает, как конвертировать документы одной строкой кода, используя контекст.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| ввод | java.lang.String | Имя файла входного документа. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Необязательные параметры загрузки, используемые для загрузки документа. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file.
### setImage(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, BufferedImage watermarkImage) {#setImage-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.awt.image.BufferedImage}
```
public static void setImage(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, BufferedImage watermarkImage)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
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


Добавляет изображение‑водяной знак в документ с параметрами и указанным форматом сохранения.

 **Remarks:** 

Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница вывода будет сохранена в отдельный файл. Указанное имя выходного файла будет использовано для генерации имён файлов для каждой части по правилу: outputFile\_partIndex.extension.

Если формат вывода — TIFF, вывод будет сохранён в один многостраничный файл TIFF.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | java.lang.String | Имя входного файла. |
| outputFileName | java.lang.String | Имя выходного файла. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Параметры сохранения. |
| watermarkImageFileName | java.lang.String | Изображение, отображаемое как водяной знак. |

### setImage(String inputFileName, String outputFileName, SaveOptions saveOptions, String watermarkImageFileName, ImageWatermarkOptions options) {#setImage-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String-com.aspose.words.ImageWatermarkOptions}
```
public static void setImage(String inputFileName, String outputFileName, SaveOptions saveOptions, String watermarkImageFileName, ImageWatermarkOptions options)
```


Добавляет изображение‑водяной знак в документ с параметрами и указанным форматом сохранения.

 **Remarks:** 

Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница вывода будет сохранена в отдельный файл. Указанное имя выходного файла будет использовано для генерации имён файлов для каждой части по правилу: outputFile\_partIndex.extension.

Если формат вывода — TIFF, вывод будет сохранён в один многостраничный файл TIFF.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | java.lang.String | Имя входного файла. |
| outputFileName | java.lang.String | Имя выходного файла. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Параметры сохранения. |
| watermarkImageFileName | java.lang.String | Изображение, отображаемое как водяной знак. |
| options | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) | Определяет дополнительные параметры для изображения водяного знака. |

### setImage(String inputFileName, String outputFileName, int saveFormat, String watermarkImageFileName) {#setImage-java.lang.String-java.lang.String-int-java.lang.String}
```
public static void setImage(String inputFileName, String outputFileName, int saveFormat, String watermarkImageFileName)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
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


Добавляет изображение‑водяной знак в документ.

 **Remarks:** 

Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница вывода будет сохранена в отдельный файл. Указанное имя выходного файла будет использовано для генерации имён файлов для каждой части по правилу: outputFile\_partIndex.extension.

Если формат вывода — TIFF, вывод будет сохранён в один многостраничный файл TIFF.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | java.lang.String | Имя входного файла. |
| outputFileName | java.lang.String | Имя выходного файла. |
| watermarkImageFileName | java.lang.String | Изображение, отображаемое как водяной знак. |

### setImage(String inputFileName, String outputFileName, String watermarkImageFileName, ImageWatermarkOptions options) {#setImage-java.lang.String-java.lang.String-java.lang.String-com.aspose.words.ImageWatermarkOptions}
```
public static void setImage(String inputFileName, String outputFileName, String watermarkImageFileName, ImageWatermarkOptions options)
```


Добавляет изображение‑водяной знак в документ с параметрами.

 **Remarks:** 

Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница вывода будет сохранена в отдельный файл. Указанное имя выходного файла будет использовано для генерации имён файлов для каждой части по правилу: outputFile\_partIndex.extension.

Если формат вывода — TIFF, вывод будет сохранён в один многостраничный файл TIFF.

 **Examples:** 

Показывает, как вставить изображение водяного знака в документ.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | java.lang.String | Имя входного файла. |
| outputFileName | java.lang.String | Имя выходного файла. |
| watermarkImageFileName | java.lang.String | Изображение, отображаемое как водяной знак. |
| options | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) | Определяет дополнительные параметры для изображения водяного знака. |

### setText(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, String watermarkText) {#setText-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.String}
```
public static void setText(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, String watermarkText)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
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


Добавляет текстовый водяной знак в документ с параметрами и указанным форматом сохранения.

 **Remarks:** 

Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница вывода будет сохранена в отдельный файл. Указанное имя выходного файла будет использовано для генерации имён файлов для каждой части по правилу: outputFile\_partIndex.extension.

Если формат вывода — TIFF, вывод будет сохранён в один многостраничный файл TIFF.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | java.lang.String | Имя входного файла. |
| outputFileName | java.lang.String | Имя выходного файла. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Параметры сохранения. |
| watermarkText | java.lang.String | Текст, отображаемый как водяной знак. |

### setText(String inputFileName, String outputFileName, SaveOptions saveOptions, String watermarkText, TextWatermarkOptions options) {#setText-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String-com.aspose.words.TextWatermarkOptions}
```
public static void setText(String inputFileName, String outputFileName, SaveOptions saveOptions, String watermarkText, TextWatermarkOptions options)
```


Добавляет текстовый водяной знак в документ с параметрами и указанным форматом сохранения.

 **Remarks:** 

Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница вывода будет сохранена в отдельный файл. Указанное имя выходного файла будет использовано для генерации имён файлов для каждой части по правилу: outputFile\_partIndex.extension.

Если формат вывода — TIFF, вывод будет сохранён в один многостраничный файл TIFF.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | java.lang.String | Имя входного файла. |
| outputFileName | java.lang.String | Имя выходного файла. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Параметры сохранения. |
| watermarkText | java.lang.String | Текст, отображаемый как водяной знак. |
| options | [TextWatermarkOptions](../../com.aspose.words/textwatermarkoptions/) | Определяет дополнительные параметры для текста водяного знака. |

### setText(String inputFileName, String outputFileName, int saveFormat, String watermarkText) {#setText-java.lang.String-java.lang.String-int-java.lang.String}
```
public static void setText(String inputFileName, String outputFileName, int saveFormat, String watermarkText)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
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


Добавляет текстовый водяной знак в документ.

 **Remarks:** 

Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница вывода будет сохранена в отдельный файл. Указанное имя выходного файла будет использовано для генерации имён файлов для каждой части по правилу: outputFile\_partIndex.extension.

Если формат вывода — TIFF, вывод будет сохранён в один многостраничный файл TIFF.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | java.lang.String | Имя входного файла. |
| outputFileName | java.lang.String | Имя выходного файла. |
| watermarkText | java.lang.String | Текст, отображаемый как водяной знак. |

### setText(String inputFileName, String outputFileName, String watermarkText, TextWatermarkOptions options) {#setText-java.lang.String-java.lang.String-java.lang.String-com.aspose.words.TextWatermarkOptions}
```
public static void setText(String inputFileName, String outputFileName, String watermarkText, TextWatermarkOptions options)
```


Добавляет текстовый водяной знак в документ с параметрами.

 **Remarks:** 

Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница вывода будет сохранена в отдельный файл. Указанное имя выходного файла будет использовано для генерации имён файлов для каждой части по правилу: outputFile\_partIndex.extension.

Если формат вывода — TIFF, вывод будет сохранён в один многостраничный файл TIFF.

 **Examples:** 

Показывает, как вставить текст водяного знака в документ.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | java.lang.String | Имя входного файла. |
| outputFileName | java.lang.String | Имя выходного файла. |
| watermarkText | java.lang.String | Текст, отображаемый как водяной знак. |
| options | [TextWatermarkOptions](../../com.aspose.words/textwatermarkoptions/) | Определяет дополнительные параметры для текста водяного знака. |

### setWatermarkToImages(InputStream inputStream, ImageSaveOptions saveOptions, InputStream watermarkImageStream) {#setWatermarkToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.io.InputStream}
```
public static OutputStream[] setWatermarkToImages(InputStream inputStream, ImageSaveOptions saveOptions, InputStream watermarkImageStream)
```


Добавляет изображение водяного знака в документ с параметрами. Рендерит вывод в изображения.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | java.io.InputStream | Входной поток. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Параметры сохранения. |
| watermarkImageStream | java.io.InputStream | Поток изображения, отображаемый как водяной знак. |

**Returns:**
java.io.OutputStream[]
### setWatermarkToImages(InputStream inputStream, ImageSaveOptions saveOptions, InputStream watermarkImageStream, ImageWatermarkOptions options) {#setWatermarkToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.io.InputStream-com.aspose.words.ImageWatermarkOptions}
```
public static OutputStream[] setWatermarkToImages(InputStream inputStream, ImageSaveOptions saveOptions, InputStream watermarkImageStream, ImageWatermarkOptions options)
```


Добавляет изображение водяного знака в документ с параметрами. Рендерит вывод в изображения.

 **Examples:** 

Показывает, как вставить изображение водяного знака в документ из потока и сохранить результат в изображения.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | java.io.InputStream | Входной поток. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Параметры сохранения. |
| watermarkImageStream | java.io.InputStream | Поток изображения, отображаемый как водяной знак. |
| options | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) | Определяет дополнительные параметры для изображения водяного знака. |

**Returns:**
java.io.OutputStream[]
### setWatermarkToImages(InputStream inputStream, ImageSaveOptions saveOptions, String watermarkText) {#setWatermarkToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String}
```
public static OutputStream[] setWatermarkToImages(InputStream inputStream, ImageSaveOptions saveOptions, String watermarkText)
```


Добавляет текстовый водяной знак в документ с параметрами. Рендерит вывод в изображения.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | java.io.InputStream | Входной поток файла. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Параметры сохранения. |
| watermarkText | java.lang.String | Текст, отображаемый как водяной знак. |

**Returns:**
java.io.OutputStream[]
### setWatermarkToImages(InputStream inputStream, ImageSaveOptions saveOptions, String watermarkText, TextWatermarkOptions options) {#setWatermarkToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String-com.aspose.words.TextWatermarkOptions}
```
public static OutputStream[] setWatermarkToImages(InputStream inputStream, ImageSaveOptions saveOptions, String watermarkText, TextWatermarkOptions options)
```


Добавляет текстовый водяной знак в документ с параметрами. Рендерит вывод в изображения.

 **Examples:** 

Показывает, как вставить текст водяного знака в документ из потока и сохранить результат в изображения.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | java.io.InputStream | Входной поток файла. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Параметры сохранения. |
| watermarkText | java.lang.String | Текст, отображаемый как водяной знак. |
| options | [TextWatermarkOptions](../../com.aspose.words/textwatermarkoptions/) | Определяет дополнительные параметры для текста водяного знака. |

**Returns:**
java.io.OutputStream[]
### setWatermarkToImages(String inputFileName, ImageSaveOptions saveOptions, byte[] watermarkImageBytes) {#setWatermarkToImages-java.lang.String-com.aspose.words.ImageSaveOptions-byte}
```
public static OutputStream[] setWatermarkToImages(String inputFileName, ImageSaveOptions saveOptions, byte[] watermarkImageBytes)
```


Добавляет изображение водяного знака в документ с параметрами. Рендерит вывод в изображения.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | java.lang.String | Имя входного файла. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Параметры сохранения. |
| watermarkImageBytes | byte[] | Байты изображения, отображаемые как водяной знак. |

**Returns:**
java.io.OutputStream[]
### setWatermarkToImages(String inputFileName, ImageSaveOptions saveOptions, byte[] watermarkImageBytes, ImageWatermarkOptions options) {#setWatermarkToImages-java.lang.String-com.aspose.words.ImageSaveOptions-byte---com.aspose.words.ImageWatermarkOptions}
```
public static OutputStream[] setWatermarkToImages(String inputFileName, ImageSaveOptions saveOptions, byte[] watermarkImageBytes, ImageWatermarkOptions options)
```


Добавляет изображение водяного знака в документ с параметрами. Рендерит вывод в изображения.

 **Examples:** 

Показывает, как вставить изображение водяного знака в документ и сохранить результат в изображения.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | java.lang.String | Имя входного файла. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Параметры сохранения. |
| watermarkImageBytes | byte[] | Байты изображения, отображаемые как водяной знак. |
| options | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) | Определяет дополнительные параметры для изображения водяного знака. |

**Returns:**
java.io.OutputStream[]
### setWatermarkToImages(String inputFileName, ImageSaveOptions saveOptions, String watermarkText) {#setWatermarkToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String}
```
public static OutputStream[] setWatermarkToImages(String inputFileName, ImageSaveOptions saveOptions, String watermarkText)
```


Добавляет текстовый водяной знак в документ с параметрами. Рендерит вывод в изображения.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | java.lang.String | Имя входного файла. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Параметры сохранения. |
| watermarkText | java.lang.String | Текст, отображаемый как водяной знак. |

**Returns:**
java.io.OutputStream[]
### setWatermarkToImages(String inputFileName, ImageSaveOptions saveOptions, String watermarkText, TextWatermarkOptions options) {#setWatermarkToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String-com.aspose.words.TextWatermarkOptions}
```
public static OutputStream[] setWatermarkToImages(String inputFileName, ImageSaveOptions saveOptions, String watermarkText, TextWatermarkOptions options)
```


Добавляет текстовый водяной знак в документ с параметрами. Рендерит вывод в изображения.

 **Examples:** 

Показывает, как вставить текст водяного знака в документ и сохранить результат в изображения.

```

 String doc = getMyDir() + "Big document.docx";
 String watermarkText = "This is a watermark";

 OutputStream[] images = Watermarker.setWatermarkToImages(doc, new ImageSaveOptions(SaveFormat.PNG), watermarkText);

 TextWatermarkOptions watermarkOptions = new TextWatermarkOptions();
 watermarkOptions.setColor(Color.RED);
 images = Watermarker.setWatermarkToImages(doc, new ImageSaveOptions(SaveFormat.PNG), watermarkText, watermarkOptions);
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | java.lang.String | Имя входного файла. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Параметры сохранения. |
| watermarkText | java.lang.String | Текст, отображаемый как водяной знак. |
| options | [TextWatermarkOptions](../../com.aspose.words/textwatermarkoptions/) | Определяет дополнительные параметры для текста водяного знака. |

**Returns:**
java.io.OutputStream[]
### to(OutputStream output, SaveOptions saveOptions) {#to-java.io.OutputStream-com.aspose.words.SaveOptions}
```
public Processor to(OutputStream output, SaveOptions saveOptions)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| вывод | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(OutputStream output, int saveFormat) {#to-java.io.OutputStream-int}
```
public Processor to(OutputStream output, int saveFormat)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| вывод | java.io.OutputStream |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(String output) {#to-java.lang.String}
```
public Processor to(String output)
```


Указывает выходной файл для процессора.

 **Remarks:** 

Если вывод состоит из нескольких файлов, указанное имя выходного файла используется для генерации имени файла каждой части по правилу: 'outputFile\_partIndex.extension'.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| вывод | java.lang.String | Имя выходного файла. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified output file.
### to(String output, SaveOptions saveOptions) {#to-java.lang.String-com.aspose.words.SaveOptions}
```
public Processor to(String output, SaveOptions saveOptions)
```


Указывает выходной файл для процессора.

 **Remarks:** 

Если вывод состоит из нескольких файлов, указанное имя выходного файла используется для генерации имени файла каждой части по правилу: 'outputFile\_partIndex.extension'.

 **Examples:** 

Показывает, как объединить документы в один результирующий документ, используя контекст.

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

Показывает, как конвертировать документы одной строкой кода, используя контекст.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| вывод | java.lang.String | Имя выходного файла. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Необязательные параметры сохранения. Если не указано, формат сохраняемого файла определяется расширением. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified output file.
### to(String output, int saveFormat) {#to-java.lang.String-int}
```
public Processor to(String output, int saveFormat)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| вывод | java.lang.String |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(ArrayList output, SaveOptions saveOptions) {#to-java.util.ArrayList-com.aspose.words.SaveOptions}
```
public Processor to(ArrayList output, SaveOptions saveOptions)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| вывод | java.util.ArrayList |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(ArrayList output, int saveFormat) {#to-java.util.ArrayList-int}
```
public Processor to(ArrayList output, int saveFormat)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| вывод | java.util.ArrayList |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### toOutput(ArrayList output, SaveOptions saveOptions) {#toOutput-java.util.ArrayList-com.aspose.words.SaveOptions}
```
public Processor toOutput(ArrayList output, SaveOptions saveOptions)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| вывод | java.util.ArrayList |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### toOutput(ArrayList output, int saveFormat) {#toOutput-java.util.ArrayList-int}
```
public Processor toOutput(ArrayList output, int saveFormat)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| вывод | java.util.ArrayList |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
