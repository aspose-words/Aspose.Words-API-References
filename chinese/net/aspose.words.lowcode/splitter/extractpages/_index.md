---
title: Splitter.ExtractPages
linktitle: ExtractPages
articleTitle: ExtractPages
second_title: Aspose.Words for .NET
description: 使用我们的 Splitter ExtractPages 方法，轻松从任何文档中提取特定页面。将其保存为所需的格式，方便访问！
type: docs
weight: 20
url: /zh/net/aspose.words.lowcode/splitter/extractpages/
---
## ExtractPages(*string, string, int, int*) {#extractpages_4}

从文档文件中提取指定范围的页面，并将提取的页面 保存到新文件。输出文件格式由输出文件的扩展名决定。

```csharp
public static void ExtractPages(string inputFileName, string outputFileName, int startPageIndex, 
    int pageCount)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | String | 输入文件名。 |
| outputFileName | String | 输出文件名。 |
| startPageIndex | Int32 | 要提取的第一页的从零开始的索引。 |
| pageCount | Int32 | 要提取的页数。 |

## 例子

显示如何从文档中提取页面。

```csharp
// 有几种方法可以从文档中提取页面：
string doc = MyDir + "Big document.docx";

Splitter.ExtractPages(doc, ArtifactsDir + "LowCode.ExtractPages.1.docx", 0, 2);
Splitter.ExtractPages(doc, ArtifactsDir + "LowCode.ExtractPages.2.docx", SaveFormat.Docx, 0, 2);
```

### 也可以看看

* class [Splitter](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## ExtractPages(*string, string, [SaveFormat](../../../aspose.words/saveformat/), int, int*) {#extractpages_2}

从文档文件中提取指定范围的页面，并使用指定的保存格式将提取的页面 保存到新文件中。

```csharp
public static void ExtractPages(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    int startPageIndex, int pageCount)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | String | 输入文件名。 |
| outputFileName | String | 输出文件名。 |
| saveFormat | SaveFormat | 保存格式。 |
| startPageIndex | Int32 | 要提取的第一页的从零开始的索引。 |
| pageCount | Int32 | 要提取的页数。 |

## 例子

显示如何从文档中提取页面。

```csharp
// 有几种方法可以从文档中提取页面：
string doc = MyDir + "Big document.docx";

Splitter.ExtractPages(doc, ArtifactsDir + "LowCode.ExtractPages.1.docx", 0, 2);
Splitter.ExtractPages(doc, ArtifactsDir + "LowCode.ExtractPages.2.docx", SaveFormat.Docx, 0, 2);
```

### 也可以看看

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Splitter](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## ExtractPages(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), int, int*) {#extractpages_3}

从文档文件中提取指定范围的页面，并使用指定的保存格式将提取的页面 保存到新文件中。

```csharp
public static void ExtractPages(string inputFileName, string outputFileName, 
    SaveOptions saveOptions, int startPageIndex, int pageCount)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | String | 输入文件名。 |
| outputFileName | String | 输出文件名。 |
| saveOptions | SaveOptions | 保存选项。 |
| startPageIndex | Int32 | 要提取的第一页的从零开始的索引。 |
| pageCount | Int32 | 要提取的页数。 |

### 也可以看看

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Splitter](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## ExtractPages(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), int, int*) {#extractpages}

从文档流中提取指定范围的页面，并使用指定的保存格式将提取的页面 保存到输出流。

```csharp
public static void ExtractPages(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    int startPageIndex, int pageCount)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | Stream | 输入流。 |
| outputStream | Stream | 输出流。 |
| saveFormat | SaveFormat | 保存格式。 |
| startPageIndex | Int32 | 要提取的第一页的从零开始的索引。 |
| pageCount | Int32 | 要提取的页数。 |

## 例子

展示如何从流中提取文档的页面。

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ExtractPagesStream.docx", FileMode.Create, FileAccess.ReadWrite))
        Splitter.ExtractPages(streamIn, streamOut, SaveFormat.Docx, 0, 2);
}
```

### 也可以看看

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Splitter](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## ExtractPages(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), int, int*) {#extractpages_1}

从文档流中提取指定范围的页面，并使用指定的保存格式将提取的页面 保存到输出流。

```csharp
public static void ExtractPages(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    int startPageIndex, int pageCount)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | Stream | 输入流。 |
| outputStream | Stream | 输出流。 |
| saveOptions | SaveOptions | 保存选项。 |
| startPageIndex | Int32 | 要提取的第一页的从零开始的索引。 |
| pageCount | Int32 | 要提取的页数。 |

### 也可以看看

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Splitter](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)
