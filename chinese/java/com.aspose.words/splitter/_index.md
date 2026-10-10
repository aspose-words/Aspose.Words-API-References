---
title: "拆分器"
linktitle: "拆分器"
second_title: "Aspose.Words for Java"
description: "提供用于使用不同标准在 Java 中将文档拆分为多个部分的方法。"
type: docs
weight: 631
url: /zh/java/com.aspose.words/splitter/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Processor](../../com.aspose.words/processor/)
```
public class Splitter extends Processor
```

提供用于使用不同标准将文档拆分为多个部分的方法。
## 方法

| 方法 | 描述 |
| --- | --- |
| [create(SplitterContext context)](#create-com.aspose.words.SplitterContext) | 创建拆分处理器的新实例。 |
| [execute()](#execute) | 执行处理器操作。 |
| [extractPages(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, int startPageIndex, int pageCount)](#extractPages-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-int-int) |  |
| [extractPages(InputStream inputStream, OutputStream outputStream, int saveFormat, int startPageIndex, int pageCount)](#extractPages-java.io.InputStream-java.io.OutputStream-int-int-int) |  |
| [extractPages(String inputFileName, String outputFileName, SaveOptions saveOptions, int startPageIndex, int pageCount)](#extractPages-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-int-int) | 从文档文件中提取指定范围的页面，并使用指定的保存格式将提取的页面保存到新文件。 |
| [extractPages(String inputFileName, String outputFileName, int startPageIndex, int pageCount)](#extractPages-java.lang.String-java.lang.String-int-int) | 从文档文件中提取指定范围的页面，并将提取的页面保存到新文件。 |
| [extractPages(String inputFileName, String outputFileName, int saveFormat, int startPageIndex, int pageCount)](#extractPages-java.lang.String-java.lang.String-int-int-int) |  |
| [from(InputStream input)](#from-java.io.InputStream) | 指定用于处理的输入文档。 |
| [from(InputStream input, LoadOptions loadOptions)](#from-java.io.InputStream-com.aspose.words.LoadOptions) | 指定用于处理的输入文档。 |
| [from(String input)](#from-java.lang.String) | 指定用于处理的输入文档。 |
| [from(String input, LoadOptions loadOptions)](#from-java.lang.String-com.aspose.words.LoadOptions) | 指定用于处理的输入文档。 |
| [removeBlankPages(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions)](#removeBlankPages-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [removeBlankPages(InputStream inputStream, OutputStream outputStream, int saveFormat)](#removeBlankPages-java.io.InputStream-java.io.OutputStream-int) |  |
| [removeBlankPages(String inputFileName, String outputFileName)](#removeBlankPages-java.lang.String-java.lang.String) | 删除文档中的空白页并保存输出。 |
| [removeBlankPages(String inputFileName, String outputFileName, SaveOptions saveOptions)](#removeBlankPages-java.lang.String-java.lang.String-com.aspose.words.SaveOptions) | 删除文档中的空白页并以指定格式保存输出。 |
| [removeBlankPages(String inputFileName, String outputFileName, int saveFormat)](#removeBlankPages-java.lang.String-java.lang.String-int) |  |
| [split(InputStream inputStream, SaveOptions saveOptions, SplitOptions options)](#split-java.io.InputStream-com.aspose.words.SaveOptions-com.aspose.words.SplitOptions) | 根据指定的拆分选项，将来自输入流的文档拆分为多个部分，并以指定的保存格式返回包含这些部分的流数组。 |
| [split(InputStream inputStream, int saveFormat, SplitOptions options)](#split-java.io.InputStream-int-com.aspose.words.SplitOptions) |  |
| [split(String inputFileName, String outputFileName, SaveOptions saveOptions, SplitOptions options)](#split-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.SplitOptions) | 根据指定的拆分选项，将文档拆分为多个部分，并以指定的保存格式将生成的部分保存为文件。 |
| [split(String inputFileName, String outputFileName, SplitOptions options)](#split-java.lang.String-java.lang.String-com.aspose.words.SplitOptions) | 根据指定的拆分选项，将文档拆分为多个部分，并将生成的部分保存为文件。 |
| [split(String inputFileName, String outputFileName, int saveFormat, SplitOptions options)](#split-java.lang.String-java.lang.String-int-com.aspose.words.SplitOptions) |  |
| [to(OutputStream output, SaveOptions saveOptions)](#to-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [to(OutputStream output, int saveFormat)](#to-java.io.OutputStream-int) |  |
| [to(String output)](#to-java.lang.String) | 指定处理器的输出文件。 |
| [to(String output, SaveOptions saveOptions)](#to-java.lang.String-com.aspose.words.SaveOptions) | 指定处理器的输出文件。 |
| [to(String output, int saveFormat)](#to-java.lang.String-int) |  |
| [to(ArrayList output, SaveOptions saveOptions)](#to-java.util.ArrayList-com.aspose.words.SaveOptions) |  |
| [to(ArrayList output, int saveFormat)](#to-java.util.ArrayList-int) |  |
| [toOutput(ArrayList output, SaveOptions saveOptions)](#toOutput-java.util.ArrayList-com.aspose.words.SaveOptions) |  |
| [toOutput(ArrayList output, int saveFormat)](#toOutput-java.util.ArrayList-int) |  |
### create(SplitterContext context) {#create-com.aspose.words.SplitterContext}
```
public static Splitter create(SplitterContext context)
```


创建拆分处理器的新实例。

 **Examples:** 

展示如何使用上下文按页拆分文档。

```

 String doc = getMyDir() + "Big document.docx";

 SplitterContext splitterContext = new SplitterContext();
 splitterContext.getSplitOptions().setSplitCriteria(SplitCriteria.PAGE);

 Splitter.create(splitterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.SplitContextDocument.docx")
         .execute();
 
```

展示如何使用上下文从流中按页拆分文档。

```

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Big document.docx")) {
     SplitterContext splitterContext = new SplitterContext();
     splitterContext.getSplitOptions().setSplitCriteria(SplitCriteria.PAGE);

     ArrayList pages = new ArrayList<>();
     Splitter.create(splitterContext)
             .from(streamIn)
             .toOutput(pages, SaveFormat.DOCX)
             .execute();
 }
 
```

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| context | [SplitterContext](../../com.aspose.words/splittercontext/) |  |

**Returns:**
[Splitter](../../com.aspose.words/splitter/)
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

### extractPages(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, int startPageIndex, int pageCount) {#extractPages-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-int-int}
```
public static void extractPages(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, int startPageIndex, int pageCount)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| startPageIndex | int |  |
| pageCount | int |  |

### extractPages(InputStream inputStream, OutputStream outputStream, int saveFormat, int startPageIndex, int pageCount) {#extractPages-java.io.InputStream-java.io.OutputStream-int-int-int}
```
public static void extractPages(InputStream inputStream, OutputStream outputStream, int saveFormat, int startPageIndex, int pageCount)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| startPageIndex | int |  |
| pageCount | int |  |

### extractPages(String inputFileName, String outputFileName, SaveOptions saveOptions, int startPageIndex, int pageCount) {#extractPages-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-int-int}
```
public static void extractPages(String inputFileName, String outputFileName, SaveOptions saveOptions, int startPageIndex, int pageCount)
```


从文档文件中提取指定范围的页面，并使用指定的保存格式将提取的页面保存到新文件。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String | 输入文件名。 |
| outputFileName | java.lang.String | 输出文件名。 |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | 保存选项。 |
| startPageIndex | int | 要提取的第一页的零基索引。 |
| pageCount | int | 要提取的页面数量。 |

### extractPages(String inputFileName, String outputFileName, int startPageIndex, int pageCount) {#extractPages-java.lang.String-java.lang.String-int-int}
```
public static void extractPages(String inputFileName, String outputFileName, int startPageIndex, int pageCount)
```


从文档文件中提取指定范围的页面，并将提取的页面保存到新文件。输出文件格式由输出文件名的扩展名决定。

 **Examples:** 

展示如何从文档中提取页面。

```

 // There is a several ways to extract pages from the document:
 String doc = getMyDir() + "Big document.docx";

 Splitter.extractPages(doc, getArtifactsDir() + "LowCode.ExtractPages.1.docx", 0, 2);
 Splitter.extractPages(doc, getArtifactsDir() + "LowCode.ExtractPages.2.docx", SaveFormat.DOCX, 0, 2);
 
```

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String | 输入文件名。 |
| outputFileName | java.lang.String | 输出文件名。 |
| startPageIndex | int | 要提取的第一页的零基索引。 |
| pageCount | int | 要提取的页面数量。 |

### extractPages(String inputFileName, String outputFileName, int saveFormat, int startPageIndex, int pageCount) {#extractPages-java.lang.String-java.lang.String-int-int-int}
```
public static void extractPages(String inputFileName, String outputFileName, int saveFormat, int startPageIndex, int pageCount)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| startPageIndex | int |  |
| pageCount | int |  |

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
### removeBlankPages(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions) {#removeBlankPages-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions}
```
public static ArrayList removeBlankPages(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
java.util.ArrayList
### removeBlankPages(InputStream inputStream, OutputStream outputStream, int saveFormat) {#removeBlankPages-java.io.InputStream-java.io.OutputStream-int}
```
public static ArrayList removeBlankPages(InputStream inputStream, OutputStream outputStream, int saveFormat)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |

**Returns:**
java.util.ArrayList
### removeBlankPages(String inputFileName, String outputFileName) {#removeBlankPages-java.lang.String-java.lang.String}
```
public static ArrayList removeBlankPages(String inputFileName, String outputFileName)
```


删除文档中的空白页并保存输出。返回被删除的页面编号列表。

 **Examples:** 

展示如何删除文档中的空白页。

```

 // There is a several ways to remove empty pages from the document:
 String doc = getMyDir() + "Blank pages.docx";

 Splitter.removeBlankPages(doc, getArtifactsDir() + "LowCode.RemoveBlankPages.1.docx");
 Splitter.removeBlankPages(doc, getArtifactsDir() + "LowCode.RemoveBlankPages.2.docx", SaveFormat.DOCX);
 
```

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String | 输入文件名。 |
| outputFileName | java.lang.String | 输出文件名。 |

**Returns:**
java.util.ArrayList - 已将页面编号列表视为空白并删除。
### removeBlankPages(String inputFileName, String outputFileName, SaveOptions saveOptions) {#removeBlankPages-java.lang.String-java.lang.String-com.aspose.words.SaveOptions}
```
public static ArrayList removeBlankPages(String inputFileName, String outputFileName, SaveOptions saveOptions)
```


删除文档中的空白页并以指定格式保存输出。返回被删除的页面编号列表。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String | 输入文件名。 |
| outputFileName | java.lang.String | 输出文件名。 |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | 保存选项。 |

**Returns:**
java.util.ArrayList - 已将页面编号列表视为空白并删除。
### removeBlankPages(String inputFileName, String outputFileName, int saveFormat) {#removeBlankPages-java.lang.String-java.lang.String-int}
```
public static ArrayList removeBlankPages(String inputFileName, String outputFileName, int saveFormat)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |

**Returns:**
java.util.ArrayList
### split(InputStream inputStream, SaveOptions saveOptions, SplitOptions options) {#split-java.io.InputStream-com.aspose.words.SaveOptions-com.aspose.words.SplitOptions}
```
public static OutputStream[] split(InputStream inputStream, SaveOptions saveOptions, SplitOptions options)
```


根据指定的拆分选项，将来自输入流的文档拆分为多个部分，并以指定的保存格式返回包含这些部分的流数组。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream | 输入流。 |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | 保存选项。 |
| options | [SplitOptions](../../com.aspose.words/splitoptions/) | 文档拆分选项。 |

**Returns:**
java.io.OutputStream[]
### split(InputStream inputStream, int saveFormat, SplitOptions options) {#split-java.io.InputStream-int-com.aspose.words.SplitOptions}
```
public static OutputStream[] split(InputStream inputStream, int saveFormat, SplitOptions options)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| saveFormat | int |  |
| options | [SplitOptions](../../com.aspose.words/splitoptions/) |  |

**Returns:**
java.io.OutputStream[]
### split(String inputFileName, String outputFileName, SaveOptions saveOptions, SplitOptions options) {#split-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.SplitOptions}
```
public static void split(String inputFileName, String outputFileName, SaveOptions saveOptions, SplitOptions options)
```


根据指定的拆分选项，将文档拆分为多个部分，并以指定的保存格式将生成的部分保存为文件。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String | 输入文件名。 |
| outputFileName | java.lang.String | 用于根据规则 "outputFile\_partIndex.extension" 生成文档部分文件名的输出文件名。 |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | 保存选项。 |
| options | [SplitOptions](../../com.aspose.words/splitoptions/) | 文档拆分选项。 |

### split(String inputFileName, String outputFileName, SplitOptions options) {#split-java.lang.String-java.lang.String-com.aspose.words.SplitOptions}
```
public static void split(String inputFileName, String outputFileName, SplitOptions options)
```


根据指定的拆分选项，将文档拆分为多个部分，并将生成的部分保存为文件。输出文件格式由输出文件名的扩展名决定。

 **Examples:** 

展示如何按页拆分文档。

```

 String doc = getMyDir() + "Big document.docx";

 SplitOptions options = new SplitOptions();
 options.setSplitCriteria(SplitCriteria.PAGE);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.1.docx", options);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.2.docx", SaveFormat.DOCX, options);
 
```

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String | 输入文件名。 |
| outputFileName | java.lang.String | 用于根据规则 "outputFile\_partIndex.extension" 生成文档部分文件名的输出文件名。 |
| options | [SplitOptions](../../com.aspose.words/splitoptions/) | 文档拆分选项。 |

### split(String inputFileName, String outputFileName, int saveFormat, SplitOptions options) {#split-java.lang.String-java.lang.String-int-com.aspose.words.SplitOptions}
```
public static void split(String inputFileName, String outputFileName, int saveFormat, SplitOptions options)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| options | [SplitOptions](../../com.aspose.words/splitoptions/) |  |

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
