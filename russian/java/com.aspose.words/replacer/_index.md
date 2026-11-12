---
title: "Заменитель"
linktitle: "Заменитель"
second_title: "Aspose.Words для Java"
description: "Предоставляет методы, предназначенные для поиска и замены текста в документе на Java."
type: docs
weight: 567
url: /ru/java/com.aspose.words/replacer/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Processor](../../com.aspose.words/processor/)
```
public class Replacer extends Processor
```

Предоставляет методы, предназначенные для поиска и замены текста в документе.
## Методы

| Метод | Описание |
| --- | --- |
| [create(ReplacerContext context)](#create-com.aspose.words.ReplacerContext) | Создаёт новый экземпляр процессора заменителя. |
| [execute()](#execute) | Выполнить действие процессора. |
| [from(InputStream input)](#from-java.io.InputStream) | Указывает входной документ для обработки. |
| [from(InputStream input, LoadOptions loadOptions)](#from-java.io.InputStream-com.aspose.words.LoadOptions) | Указывает входной документ для обработки. |
| [from(String input)](#from-java.lang.String) | Указывает входной документ для обработки. |
| [from(String input, LoadOptions loadOptions)](#from-java.lang.String-com.aspose.words.LoadOptions) | Указывает входной документ для обработки. |
| [replace(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, String pattern, String replacement)](#replace-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.String-java.lang.String) |  |
| [replace(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, String pattern, String replacement, FindReplaceOptions options)](#replace-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions) |  |
| [replace(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Pattern pattern, String replacement)](#replace-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.util.regex.Pattern-java.lang.String) |  |
| [replace(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Pattern pattern, String replacement, FindReplaceOptions options)](#replace-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions) |  |
| [replace(InputStream inputStream, OutputStream outputStream, int saveFormat, String pattern, String replacement)](#replace-java.io.InputStream-java.io.OutputStream-int-java.lang.String-java.lang.String) |  |
| [replace(InputStream inputStream, OutputStream outputStream, int saveFormat, String pattern, String replacement, FindReplaceOptions options)](#replace-java.io.InputStream-java.io.OutputStream-int-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions) |  |
| [replace(InputStream inputStream, OutputStream outputStream, int saveFormat, Pattern pattern, String replacement)](#replace-java.io.InputStream-java.io.OutputStream-int-java.util.regex.Pattern-java.lang.String) |  |
| [replace(InputStream inputStream, OutputStream outputStream, int saveFormat, Pattern pattern, String replacement, FindReplaceOptions options)](#replace-java.io.InputStream-java.io.OutputStream-int-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions) |  |
| [replace(String inputFileName, String outputFileName, SaveOptions saveOptions, String pattern, String replacement)](#replace-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String-java.lang.String) | Заменяет все вхождения указанного шаблона строкового символа на строку‑замену во входном файле, используя указанный формат сохранения и дополнительные параметры. |
| [replace(String inputFileName, String outputFileName, SaveOptions saveOptions, String pattern, String replacement, FindReplaceOptions options)](#replace-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions) | Заменяет все вхождения указанного шаблона строкового символа на строку‑замену во входном файле, используя указанный формат сохранения и дополнительные параметры. |
| [replace(String inputFileName, String outputFileName, SaveOptions saveOptions, Pattern pattern, String replacement)](#replace-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.util.regex.Pattern-java.lang.String) | Заменяет все вхождения указанного шаблона строкового символа на строку‑замену во входном файле с использованием регулярного выражения, используя указанный формат сохранения и дополнительные параметры. |
| [replace(String inputFileName, String outputFileName, SaveOptions saveOptions, Pattern pattern, String replacement, FindReplaceOptions options)](#replace-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions) | Заменяет все вхождения указанного шаблона строкового символа на строку‑замену во входном файле с использованием регулярного выражения, используя указанный формат сохранения и дополнительные параметры. |
| [replace(String inputFileName, String outputFileName, int saveFormat, String pattern, String replacement)](#replace-java.lang.String-java.lang.String-int-java.lang.String-java.lang.String) |  |
| [replace(String inputFileName, String outputFileName, int saveFormat, String pattern, String replacement, FindReplaceOptions options)](#replace-java.lang.String-java.lang.String-int-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions) |  |
| [replace(String inputFileName, String outputFileName, int saveFormat, Pattern pattern, String replacement)](#replace-java.lang.String-java.lang.String-int-java.util.regex.Pattern-java.lang.String) |  |
| [replace(String inputFileName, String outputFileName, int saveFormat, Pattern pattern, String replacement, FindReplaceOptions options)](#replace-java.lang.String-java.lang.String-int-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions) |  |
| [replace(String inputFileName, String outputFileName, String pattern, String replacement)](#replace-java.lang.String-java.lang.String-java.lang.String-java.lang.String) | Заменяет все вхождения указанного шаблона строкового символа на строку‑замену во входном файле. |
| [replace(String inputFileName, String outputFileName, Pattern pattern, String replacement)](#replace-java.lang.String-java.lang.String-java.util.regex.Pattern-java.lang.String) | Заменяет все вхождения указанного шаблона строкового символа на строку‑замену во входном файле с использованием регулярного выражения. |
| [replaceToImages(InputStream inputStream, ImageSaveOptions saveOptions, String pattern, String replacement)](#replaceToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String-java.lang.String) | Заменяет все вхождения указанного шаблона строкового символа на строку‑замену во входном файле. |
| [replaceToImages(InputStream inputStream, ImageSaveOptions saveOptions, String pattern, String replacement, FindReplaceOptions options)](#replaceToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions) | Заменяет все вхождения указанного шаблона строкового символа на строку‑замену во входном файле. |
| [replaceToImages(InputStream inputStream, ImageSaveOptions saveOptions, Pattern pattern, String replacement)](#replaceToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.util.regex.Pattern-java.lang.String) | Заменяет все вхождения указанного шаблона регулярного выражения на строку‑замену во входном файле. |
| [replaceToImages(InputStream inputStream, ImageSaveOptions saveOptions, Pattern pattern, String replacement, FindReplaceOptions options)](#replaceToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions) | Заменяет все вхождения указанного шаблона регулярного выражения на строку‑замену во входном файле. |
| [replaceToImages(String inputFileName, ImageSaveOptions saveOptions, String pattern, String replacement)](#replaceToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String-java.lang.String) | Заменяет все вхождения указанного шаблона строкового символа на строку‑замену во входном файле. |
| [replaceToImages(String inputFileName, ImageSaveOptions saveOptions, String pattern, String replacement, FindReplaceOptions options)](#replaceToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions) | Заменяет все вхождения указанного шаблона строкового символа на строку‑замену во входном файле. |
| [replaceToImages(String inputFileName, ImageSaveOptions saveOptions, Pattern pattern, String replacement)](#replaceToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.util.regex.Pattern-java.lang.String) | Заменяет все вхождения указанного шаблона регулярного выражения на строку‑замену во входном файле. |
| [replaceToImages(String inputFileName, ImageSaveOptions saveOptions, Pattern pattern, String replacement, FindReplaceOptions options)](#replaceToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions) | Заменяет все вхождения указанного шаблона регулярного выражения на строку‑замену во входном файле. |
| [to(OutputStream output, SaveOptions saveOptions)](#to-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [to(OutputStream output, int saveFormat)](#to-java.io.OutputStream-int) |  |
| [to(String output)](#to-java.lang.String) | Указывает выходной файл для процессора. |
| [to(String output, SaveOptions saveOptions)](#to-java.lang.String-com.aspose.words.SaveOptions) | Указывает выходной файл для процессора. |
| [to(String output, int saveFormat)](#to-java.lang.String-int) |  |
| [to(ArrayList output, SaveOptions saveOptions)](#to-java.util.ArrayList-com.aspose.words.SaveOptions) |  |
| [to(ArrayList output, int saveFormat)](#to-java.util.ArrayList-int) |  |
| [toOutput(ArrayList output, SaveOptions saveOptions)](#toOutput-java.util.ArrayList-com.aspose.words.SaveOptions) |  |
| [toOutput(ArrayList output, int saveFormat)](#toOutput-java.util.ArrayList-int) |  |
### create(ReplacerContext context) {#create-com.aspose.words.ReplacerContext}
```
public static Replacer create(ReplacerContext context)
```


Создаёт новый экземпляр процессора заменителя.

 **Examples:** 

Показывает, как заменить строку в документе, используя контекст.

```

 // There is a several ways to replace string in the document:
 String doc = getMyDir() + "Footer.docx";
 String pattern = "(C)2006 Aspose Pty Ltd.";
 String replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

 ReplacerContext replacerContext = new ReplacerContext();
 replacerContext.setReplacement(pattern, replacement);
 replacerContext.getFindReplaceOptions().setFindWholeWordsOnly(false);

 Replacer.create(replacerContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ReplaceContext.docx")
         .execute();
 
```

Показывает, как заменить строку в документе, используя документы из потока, используя контекст.

```

 // There is a several ways to replace string in the document using documents from the stream:
 String pattern = "(C)2006 Aspose Pty Ltd.";
 String replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Footer.docx")) {
     ReplacerContext replacerContext = new ReplacerContext();
     replacerContext.setReplacement(pattern, replacement);
     replacerContext.getFindReplaceOptions().setFindWholeWordsOnly(false);

     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.ReplaceContextStream.docx")) {
         Replacer.create(replacerContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```

Показывает, как заменить строку с помощью regex в документе, используя контекст.

```

 // There is a several ways to replace string with regex in the document:
 String doc = getMyDir() + "Footer.docx";
 Pattern pattern = Pattern.compile("gr(a|e)y");
 String replacement = "lavender";

 ReplacerContext replacerContext = new ReplacerContext();
 replacerContext.setReplacement(pattern, replacement);
 replacerContext.getFindReplaceOptions().setFindWholeWordsOnly(false);

 Replacer.create(replacerContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ReplaceContextRegex.docx")
         .execute();
 
```

Показывает, как заменить строку с помощью regex в документе, используя документы из потока, используя контекст.

```

 // There is a several ways to replace string with regex in the document using documents from the stream:
 Pattern pattern = Pattern.compile("gr(a|e)y");
 String replacement = "lavender";

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Replace regex.docx")) {
     ReplacerContext replacerContext = new ReplacerContext();
     replacerContext.setReplacement(pattern, replacement);
     replacerContext.getFindReplaceOptions().setFindWholeWordsOnly(false);

     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.ReplaceContextStreamRegex.docx")) {
         Replacer.create(replacerContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| context | [ReplacerContext](../../com.aspose.words/replacercontext/) |  |

**Returns:**
[Replacer](../../com.aspose.words/replacer/)
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
### replace(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, String pattern, String replacement) {#replace-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.String-java.lang.String}
```
public static int replace(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, String pattern, String replacement)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| шаблон | java.lang.String |  |
| замена | java.lang.String |  |

**Returns:**
int
### replace(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, String pattern, String replacement, FindReplaceOptions options) {#replace-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions}
```
public static int replace(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, String pattern, String replacement, FindReplaceOptions options)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| шаблон | java.lang.String |  |
| замена | java.lang.String |  |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) |  |

**Returns:**
int
### replace(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Pattern pattern, String replacement) {#replace-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.util.regex.Pattern-java.lang.String}
```
public static int replace(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Pattern pattern, String replacement)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| шаблон | java.util.regex.Pattern |  |
| замена | java.lang.String |  |

**Returns:**
int
### replace(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Pattern pattern, String replacement, FindReplaceOptions options) {#replace-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions}
```
public static int replace(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Pattern pattern, String replacement, FindReplaceOptions options)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| шаблон | java.util.regex.Pattern |  |
| замена | java.lang.String |  |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) |  |

**Returns:**
int
### replace(InputStream inputStream, OutputStream outputStream, int saveFormat, String pattern, String replacement) {#replace-java.io.InputStream-java.io.OutputStream-int-java.lang.String-java.lang.String}
```
public static int replace(InputStream inputStream, OutputStream outputStream, int saveFormat, String pattern, String replacement)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| шаблон | java.lang.String |  |
| замена | java.lang.String |  |

**Returns:**
int
### replace(InputStream inputStream, OutputStream outputStream, int saveFormat, String pattern, String replacement, FindReplaceOptions options) {#replace-java.io.InputStream-java.io.OutputStream-int-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions}
```
public static int replace(InputStream inputStream, OutputStream outputStream, int saveFormat, String pattern, String replacement, FindReplaceOptions options)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| шаблон | java.lang.String |  |
| замена | java.lang.String |  |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) |  |

**Returns:**
int
### replace(InputStream inputStream, OutputStream outputStream, int saveFormat, Pattern pattern, String replacement) {#replace-java.io.InputStream-java.io.OutputStream-int-java.util.regex.Pattern-java.lang.String}
```
public static int replace(InputStream inputStream, OutputStream outputStream, int saveFormat, Pattern pattern, String replacement)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| шаблон | java.util.regex.Pattern |  |
| замена | java.lang.String |  |

**Returns:**
int
### replace(InputStream inputStream, OutputStream outputStream, int saveFormat, Pattern pattern, String replacement, FindReplaceOptions options) {#replace-java.io.InputStream-java.io.OutputStream-int-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions}
```
public static int replace(InputStream inputStream, OutputStream outputStream, int saveFormat, Pattern pattern, String replacement, FindReplaceOptions options)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| шаблон | java.util.regex.Pattern |  |
| замена | java.lang.String |  |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) |  |

**Returns:**
int
### replace(String inputFileName, String outputFileName, SaveOptions saveOptions, String pattern, String replacement) {#replace-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String-java.lang.String}
```
public static int replace(String inputFileName, String outputFileName, SaveOptions saveOptions, String pattern, String replacement)
```


Заменяет все вхождения указанного шаблона строкового символа на строку‑замену во входном файле, используя указанный формат сохранения и дополнительные параметры.

 **Remarks:** 

Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница вывода будет сохранена в отдельный файл. Указанное имя выходного файла будет использовано для генерации имён файлов для каждой части по правилу: outputFile\_partIndex.extension.

Если формат вывода — TIFF, вывод будет сохранён в один многостраничный файл TIFF.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | java.lang.String | Имя входного файла. |
| outputFileName | java.lang.String | Имя выходного файла. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Параметры сохранения. |
| шаблон | java.lang.String | Строка, которую нужно заменить. |
| замена | java.lang.String | Строка для замены всех вхождений шаблона. |

**Returns:**
int — количество выполненных замен.
### replace(String inputFileName, String outputFileName, SaveOptions saveOptions, String pattern, String replacement, FindReplaceOptions options) {#replace-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions}
```
public static int replace(String inputFileName, String outputFileName, SaveOptions saveOptions, String pattern, String replacement, FindReplaceOptions options)
```


Заменяет все вхождения указанного шаблона строкового символа на строку‑замену во входном файле, используя указанный формат сохранения и дополнительные параметры.

 **Remarks:** 

Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница вывода будет сохранена в отдельный файл. Указанное имя выходного файла будет использовано для генерации имён файлов для каждой части по правилу: outputFile\_partIndex.extension.

Если формат вывода — TIFF, вывод будет сохранён в один многостраничный файл TIFF.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | java.lang.String | Имя входного файла. |
| outputFileName | java.lang.String | Имя выходного файла. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Параметры сохранения. |
| шаблон | java.lang.String | Строка, которую нужно заменить. |
| замена | java.lang.String | Строка для замены всех вхождений шаблона. |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) объект для указания дополнительных параметров. |

**Returns:**
int — количество выполненных замен.
### replace(String inputFileName, String outputFileName, SaveOptions saveOptions, Pattern pattern, String replacement) {#replace-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.util.regex.Pattern-java.lang.String}
```
public static int replace(String inputFileName, String outputFileName, SaveOptions saveOptions, Pattern pattern, String replacement)
```


Заменяет все вхождения указанного шаблона строкового символа на строку‑замену во входном файле с использованием регулярного выражения, используя указанный формат сохранения и дополнительные параметры.

 **Remarks:** 

Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница вывода будет сохранена в отдельный файл. Указанное имя выходного файла будет использовано для генерации имён файлов для каждой части по правилу: outputFile\_partIndex.extension.

Если формат вывода — TIFF, вывод будет сохранён в один многостраничный файл TIFF.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | java.lang.String | Имя входного файла. |
| outputFileName | java.lang.String | Имя выходного файла. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Параметры сохранения. |
| шаблон | java.util.regex.Pattern | Шаблон регулярного выражения, используемый для поиска совпадений. |
| замена | java.lang.String | Строка для замены всех вхождений шаблона. |

**Returns:**
int — количество выполненных замен.
### replace(String inputFileName, String outputFileName, SaveOptions saveOptions, Pattern pattern, String replacement, FindReplaceOptions options) {#replace-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions}
```
public static int replace(String inputFileName, String outputFileName, SaveOptions saveOptions, Pattern pattern, String replacement, FindReplaceOptions options)
```


Заменяет все вхождения указанного шаблона строкового символа на строку‑замену во входном файле с использованием регулярного выражения, используя указанный формат сохранения и дополнительные параметры.

 **Remarks:** 

Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница вывода будет сохранена в отдельный файл. Указанное имя выходного файла будет использовано для генерации имён файлов для каждой части по правилу: outputFile\_partIndex.extension.

Если формат вывода — TIFF, вывод будет сохранён в один многостраничный файл TIFF.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | java.lang.String | Имя входного файла. |
| outputFileName | java.lang.String | Имя выходного файла. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Параметры сохранения. |
| шаблон | java.util.regex.Pattern | Шаблон регулярного выражения, используемый для поиска совпадений. |
| замена | java.lang.String | Строка для замены всех вхождений шаблона. |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) объект для указания дополнительных параметров. |

**Returns:**
int — количество выполненных замен.
### replace(String inputFileName, String outputFileName, int saveFormat, String pattern, String replacement) {#replace-java.lang.String-java.lang.String-int-java.lang.String-java.lang.String}
```
public static int replace(String inputFileName, String outputFileName, int saveFormat, String pattern, String replacement)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| шаблон | java.lang.String |  |
| замена | java.lang.String |  |

**Returns:**
int
### replace(String inputFileName, String outputFileName, int saveFormat, String pattern, String replacement, FindReplaceOptions options) {#replace-java.lang.String-java.lang.String-int-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions}
```
public static int replace(String inputFileName, String outputFileName, int saveFormat, String pattern, String replacement, FindReplaceOptions options)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| шаблон | java.lang.String |  |
| замена | java.lang.String |  |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) |  |

**Returns:**
int
### replace(String inputFileName, String outputFileName, int saveFormat, Pattern pattern, String replacement) {#replace-java.lang.String-java.lang.String-int-java.util.regex.Pattern-java.lang.String}
```
public static int replace(String inputFileName, String outputFileName, int saveFormat, Pattern pattern, String replacement)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| шаблон | java.util.regex.Pattern |  |
| замена | java.lang.String |  |

**Returns:**
int
### replace(String inputFileName, String outputFileName, int saveFormat, Pattern pattern, String replacement, FindReplaceOptions options) {#replace-java.lang.String-java.lang.String-int-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions}
```
public static int replace(String inputFileName, String outputFileName, int saveFormat, Pattern pattern, String replacement, FindReplaceOptions options)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| шаблон | java.util.regex.Pattern |  |
| замена | java.lang.String |  |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) |  |

**Returns:**
int
### replace(String inputFileName, String outputFileName, String pattern, String replacement) {#replace-java.lang.String-java.lang.String-java.lang.String-java.lang.String}
```
public static int replace(String inputFileName, String outputFileName, String pattern, String replacement)
```


Заменяет все вхождения указанного шаблона строкового символа на строку‑замену во входном файле.

 **Remarks:** 

Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница вывода будет сохранена в отдельный файл. Указанное имя выходного файла будет использовано для генерации имён файлов для каждой части по правилу: outputFile\_partIndex.extension.

Если формат вывода — TIFF, вывод будет сохранён в один многостраничный файл TIFF.

 **Examples:** 

Показывает, как заменить строку в документе.

```

 // There is a several ways to replace string in the document:
 String doc = getMyDir() + "Footer.docx";
 String pattern = "(C)2006 Aspose Pty Ltd.";
 String replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

 FindReplaceOptions options = new FindReplaceOptions();
 options.setFindWholeWordsOnly(false);
 Replacer.replace(doc, getArtifactsDir() + "LowCode.Replace.1.docx", pattern, replacement);
 Replacer.replace(doc, getArtifactsDir() + "LowCode.Replace.2.docx", SaveFormat.DOCX, pattern, replacement);
 Replacer.replace(doc, getArtifactsDir() + "LowCode.Replace.3.docx", SaveFormat.DOCX, pattern, replacement, options);
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | java.lang.String | Имя входного файла. |
| outputFileName | java.lang.String | Имя выходного файла. |
| шаблон | java.lang.String | Строка, которую нужно заменить. |
| замена | java.lang.String | Строка для замены всех вхождений шаблона. |

**Returns:**
int — количество выполненных замен.
### replace(String inputFileName, String outputFileName, Pattern pattern, String replacement) {#replace-java.lang.String-java.lang.String-java.util.regex.Pattern-java.lang.String}
```
public static int replace(String inputFileName, String outputFileName, Pattern pattern, String replacement)
```


Заменяет все вхождения указанного шаблона строкового символа на строку‑замену во входном файле с использованием регулярного выражения.

 **Remarks:** 

Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница вывода будет сохранена в отдельный файл. Указанное имя выходного файла будет использовано для генерации имён файлов для каждой части по правилу: outputFile\_partIndex.extension.

Если формат вывода — TIFF, вывод будет сохранён в один многостраничный файл TIFF.

 **Examples:** 

Показывает, как заменить строку с помощью regex в документе.

```

 // There is a several ways to replace string with regex in the document:
 String doc = getMyDir() + "Footer.docx";
 String pattern = "gr(a|e)y";
 String replacement = "lavender";

 Replacer.replace(doc, getArtifactsDir() + "LowCode.ReplaceRegex.1.docx", pattern, replacement);
 Replacer.replace(doc, getArtifactsDir() + "LowCode.ReplaceRegex.2.docx", SaveFormat.DOCX, pattern, replacement);
 FindReplaceOptions options = new FindReplaceOptions();
 options.setFindWholeWordsOnly(false);
 Replacer.replace(doc, getArtifactsDir() + "LowCode.ReplaceRegex.3.docx", SaveFormat.DOCX, pattern, replacement, options);
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | java.lang.String | Имя входного файла. |
| outputFileName | java.lang.String | Имя выходного файла. |
| шаблон | java.util.regex.Pattern | Шаблон регулярного выражения, используемый для поиска совпадений. |
| замена | java.lang.String | Строка для замены всех вхождений шаблона. |

**Returns:**
int — количество выполненных замен.
### replaceToImages(InputStream inputStream, ImageSaveOptions saveOptions, String pattern, String replacement) {#replaceToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String-java.lang.String}
```
public static OutputStream[] replaceToImages(InputStream inputStream, ImageSaveOptions saveOptions, String pattern, String replacement)
```


Заменяет все вхождения указанного шаблона строкового символа на строку‑замену во входном файле. Выводит результат в виде изображений.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | java.io.InputStream | Входной поток файла. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Параметры сохранения. |
| шаблон | java.lang.String | Строка, которую нужно заменить. |
| замена | java.lang.String | Строка для замены всех вхождений шаблона. |

**Returns:**
java.io.OutputStream[]
### replaceToImages(InputStream inputStream, ImageSaveOptions saveOptions, String pattern, String replacement, FindReplaceOptions options) {#replaceToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions}
```
public static OutputStream[] replaceToImages(InputStream inputStream, ImageSaveOptions saveOptions, String pattern, String replacement, FindReplaceOptions options)
```


Заменяет все вхождения указанного шаблона строкового символа на строку‑замену во входном файле. Выводит результат в виде изображений.

 **Examples:** 

Показывает, как заменить строку в документе, используя документы из потока, и сохранить результат в виде изображений.

```

 // There is a several ways to replace string in the document using documents from the stream:
 String pattern = "(C)2006 Aspose Pty Ltd.";
 String replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Footer.docx")) {
     OutputStream[] images = Replacer.replaceToImages(streamIn, new ImageSaveOptions(SaveFormat.PNG), pattern, replacement);

     FindReplaceOptions options = new FindReplaceOptions();
     options.setFindWholeWordsOnly(false);
     images = Replacer.replaceToImages(streamIn, new ImageSaveOptions(SaveFormat.PNG), pattern, replacement, options);
 }
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | java.io.InputStream | Входной поток файла. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Параметры сохранения. |
| шаблон | java.lang.String | Строка, которую нужно заменить. |
| замена | java.lang.String | Строка для замены всех вхождений шаблона. |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) объект для указания дополнительных параметров. |

**Returns:**
java.io.OutputStream[]
### replaceToImages(InputStream inputStream, ImageSaveOptions saveOptions, Pattern pattern, String replacement) {#replaceToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.util.regex.Pattern-java.lang.String}
```
public static OutputStream[] replaceToImages(InputStream inputStream, ImageSaveOptions saveOptions, Pattern pattern, String replacement)
```


Заменяет все вхождения указанного шаблона регулярного выражения на строку‑замену во входном файле. Выводит результат в виде изображений.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | java.io.InputStream | Входной поток файла. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Параметры сохранения. |
| шаблон | java.util.regex.Pattern | Шаблон регулярного выражения, используемый для поиска совпадений. |
| замена | java.lang.String | Строка для замены всех вхождений шаблона. |

**Returns:**
java.io.OutputStream[]
### replaceToImages(InputStream inputStream, ImageSaveOptions saveOptions, Pattern pattern, String replacement, FindReplaceOptions options) {#replaceToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions}
```
public static OutputStream[] replaceToImages(InputStream inputStream, ImageSaveOptions saveOptions, Pattern pattern, String replacement, FindReplaceOptions options)
```


Заменяет все вхождения указанного шаблона регулярного выражения на строку‑замену во входном файле. Выводит результат в виде изображений.

 **Examples:** 

Показывает, как заменить строку с помощью регулярного выражения в документе, используя документы из потока, и сохранить результат в изображения.

```

 // There is a several ways to replace string with regex in the document using documents from the stream:
 Pattern pattern = Pattern.compile("gr(a|e)y");
 String replacement = "lavender";

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Replace regex.docx")) {
     OutputStream[] images = Replacer.replaceToImages(streamIn, new ImageSaveOptions(SaveFormat.PNG), pattern, replacement);
     FindReplaceOptions options = new FindReplaceOptions();
     options.setFindWholeWordsOnly(false);
     images = Replacer.replaceToImages(streamIn, new ImageSaveOptions(SaveFormat.PNG), pattern, replacement, options);
 }
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | java.io.InputStream | Входной поток файла. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Параметры сохранения. |
| шаблон | java.util.regex.Pattern | Шаблон регулярного выражения, используемый для поиска совпадений. |
| замена | java.lang.String | Строка для замены всех вхождений шаблона. |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) объект для указания дополнительных параметров. |

**Returns:**
java.io.OutputStream[]
### replaceToImages(String inputFileName, ImageSaveOptions saveOptions, String pattern, String replacement) {#replaceToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String-java.lang.String}
```
public static OutputStream[] replaceToImages(String inputFileName, ImageSaveOptions saveOptions, String pattern, String replacement)
```


Заменяет все вхождения указанного шаблона строкового символа на строку‑замену во входном файле. Выводит результат в виде изображений.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | java.lang.String | Имя входного файла. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Параметры сохранения. |
| шаблон | java.lang.String | Строка, которую нужно заменить. |
| замена | java.lang.String | Строка для замены всех вхождений шаблона. |

**Returns:**
java.io.OutputStream[]
### replaceToImages(String inputFileName, ImageSaveOptions saveOptions, String pattern, String replacement, FindReplaceOptions options) {#replaceToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions}
```
public static OutputStream[] replaceToImages(String inputFileName, ImageSaveOptions saveOptions, String pattern, String replacement, FindReplaceOptions options)
```


Заменяет все вхождения указанного шаблона строкового символа на строку‑замену во входном файле. Выводит результат в виде изображений.

 **Examples:** 

Показывает, как заменить строку в документе и сохранить результат в изображения.

```

 // There is a several ways to replace string in the document:
 String doc = getMyDir() + "Footer.docx";
 String pattern = "(C)2006 Aspose Pty Ltd.";
 String replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

 OutputStream[] images = Replacer.replaceToImages(doc, new ImageSaveOptions(SaveFormat.PNG), pattern, replacement);

 FindReplaceOptions options = new FindReplaceOptions();
 options.setFindWholeWordsOnly(false);
 images = Replacer.replaceToImages(doc, new ImageSaveOptions(SaveFormat.PNG), pattern, replacement, options);
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | java.lang.String | Имя входного файла. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Параметры сохранения. |
| шаблон | java.lang.String | Строка, которую нужно заменить. |
| замена | java.lang.String | Строка для замены всех вхождений шаблона. |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) объект для указания дополнительных параметров. |

**Returns:**
java.io.OutputStream[]
### replaceToImages(String inputFileName, ImageSaveOptions saveOptions, Pattern pattern, String replacement) {#replaceToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.util.regex.Pattern-java.lang.String}
```
public static OutputStream[] replaceToImages(String inputFileName, ImageSaveOptions saveOptions, Pattern pattern, String replacement)
```


Заменяет все вхождения указанного шаблона регулярного выражения на строку‑замену во входном файле. Выводит результат в виде изображений.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | java.lang.String | Имя входного файла. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Параметры сохранения. |
| шаблон | java.util.regex.Pattern | Шаблон регулярного выражения, используемый для поиска совпадений. |
| замена | java.lang.String | Строка для замены всех вхождений шаблона. |

**Returns:**
java.io.OutputStream[]
### replaceToImages(String inputFileName, ImageSaveOptions saveOptions, Pattern pattern, String replacement, FindReplaceOptions options) {#replaceToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions}
```
public static OutputStream[] replaceToImages(String inputFileName, ImageSaveOptions saveOptions, Pattern pattern, String replacement, FindReplaceOptions options)
```


Заменяет все вхождения указанного шаблона регулярного выражения на строку‑замену во входном файле. Выводит результат в виде изображений.

 **Examples:** 

Показывает, как заменить строку с помощью регулярного выражения в документе и сохранить результат в изображения.

```

 // There is a several ways to replace string with regex in the document:
 String doc = getMyDir() + "Footer.docx";
 Pattern pattern = Pattern.compile("gr(a|e)y");
 String replacement = "lavender";

 OutputStream[] images = Replacer.replaceToImages(doc, new ImageSaveOptions(SaveFormat.PNG), pattern, replacement);
 FindReplaceOptions options = new FindReplaceOptions();
 options.setFindWholeWordsOnly(false);
 images = Replacer.replaceToImages(doc, new ImageSaveOptions(SaveFormat.PNG), pattern, replacement, options);
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | java.lang.String | Имя входного файла. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Параметры сохранения. |
| шаблон | java.util.regex.Pattern | Шаблон регулярного выражения, используемый для поиска совпадений. |
| замена | java.lang.String | Строка для замены всех вхождений шаблона. |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) объект для указания дополнительных параметров. |

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
