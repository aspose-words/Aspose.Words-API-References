---
title: "Replacer"
linktitle: "Replacer"
second_title: "Aspose.Words for Java"
description: "提供用于在 Java 中查找和替换文档中文本的方法。"
type: docs
weight: 567
url: /zh/java/com.aspose.words/replacer/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Processor](../../com.aspose.words/processor/)
```
public class Replacer extends Processor
```

提供用于在文档中查找和替换文本的方法。
## 方法

| 方法 | 描述 |
| --- | --- |
| [create(ReplacerContext context)](#create-com.aspose.words.ReplacerContext) | 创建 replacer 处理器的新实例。 |
| [execute()](#execute) | 执行处理器操作。 |
| [from(InputStream input)](#from-java.io.InputStream) | 指定用于处理的输入文档。 |
| [from(InputStream input, LoadOptions loadOptions)](#from-java.io.InputStream-com.aspose.words.LoadOptions) | 指定用于处理的输入文档。 |
| [from(String input)](#from-java.lang.String) | 指定用于处理的输入文档。 |
| [from(String input, LoadOptions loadOptions)](#from-java.lang.String-com.aspose.words.LoadOptions) | 指定用于处理的输入文档。 |
| [replace(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, String pattern, String replacement)](#replace-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.String-java.lang.String) |  |
| [replace(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, String pattern, String replacement, FindReplaceOptions options)](#replace-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions) |  |
| [replace(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Pattern pattern, String replacement)](#replace-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.util.regex.Pattern-java.lang.String) |  |
| [replace(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Pattern pattern, String replacement, FindReplaceOptions options)](#replace-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions) |  |
| [replace(InputStream inputStream, OutputStream outputStream, int saveFormat, String pattern, String replacement)](#replace-java.io.InputStream-java.io.OutputStream-int-java.lang.String-java.lang.String) |  |
| [replace(InputStream inputStream, OutputStream outputStream, int saveFormat, String pattern, String replacement, FindReplaceOptions options)](#replace-java.io.InputStream-java.io.OutputStream-int-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions) |  |
| [replace(InputStream inputStream, OutputStream outputStream, int saveFormat, Pattern pattern, String replacement)](#replace-java.io.InputStream-java.io.OutputStream-int-java.util.regex.Pattern-java.lang.String) |  |
| [replace(InputStream inputStream, OutputStream outputStream, int saveFormat, Pattern pattern, String replacement, FindReplaceOptions options)](#replace-java.io.InputStream-java.io.OutputStream-int-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions) |  |
| [replace(String inputFileName, String outputFileName, SaveOptions saveOptions, String pattern, String replacement)](#replace-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String-java.lang.String) | 在输入文件中，将指定字符字符串模式的所有出现替换为替换字符串，使用指定的保存格式和其他选项。 |
| [replace(String inputFileName, String outputFileName, SaveOptions saveOptions, String pattern, String replacement, FindReplaceOptions options)](#replace-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions) | 在输入文件中，将指定字符字符串模式的所有出现替换为替换字符串，使用指定的保存格式和其他选项。 |
| [replace(String inputFileName, String outputFileName, SaveOptions saveOptions, Pattern pattern, String replacement)](#replace-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.util.regex.Pattern-java.lang.String) | 在输入文件中，使用正则表达式将指定字符字符串模式的所有出现替换为替换字符串，使用指定的保存格式和其他选项。 |
| [replace(String inputFileName, String outputFileName, SaveOptions saveOptions, Pattern pattern, String replacement, FindReplaceOptions options)](#replace-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions) | 在输入文件中，使用正则表达式将指定字符字符串模式的所有出现替换为替换字符串，使用指定的保存格式和其他选项。 |
| [replace(String inputFileName, String outputFileName, int saveFormat, String pattern, String replacement)](#replace-java.lang.String-java.lang.String-int-java.lang.String-java.lang.String) |  |
| [replace(String inputFileName, String outputFileName, int saveFormat, String pattern, String replacement, FindReplaceOptions options)](#replace-java.lang.String-java.lang.String-int-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions) |  |
| [replace(String inputFileName, String outputFileName, int saveFormat, Pattern pattern, String replacement)](#replace-java.lang.String-java.lang.String-int-java.util.regex.Pattern-java.lang.String) |  |
| [replace(String inputFileName, String outputFileName, int saveFormat, Pattern pattern, String replacement, FindReplaceOptions options)](#replace-java.lang.String-java.lang.String-int-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions) |  |
| [replace(String inputFileName, String outputFileName, String pattern, String replacement)](#replace-java.lang.String-java.lang.String-java.lang.String-java.lang.String) | 在输入文件中，将指定字符字符串模式的所有出现替换为替换字符串。 |
| [replace(String inputFileName, String outputFileName, Pattern pattern, String replacement)](#replace-java.lang.String-java.lang.String-java.util.regex.Pattern-java.lang.String) | 在输入文件中，使用正则表达式将指定字符字符串模式的所有出现替换为替换字符串。 |
| [replaceToImages(InputStream inputStream, ImageSaveOptions saveOptions, String pattern, String replacement)](#replaceToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String-java.lang.String) | 在输入文件中，将指定字符字符串模式的所有出现替换为替换字符串。 |
| [replaceToImages(InputStream inputStream, ImageSaveOptions saveOptions, String pattern, String replacement, FindReplaceOptions options)](#replaceToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions) | 在输入文件中，将指定字符字符串模式的所有出现替换为替换字符串。 |
| [replaceToImages(InputStream inputStream, ImageSaveOptions saveOptions, Pattern pattern, String replacement)](#replaceToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.util.regex.Pattern-java.lang.String) | 在输入文件中，将指定正则表达式模式的所有出现替换为替换字符串。 |
| [replaceToImages(InputStream inputStream, ImageSaveOptions saveOptions, Pattern pattern, String replacement, FindReplaceOptions options)](#replaceToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions) | 在输入文件中，将指定正则表达式模式的所有出现替换为替换字符串。 |
| [replaceToImages(String inputFileName, ImageSaveOptions saveOptions, String pattern, String replacement)](#replaceToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String-java.lang.String) | 在输入文件中，将指定字符字符串模式的所有出现替换为替换字符串。 |
| [replaceToImages(String inputFileName, ImageSaveOptions saveOptions, String pattern, String replacement, FindReplaceOptions options)](#replaceToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions) | 在输入文件中，将指定字符字符串模式的所有出现替换为替换字符串。 |
| [replaceToImages(String inputFileName, ImageSaveOptions saveOptions, Pattern pattern, String replacement)](#replaceToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.util.regex.Pattern-java.lang.String) | 在输入文件中，将指定正则表达式模式的所有出现替换为替换字符串。 |
| [replaceToImages(String inputFileName, ImageSaveOptions saveOptions, Pattern pattern, String replacement, FindReplaceOptions options)](#replaceToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions) | 在输入文件中，将指定正则表达式模式的所有出现替换为替换字符串。 |
| [to(OutputStream output, SaveOptions saveOptions)](#to-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [to(OutputStream output, int saveFormat)](#to-java.io.OutputStream-int) |  |
| [to(String output)](#to-java.lang.String) | 指定处理器的输出文件。 |
| [to(String output, SaveOptions saveOptions)](#to-java.lang.String-com.aspose.words.SaveOptions) | 指定处理器的输出文件。 |
| [to(String output, int saveFormat)](#to-java.lang.String-int) |  |
| [to(ArrayList output, SaveOptions saveOptions)](#to-java.util.ArrayList-com.aspose.words.SaveOptions) |  |
| [to(ArrayList output, int saveFormat)](#to-java.util.ArrayList-int) |  |
| [toOutput(ArrayList output, SaveOptions saveOptions)](#toOutput-java.util.ArrayList-com.aspose.words.SaveOptions) |  |
| [toOutput(ArrayList output, int saveFormat)](#toOutput-java.util.ArrayList-int) |  |
### create(ReplacerContext context) {#create-com.aspose.words.ReplacerContext}
```
public static Replacer create(ReplacerContext context)
```


创建 replacer 处理器的新实例。

 **Examples:** 

展示如何使用上下文在文档中替换字符串。

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

展示如何使用来自流的文档并使用上下文在文档中替换字符串。

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

展示如何使用上下文在文档中使用正则表达式替换字符串。

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

展示如何使用来自流的文档并使用上下文在文档中使用正则表达式替换字符串。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| context | [ReplacerContext](../../com.aspose.words/replacercontext/) |  |

**Returns:**
[Replacer](../../com.aspose.words/replacer/)
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
### replace(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, String pattern, String replacement) {#replace-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.String-java.lang.String}
```
public static int replace(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, String pattern, String replacement)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| 模式 | java.lang.String |  |
| 替换 | java.lang.String |  |

**Returns:**
int
### replace(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, String pattern, String replacement, FindReplaceOptions options) {#replace-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions}
```
public static int replace(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, String pattern, String replacement, FindReplaceOptions options)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| 模式 | java.lang.String |  |
| 替换 | java.lang.String |  |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) |  |

**Returns:**
int
### replace(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Pattern pattern, String replacement) {#replace-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.util.regex.Pattern-java.lang.String}
```
public static int replace(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Pattern pattern, String replacement)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| 模式 | java.util.regex.Pattern |  |
| 替换 | java.lang.String |  |

**Returns:**
int
### replace(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Pattern pattern, String replacement, FindReplaceOptions options) {#replace-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions}
```
public static int replace(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Pattern pattern, String replacement, FindReplaceOptions options)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| 模式 | java.util.regex.Pattern |  |
| 替换 | java.lang.String |  |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) |  |

**Returns:**
int
### replace(InputStream inputStream, OutputStream outputStream, int saveFormat, String pattern, String replacement) {#replace-java.io.InputStream-java.io.OutputStream-int-java.lang.String-java.lang.String}
```
public static int replace(InputStream inputStream, OutputStream outputStream, int saveFormat, String pattern, String replacement)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| 模式 | java.lang.String |  |
| 替换 | java.lang.String |  |

**Returns:**
int
### replace(InputStream inputStream, OutputStream outputStream, int saveFormat, String pattern, String replacement, FindReplaceOptions options) {#replace-java.io.InputStream-java.io.OutputStream-int-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions}
```
public static int replace(InputStream inputStream, OutputStream outputStream, int saveFormat, String pattern, String replacement, FindReplaceOptions options)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| 模式 | java.lang.String |  |
| 替换 | java.lang.String |  |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) |  |

**Returns:**
int
### replace(InputStream inputStream, OutputStream outputStream, int saveFormat, Pattern pattern, String replacement) {#replace-java.io.InputStream-java.io.OutputStream-int-java.util.regex.Pattern-java.lang.String}
```
public static int replace(InputStream inputStream, OutputStream outputStream, int saveFormat, Pattern pattern, String replacement)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| 模式 | java.util.regex.Pattern |  |
| 替换 | java.lang.String |  |

**Returns:**
int
### replace(InputStream inputStream, OutputStream outputStream, int saveFormat, Pattern pattern, String replacement, FindReplaceOptions options) {#replace-java.io.InputStream-java.io.OutputStream-int-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions}
```
public static int replace(InputStream inputStream, OutputStream outputStream, int saveFormat, Pattern pattern, String replacement, FindReplaceOptions options)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| 模式 | java.util.regex.Pattern |  |
| 替换 | java.lang.String |  |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) |  |

**Returns:**
int
### replace(String inputFileName, String outputFileName, SaveOptions saveOptions, String pattern, String replacement) {#replace-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String-java.lang.String}
```
public static int replace(String inputFileName, String outputFileName, SaveOptions saveOptions, String pattern, String replacement)
```


在输入文件中，将指定字符字符串模式的所有出现替换为替换字符串，使用指定的保存格式和其他选项。

 **Remarks:** 

如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则 outputFile\_partIndex.extension 为每个部分生成文件名。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String | 输入文件名。 |
| outputFileName | java.lang.String | 输出文件名。 |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | 保存选项。 |
| 模式 | java.lang.String | 要被替换的字符串。 |
| 替换 | java.lang.String | 用于替换模式所有出现的字符串。 |

**Returns:**
int - 已进行的替换次数。
### replace(String inputFileName, String outputFileName, SaveOptions saveOptions, String pattern, String replacement, FindReplaceOptions options) {#replace-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions}
```
public static int replace(String inputFileName, String outputFileName, SaveOptions saveOptions, String pattern, String replacement, FindReplaceOptions options)
```


在输入文件中，将指定字符字符串模式的所有出现替换为替换字符串，使用指定的保存格式和其他选项。

 **Remarks:** 

如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则 outputFile\_partIndex.extension 为每个部分生成文件名。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String | 输入文件名。 |
| outputFileName | java.lang.String | 输出文件名。 |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | 保存选项。 |
| 模式 | java.lang.String | 要被替换的字符串。 |
| 替换 | java.lang.String | 用于替换模式所有出现的字符串。 |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) | 用于指定其他选项的 [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) 对象。 |

**Returns:**
int - 已进行的替换次数。
### replace(String inputFileName, String outputFileName, SaveOptions saveOptions, Pattern pattern, String replacement) {#replace-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.util.regex.Pattern-java.lang.String}
```
public static int replace(String inputFileName, String outputFileName, SaveOptions saveOptions, Pattern pattern, String replacement)
```


在输入文件中，使用正则表达式将指定字符字符串模式的所有出现替换为替换字符串，使用指定的保存格式和其他选项。

 **Remarks:** 

如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则 outputFile\_partIndex.extension 为每个部分生成文件名。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String | 输入文件名。 |
| outputFileName | java.lang.String | 输出文件名。 |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | 保存选项。 |
| 模式 | java.util.regex.Pattern | 用于查找匹配项的正则表达式模式。 |
| 替换 | java.lang.String | 用于替换模式所有出现的字符串。 |

**Returns:**
int - 已进行的替换次数。
### replace(String inputFileName, String outputFileName, SaveOptions saveOptions, Pattern pattern, String replacement, FindReplaceOptions options) {#replace-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions}
```
public static int replace(String inputFileName, String outputFileName, SaveOptions saveOptions, Pattern pattern, String replacement, FindReplaceOptions options)
```


在输入文件中，使用正则表达式将指定字符字符串模式的所有出现替换为替换字符串，使用指定的保存格式和其他选项。

 **Remarks:** 

如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则 outputFile\_partIndex.extension 为每个部分生成文件名。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String | 输入文件名。 |
| outputFileName | java.lang.String | 输出文件名。 |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | 保存选项。 |
| 模式 | java.util.regex.Pattern | 用于查找匹配项的正则表达式模式。 |
| 替换 | java.lang.String | 用于替换模式所有出现的字符串。 |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) | 用于指定其他选项的 [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) 对象。 |

**Returns:**
int - 已进行的替换次数。
### replace(String inputFileName, String outputFileName, int saveFormat, String pattern, String replacement) {#replace-java.lang.String-java.lang.String-int-java.lang.String-java.lang.String}
```
public static int replace(String inputFileName, String outputFileName, int saveFormat, String pattern, String replacement)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| 模式 | java.lang.String |  |
| 替换 | java.lang.String |  |

**Returns:**
int
### replace(String inputFileName, String outputFileName, int saveFormat, String pattern, String replacement, FindReplaceOptions options) {#replace-java.lang.String-java.lang.String-int-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions}
```
public static int replace(String inputFileName, String outputFileName, int saveFormat, String pattern, String replacement, FindReplaceOptions options)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| 模式 | java.lang.String |  |
| 替换 | java.lang.String |  |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) |  |

**Returns:**
int
### replace(String inputFileName, String outputFileName, int saveFormat, Pattern pattern, String replacement) {#replace-java.lang.String-java.lang.String-int-java.util.regex.Pattern-java.lang.String}
```
public static int replace(String inputFileName, String outputFileName, int saveFormat, Pattern pattern, String replacement)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| 模式 | java.util.regex.Pattern |  |
| 替换 | java.lang.String |  |

**Returns:**
int
### replace(String inputFileName, String outputFileName, int saveFormat, Pattern pattern, String replacement, FindReplaceOptions options) {#replace-java.lang.String-java.lang.String-int-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions}
```
public static int replace(String inputFileName, String outputFileName, int saveFormat, Pattern pattern, String replacement, FindReplaceOptions options)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| 模式 | java.util.regex.Pattern |  |
| 替换 | java.lang.String |  |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) |  |

**Returns:**
int
### replace(String inputFileName, String outputFileName, String pattern, String replacement) {#replace-java.lang.String-java.lang.String-java.lang.String-java.lang.String}
```
public static int replace(String inputFileName, String outputFileName, String pattern, String replacement)
```


在输入文件中，将指定字符字符串模式的所有出现替换为替换字符串。

 **Remarks:** 

如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则 outputFile\_partIndex.extension 为每个部分生成文件名。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

 **Examples:** 

展示如何在文档中替换字符串。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String | 输入文件名。 |
| outputFileName | java.lang.String | 输出文件名。 |
| 模式 | java.lang.String | 要被替换的字符串。 |
| 替换 | java.lang.String | 用于替换模式所有出现的字符串。 |

**Returns:**
int - 已进行的替换次数。
### replace(String inputFileName, String outputFileName, Pattern pattern, String replacement) {#replace-java.lang.String-java.lang.String-java.util.regex.Pattern-java.lang.String}
```
public static int replace(String inputFileName, String outputFileName, Pattern pattern, String replacement)
```


在输入文件中，使用正则表达式将指定字符字符串模式的所有出现替换为替换字符串。

 **Remarks:** 

如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则 outputFile\_partIndex.extension 为每个部分生成文件名。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

 **Examples:** 

展示如何在文档中使用正则表达式替换字符串。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String | 输入文件名。 |
| outputFileName | java.lang.String | 输出文件名。 |
| 模式 | java.util.regex.Pattern | 用于查找匹配项的正则表达式模式。 |
| 替换 | java.lang.String | 用于替换模式所有出现的字符串。 |

**Returns:**
int - 已进行的替换次数。
### replaceToImages(InputStream inputStream, ImageSaveOptions saveOptions, String pattern, String replacement) {#replaceToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String-java.lang.String}
```
public static OutputStream[] replaceToImages(InputStream inputStream, ImageSaveOptions saveOptions, String pattern, String replacement)
```


在输入文件中，将指定字符字符串模式的所有出现替换为替换字符串。将输出渲染为图像。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream | 输入文件流。 |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | 保存选项。 |
| 模式 | java.lang.String | 要被替换的字符串。 |
| 替换 | java.lang.String | 用于替换模式所有出现的字符串。 |

**Returns:**
java.io.OutputStream[]
### replaceToImages(InputStream inputStream, ImageSaveOptions saveOptions, String pattern, String replacement, FindReplaceOptions options) {#replaceToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions}
```
public static OutputStream[] replaceToImages(InputStream inputStream, ImageSaveOptions saveOptions, String pattern, String replacement, FindReplaceOptions options)
```


在输入文件中，将指定字符字符串模式的所有出现替换为替换字符串。将输出渲染为图像。

 **Examples:** 

展示如何使用来自流的文档在文档中替换字符串并将结果保存为图像。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream | 输入文件流。 |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | 保存选项。 |
| 模式 | java.lang.String | 要被替换的字符串。 |
| 替换 | java.lang.String | 用于替换模式所有出现的字符串。 |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) | 用于指定其他选项的 [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) 对象。 |

**Returns:**
java.io.OutputStream[]
### replaceToImages(InputStream inputStream, ImageSaveOptions saveOptions, Pattern pattern, String replacement) {#replaceToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.util.regex.Pattern-java.lang.String}
```
public static OutputStream[] replaceToImages(InputStream inputStream, ImageSaveOptions saveOptions, Pattern pattern, String replacement)
```


在输入文件中，将指定正则表达式模式的所有出现替换为替换字符串。将输出渲染为图像。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream | 输入文件流。 |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | 保存选项。 |
| 模式 | java.util.regex.Pattern | 用于查找匹配项的正则表达式模式。 |
| 替换 | java.lang.String | 用于替换模式所有出现的字符串。 |

**Returns:**
java.io.OutputStream[]
### replaceToImages(InputStream inputStream, ImageSaveOptions saveOptions, Pattern pattern, String replacement, FindReplaceOptions options) {#replaceToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions}
```
public static OutputStream[] replaceToImages(InputStream inputStream, ImageSaveOptions saveOptions, Pattern pattern, String replacement, FindReplaceOptions options)
```


在输入文件中，将指定正则表达式模式的所有出现替换为替换字符串。将输出渲染为图像。

 **Examples:** 

展示如何在文档中使用来自流的文档通过正则表达式替换字符串并将结果保存为图像。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream | 输入文件流。 |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | 保存选项。 |
| 模式 | java.util.regex.Pattern | 用于查找匹配项的正则表达式模式。 |
| 替换 | java.lang.String | 用于替换模式所有出现的字符串。 |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) | 用于指定其他选项的 [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) 对象。 |

**Returns:**
java.io.OutputStream[]
### replaceToImages(String inputFileName, ImageSaveOptions saveOptions, String pattern, String replacement) {#replaceToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String-java.lang.String}
```
public static OutputStream[] replaceToImages(String inputFileName, ImageSaveOptions saveOptions, String pattern, String replacement)
```


在输入文件中，将指定字符字符串模式的所有出现替换为替换字符串。将输出渲染为图像。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String | 输入文件名。 |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | 保存选项。 |
| 模式 | java.lang.String | 要被替换的字符串。 |
| 替换 | java.lang.String | 用于替换模式所有出现的字符串。 |

**Returns:**
java.io.OutputStream[]
### replaceToImages(String inputFileName, ImageSaveOptions saveOptions, String pattern, String replacement, FindReplaceOptions options) {#replaceToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions}
```
public static OutputStream[] replaceToImages(String inputFileName, ImageSaveOptions saveOptions, String pattern, String replacement, FindReplaceOptions options)
```


在输入文件中，将指定字符字符串模式的所有出现替换为替换字符串。将输出渲染为图像。

 **Examples:** 

展示如何在文档中替换字符串并将结果保存为图像。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String | 输入文件名。 |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | 保存选项。 |
| 模式 | java.lang.String | 要被替换的字符串。 |
| 替换 | java.lang.String | 用于替换模式所有出现的字符串。 |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) | 用于指定其他选项的 [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) 对象。 |

**Returns:**
java.io.OutputStream[]
### replaceToImages(String inputFileName, ImageSaveOptions saveOptions, Pattern pattern, String replacement) {#replaceToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.util.regex.Pattern-java.lang.String}
```
public static OutputStream[] replaceToImages(String inputFileName, ImageSaveOptions saveOptions, Pattern pattern, String replacement)
```


在输入文件中，将指定正则表达式模式的所有出现替换为替换字符串。将输出渲染为图像。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String | 输入文件名。 |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | 保存选项。 |
| 模式 | java.util.regex.Pattern | 用于查找匹配项的正则表达式模式。 |
| 替换 | java.lang.String | 用于替换模式所有出现的字符串。 |

**Returns:**
java.io.OutputStream[]
### replaceToImages(String inputFileName, ImageSaveOptions saveOptions, Pattern pattern, String replacement, FindReplaceOptions options) {#replaceToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions}
```
public static OutputStream[] replaceToImages(String inputFileName, ImageSaveOptions saveOptions, Pattern pattern, String replacement, FindReplaceOptions options)
```


在输入文件中，将指定正则表达式模式的所有出现替换为替换字符串。将输出渲染为图像。

 **Examples:** 

展示如何在文档中使用正则表达式替换字符串并将结果保存为图像。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String | 输入文件名。 |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | 保存选项。 |
| 模式 | java.util.regex.Pattern | 用于查找匹配项的正则表达式模式。 |
| 替换 | java.lang.String | 用于替换模式所有出现的字符串。 |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) | 用于指定其他选项的 [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) 对象。 |

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
