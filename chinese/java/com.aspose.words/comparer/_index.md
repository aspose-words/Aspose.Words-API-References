---
title: "比较器"
linktitle: "比较器"
second_title: "Aspose.Words for Java"
description: "提供用于在 Java 中比较文档的方法。"
type: docs
weight: 114
url: /zh/java/com.aspose.words/comparer/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Processor](../../com.aspose.words/processor/)
```
public class Comparer extends Processor
```

提供用于比较文档的方法。
## 方法

| 方法 | 描述 |
| --- | --- |
| [compare(InputStream v1, InputStream v2, OutputStream outputStream, SaveOptions saveOptions, String author, Date dateTime)](#compare-java.io.InputStream-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.String-java.util.Date) |  |
| [compare(InputStream v1, InputStream v2, OutputStream outputStream, SaveOptions saveOptions, String author, Date dateTime, CompareOptions compareOptions)](#compare-java.io.InputStream-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.String-java.util.Date-com.aspose.words.CompareOptions) |  |
| [compare(InputStream v1, InputStream v2, OutputStream outputStream, int saveFormat, String author, Date dateTime)](#compare-java.io.InputStream-java.io.InputStream-java.io.OutputStream-int-java.lang.String-java.util.Date) |  |
| [compare(InputStream v1, InputStream v2, OutputStream outputStream, int saveFormat, String author, Date dateTime, CompareOptions compareOptions)](#compare-java.io.InputStream-java.io.InputStream-java.io.OutputStream-int-java.lang.String-java.util.Date-com.aspose.words.CompareOptions) |  |
| [compare(String v1, String v2, String outputFileName, SaveOptions saveOptions, String author, Date dateTime)](#compare-java.lang.String-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String-java.util.Date) | 比较两个文档，使用附加选项，并将差异保存到指定的输出文件中，使用提供的保存格式，生成的更改以多个编辑和格式修订的形式呈现。 |
| [compare(String v1, String v2, String outputFileName, SaveOptions saveOptions, String author, Date dateTime, CompareOptions compareOptions)](#compare-java.lang.String-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String-java.util.Date-com.aspose.words.CompareOptions) | 比较两个文档，使用附加选项，并将差异保存到指定的输出文件中，使用提供的保存格式，生成的更改以多个编辑和格式修订的形式呈现。 |
| [compare(String v1, String v2, String outputFileName, int saveFormat, String author, Date dateTime)](#compare-java.lang.String-java.lang.String-java.lang.String-int-java.lang.String-java.util.Date) |  |
| [compare(String v1, String v2, String outputFileName, int saveFormat, String author, Date dateTime, CompareOptions compareOptions)](#compare-java.lang.String-java.lang.String-java.lang.String-int-java.lang.String-java.util.Date-com.aspose.words.CompareOptions) |  |
| [compare(String v1, String v2, String outputFileName, String author, Date dateTime)](#compare-java.lang.String-java.lang.String-java.lang.String-java.lang.String-java.util.Date) | 比较两个文档，使用附加选项，并将差异保存到指定的输出文件中，生成的更改以多个编辑和格式修订的形式呈现。 |
| [compare(String v1, String v2, String outputFileName, String author, Date dateTime, CompareOptions compareOptions)](#compare-java.lang.String-java.lang.String-java.lang.String-java.lang.String-java.util.Date-com.aspose.words.CompareOptions) | 比较两个文档，使用附加选项，并将差异保存到指定的输出文件中，生成的更改以多个编辑和格式修订的形式呈现。 |
| [compareToImages(InputStream v1, InputStream v2, ImageSaveOptions imageSaveOptions, String author, Date dateTime)](#compareToImages-java.io.InputStream-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String-java.util.Date) | 比较两个文档并将差异保存为图像。 |
| [compareToImages(InputStream v1, InputStream v2, ImageSaveOptions imageSaveOptions, String author, Date dateTime, CompareOptions compareOptions)](#compareToImages-java.io.InputStream-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String-java.util.Date-com.aspose.words.CompareOptions) | 比较两个文档并将差异保存为图像。 |
| [compareToImages(String v1, String v2, ImageSaveOptions imageSaveOptions, String author, Date dateTime)](#compareToImages-java.lang.String-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String-java.util.Date) | 比较两个文档并将差异保存为图像。 |
| [compareToImages(String v1, String v2, ImageSaveOptions imageSaveOptions, String author, Date dateTime, CompareOptions compareOptions)](#compareToImages-java.lang.String-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String-java.util.Date-com.aspose.words.CompareOptions) | 比较两个文档并将差异保存为图像。 |
| [create()](#create) | 创建转换处理器的新实例。 |
| [create(ComparerContext context)](#create-com.aspose.words.ComparerContext) | 创建比较器处理器的新实例。 |
| [execute()](#execute) | 执行处理器操作。 |
| [from(InputStream input)](#from-java.io.InputStream) | 指定用于处理的输入文档。 |
| [from(InputStream input, LoadOptions loadOptions)](#from-java.io.InputStream-com.aspose.words.LoadOptions) | 指定用于处理的输入文档。 |
| [from(String input)](#from-java.lang.String) | 指定用于处理的输入文档。 |
| [from(String input, LoadOptions loadOptions)](#from-java.lang.String-com.aspose.words.LoadOptions) | 指定用于处理的输入文档。 |
| [to(OutputStream output, SaveOptions saveOptions)](#to-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [to(OutputStream output, int saveFormat)](#to-java.io.OutputStream-int) |  |
| [to(String output)](#to-java.lang.String) | 指定处理器的输出文件。 |
| [to(String output, SaveOptions saveOptions)](#to-java.lang.String-com.aspose.words.SaveOptions) | 指定处理器的输出文件。 |
| [to(String output, int saveFormat)](#to-java.lang.String-int) |  |
| [to(ArrayList output, SaveOptions saveOptions)](#to-java.util.ArrayList-com.aspose.words.SaveOptions) |  |
| [to(ArrayList output, int saveFormat)](#to-java.util.ArrayList-int) |  |
| [toOutput(ArrayList output, SaveOptions saveOptions)](#toOutput-java.util.ArrayList-com.aspose.words.SaveOptions) |  |
| [toOutput(ArrayList output, int saveFormat)](#toOutput-java.util.ArrayList-int) |  |
### compare(InputStream v1, InputStream v2, OutputStream outputStream, SaveOptions saveOptions, String author, Date dateTime) {#compare-java.io.InputStream-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.String-java.util.Date}
```
public static void compare(InputStream v1, InputStream v2, OutputStream outputStream, SaveOptions saveOptions, String author, Date dateTime)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| v1 | java.io.InputStream |  |
| v2 | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| 作者 | java.lang.String |  |
| 日期时间 | java.util.Date |  |

### compare(InputStream v1, InputStream v2, OutputStream outputStream, SaveOptions saveOptions, String author, Date dateTime, CompareOptions compareOptions) {#compare-java.io.InputStream-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.String-java.util.Date-com.aspose.words.CompareOptions}
```
public static void compare(InputStream v1, InputStream v2, OutputStream outputStream, SaveOptions saveOptions, String author, Date dateTime, CompareOptions compareOptions)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| v1 | java.io.InputStream |  |
| v2 | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| 作者 | java.lang.String |  |
| 日期时间 | java.util.Date |  |
| compareOptions | [CompareOptions](../../com.aspose.words/compareoptions/) |  |

### compare(InputStream v1, InputStream v2, OutputStream outputStream, int saveFormat, String author, Date dateTime) {#compare-java.io.InputStream-java.io.InputStream-java.io.OutputStream-int-java.lang.String-java.util.Date}
```
public static void compare(InputStream v1, InputStream v2, OutputStream outputStream, int saveFormat, String author, Date dateTime)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| v1 | java.io.InputStream |  |
| v2 | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| 作者 | java.lang.String |  |
| 日期时间 | java.util.Date |  |

### compare(InputStream v1, InputStream v2, OutputStream outputStream, int saveFormat, String author, Date dateTime, CompareOptions compareOptions) {#compare-java.io.InputStream-java.io.InputStream-java.io.OutputStream-int-java.lang.String-java.util.Date-com.aspose.words.CompareOptions}
```
public static void compare(InputStream v1, InputStream v2, OutputStream outputStream, int saveFormat, String author, Date dateTime, CompareOptions compareOptions)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| v1 | java.io.InputStream |  |
| v2 | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| 作者 | java.lang.String |  |
| 日期时间 | java.util.Date |  |
| compareOptions | [CompareOptions](../../com.aspose.words/compareoptions/) |  |

### compare(String v1, String v2, String outputFileName, SaveOptions saveOptions, String author, Date dateTime) {#compare-java.lang.String-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String-java.util.Date}
```
public static void compare(String v1, String v2, String outputFileName, SaveOptions saveOptions, String author, Date dateTime)
```


比较两个文档，使用附加选项，并将差异保存到指定的输出文件中，使用提供的保存格式，生成的更改以多个编辑和格式修订的形式呈现。

 **Remarks:** 

如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则 outputFile\_partIndex.extension 为每个部分生成文件名。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| v1 | java.lang.String | 原始文档。 |
| v2 | java.lang.String | 修改后的文档。 |
| outputFileName | java.lang.String | 输出文件名。 |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | 输出的保存选项。 |
| 作者 | java.lang.String | 用于修订的作者缩写。 |
| 日期时间 | java.util.Date | 用于修订的日期和时间。 |

### compare(String v1, String v2, String outputFileName, SaveOptions saveOptions, String author, Date dateTime, CompareOptions compareOptions) {#compare-java.lang.String-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String-java.util.Date-com.aspose.words.CompareOptions}
```
public static void compare(String v1, String v2, String outputFileName, SaveOptions saveOptions, String author, Date dateTime, CompareOptions compareOptions)
```


比较两个文档，使用附加选项，并将差异保存到指定的输出文件中，使用提供的保存格式，生成的更改以多个编辑和格式修订的形式呈现。

 **Remarks:** 

如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则 outputFile\_partIndex.extension 为每个部分生成文件名。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| v1 | java.lang.String | 原始文档。 |
| v2 | java.lang.String | 修改后的文档。 |
| outputFileName | java.lang.String | 输出文件名。 |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | 输出的保存选项。 |
| 作者 | java.lang.String | 用于修订的作者缩写。 |
| 日期时间 | java.util.Date | 用于修订的日期和时间。 |
| compareOptions | [CompareOptions](../../com.aspose.words/compareoptions/) | 文档比较选项。 |

### compare(String v1, String v2, String outputFileName, int saveFormat, String author, Date dateTime) {#compare-java.lang.String-java.lang.String-java.lang.String-int-java.lang.String-java.util.Date}
```
public static void compare(String v1, String v2, String outputFileName, int saveFormat, String author, Date dateTime)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| v1 | java.lang.String |  |
| v2 | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| 作者 | java.lang.String |  |
| 日期时间 | java.util.Date |  |

### compare(String v1, String v2, String outputFileName, int saveFormat, String author, Date dateTime, CompareOptions compareOptions) {#compare-java.lang.String-java.lang.String-java.lang.String-int-java.lang.String-java.util.Date-com.aspose.words.CompareOptions}
```
public static void compare(String v1, String v2, String outputFileName, int saveFormat, String author, Date dateTime, CompareOptions compareOptions)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| v1 | java.lang.String |  |
| v2 | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| 作者 | java.lang.String |  |
| 日期时间 | java.util.Date |  |
| compareOptions | [CompareOptions](../../com.aspose.words/compareoptions/) |  |

### compare(String v1, String v2, String outputFileName, String author, Date dateTime) {#compare-java.lang.String-java.lang.String-java.lang.String-java.lang.String-java.util.Date}
```
public static void compare(String v1, String v2, String outputFileName, String author, Date dateTime)
```


比较两个文档，使用附加选项，并将差异保存到指定的输出文件中，生成的更改以多个编辑和格式修订的形式呈现。

 **Remarks:** 

如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则 outputFile\_partIndex.extension 为每个部分生成文件名。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| v1 | java.lang.String | 原始文档。 |
| v2 | java.lang.String | 修改后的文档。 |
| outputFileName | java.lang.String | 输出文件名。 |
| 作者 | java.lang.String | 用于修订的作者缩写。 |
| 日期时间 | java.util.Date | 用于修订的日期和时间。 |

### compare(String v1, String v2, String outputFileName, String author, Date dateTime, CompareOptions compareOptions) {#compare-java.lang.String-java.lang.String-java.lang.String-java.lang.String-java.util.Date-com.aspose.words.CompareOptions}
```
public static void compare(String v1, String v2, String outputFileName, String author, Date dateTime, CompareOptions compareOptions)
```


比较两个文档，使用附加选项，并将差异保存到指定的输出文件中，生成的更改以多个编辑和格式修订的形式呈现。

 **Remarks:** 

如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则 outputFile\_partIndex.extension 为每个部分生成文件名。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

 **Examples:** 

展示如何简单比较文档。

```

 // There is a several ways to compare documents:
 String firstDoc = getMyDir() + "Table column bookmarks.docx";
 String secondDoc = getMyDir() + "Table column bookmarks.doc";

 Comparer.compare(firstDoc, secondDoc, getArtifactsDir() + "LowCode.CompareDocuments.1.docx", "Author", new Date());
 Comparer.compare(firstDoc, secondDoc, getArtifactsDir() + "LowCode.CompareDocuments.2.docx", SaveFormat.DOCX, "Author", new Date());
 CompareOptions options = new CompareOptions();
 options.setIgnoreCaseChanges(true);
 Comparer.compare(firstDoc, secondDoc, getArtifactsDir() + "LowCode.CompareDocuments.3.docx", "Author", new Date(), options);
 Comparer.compare(firstDoc, secondDoc, getArtifactsDir() + "LowCode.CompareDocuments.4.docx", SaveFormat.DOCX, "Author", new Date(), options);
 
```

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| v1 | java.lang.String | 原始文档。 |
| v2 | java.lang.String | 修改后的文档。 |
| outputFileName | java.lang.String | 输出文件名。 |
| 作者 | java.lang.String | 用于修订的作者缩写。 |
| 日期时间 | java.util.Date | 用于修订的日期和时间。 |
| compareOptions | [CompareOptions](../../com.aspose.words/compareoptions/) | 文档比较选项。 |

### compareToImages(InputStream v1, InputStream v2, ImageSaveOptions imageSaveOptions, String author, Date dateTime) {#compareToImages-java.io.InputStream-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String-java.util.Date}
```
public static OutputStream[] compareToImages(InputStream v1, InputStream v2, ImageSaveOptions imageSaveOptions, String author, Date dateTime)
```


比较两个文档并将差异保存为图像。返回数组中的每个项代表输出的单页，以图像形式呈现。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| v1 | java.io.InputStream | 原始文档。 |
| v2 | java.io.InputStream | 修改后的文档。 |
| imageSaveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | 输出的图像保存选项。 |
| 作者 | java.lang.String | 用于修订的作者缩写。 |
| 日期时间 | java.util.Date | 用于修订的日期和时间。 |

**Returns:**
java.io.OutputStream[]
### compareToImages(InputStream v1, InputStream v2, ImageSaveOptions imageSaveOptions, String author, Date dateTime, CompareOptions compareOptions) {#compareToImages-java.io.InputStream-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String-java.util.Date-com.aspose.words.CompareOptions}
```
public static OutputStream[] compareToImages(InputStream v1, InputStream v2, ImageSaveOptions imageSaveOptions, String author, Date dateTime, CompareOptions compareOptions)
```


比较两个文档并将差异保存为图像。返回数组中的每个项代表输出的单页，以图像形式呈现。

 **Examples:** 

展示如何比较文档并将结果保存为图像。

```

 // There is a several ways to compare documents:
 String firstDoc = getMyDir() + "Table column bookmarks.docx";
 String secondDoc = getMyDir() + "Table column bookmarks.doc";

 OutputStream[] pages = Comparer.compareToImages(firstDoc, secondDoc, new ImageSaveOptions(SaveFormat.PNG), "Author", new Date());

 try (FileInputStream firstStreamIn = new FileInputStream(firstDoc)) {
     try (FileInputStream secondStreamIn = new FileInputStream(secondDoc)) {
         CompareOptions compareOptions = new CompareOptions();
         compareOptions.setIgnoreCaseChanges(true);
         pages = Comparer.compareToImages(firstStreamIn, secondStreamIn, new ImageSaveOptions(SaveFormat.PNG), "Author", new Date(), compareOptions);
     }
 }
 
```

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| v1 | java.io.InputStream | 原始文档。 |
| v2 | java.io.InputStream | 修改后的文档。 |
| imageSaveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | 输出的图像保存选项。 |
| 作者 | java.lang.String | 用于修订的作者缩写。 |
| 日期时间 | java.util.Date | 用于修订的日期和时间。 |
| compareOptions | [CompareOptions](../../com.aspose.words/compareoptions/) | 文档比较选项。 |

**Returns:**
java.io.OutputStream[]
### compareToImages(String v1, String v2, ImageSaveOptions imageSaveOptions, String author, Date dateTime) {#compareToImages-java.lang.String-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String-java.util.Date}
```
public static OutputStream[] compareToImages(String v1, String v2, ImageSaveOptions imageSaveOptions, String author, Date dateTime)
```


比较两个文档并将差异保存为图像。返回数组中的每个项代表输出的单页，以图像形式呈现。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| v1 | java.lang.String | 原始文档。 |
| v2 | java.lang.String | 修改后的文档。 |
| imageSaveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | 输出的图像保存选项。 |
| 作者 | java.lang.String | 用于修订的作者缩写。 |
| 日期时间 | java.util.Date | 用于修订的日期和时间。 |

**Returns:**
java.io.OutputStream[]
### compareToImages(String v1, String v2, ImageSaveOptions imageSaveOptions, String author, Date dateTime, CompareOptions compareOptions) {#compareToImages-java.lang.String-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String-java.util.Date-com.aspose.words.CompareOptions}
```
public static OutputStream[] compareToImages(String v1, String v2, ImageSaveOptions imageSaveOptions, String author, Date dateTime, CompareOptions compareOptions)
```


比较两个文档并将差异保存为图像。返回数组中的每个项代表输出的单页，以图像形式呈现。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| v1 | java.lang.String | 原始文档。 |
| v2 | java.lang.String | 修改后的文档。 |
| imageSaveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | 输出的图像保存选项。 |
| 作者 | java.lang.String | 用于修订的作者缩写。 |
| 日期时间 | java.util.Date | 用于修订的日期和时间。 |
| compareOptions | [CompareOptions](../../com.aspose.words/compareoptions/) | 文档比较选项。 |

**Returns:**
java.io.OutputStream[]
### create() {#create}
```
public static Comparer create()
```


创建转换处理器的新实例。

**Returns:**
[Comparer](../../com.aspose.words/comparer/)
### create(ComparerContext context) {#create-com.aspose.words.ComparerContext}
```
public static Comparer create(ComparerContext context)
```


创建比较器处理器的新实例。

 **Examples:** 

展示如何使用上下文简单比较文档。

```

 // There is a several ways to compare documents:
 String firstDoc = getMyDir() + "Table column bookmarks.docx";
 String secondDoc = getMyDir() + "Table column bookmarks.doc";

 ComparerContext comparerContext = new ComparerContext();
 comparerContext.getCompareOptions().setIgnoreCaseChanges(true);
 comparerContext.setAuthor("Author");
 comparerContext.setDateTime(new Date());

 Comparer.create(comparerContext)
         .from(firstDoc)
         .from(secondDoc)
         .to(getArtifactsDir() + "LowCode.CompareContextDocuments.docx")
         .execute();
 
```

展示如何使用上下文从流中比较文档。

```

 // There is a several ways to compare documents from the stream:
 try (FileInputStream firstStreamIn = new FileInputStream(getMyDir() + "Table column bookmarks.docx")) {
     try (FileInputStream secondStreamIn = new FileInputStream(getMyDir() + "Table column bookmarks.doc")) {
         ComparerContext comparerContext = new ComparerContext();
         comparerContext.getCompareOptions().setIgnoreCaseChanges(true);
         comparerContext.setAuthor("Author");
         comparerContext.setDateTime(new Date());

         try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.CompareContextStreamDocuments.docx")) {
             Comparer.create(comparerContext)
                     .from(firstStreamIn)
                     .from(secondStreamIn)
                     .to(streamOut, SaveFormat.DOCX)
                     .execute();
         }
     }
 }
 
```

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| context | [ComparerContext](../../com.aspose.words/comparercontext/) |  |

**Returns:**
[Comparer](../../com.aspose.words/comparer/)
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
