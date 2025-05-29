---
title: Processor.To
linktitle: To
articleTitle: To
second_title: Aspose.Words for .NET
description: 使用我们的处理器方法优化您的工作流程，该方法明确定义输出文件，提高效率并简化您的数据管理任务。
type: docs
weight: 30
url: /zh/net/aspose.words.lowcode/processor/to/
---
## To(*string, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#to_5}

指定处理器的输出文件。

```csharp
public Processor To(string output, SaveOptions saveOptions = null)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| output | String | 输出文件名。 |
| saveOptions | SaveOptions | 可选的保存选项。如果未指定，则保存格式由文件扩展名决定。 |

### 返回值

返回具有指定输出文件的处理器。

## 评论

如果输出由多个文件组成，则使用指定的输出文件名为每个部分生成文件名 ，遵循规则：'outputFile_partIndex.extension'.

## 例子

展示如何使用上下文通过一行代码转换文档。

```csharp
string doc = MyDir + "Big document.docx";

Converter.Create(new ConverterContext())
    .From(doc)
    .To(ArtifactsDir + "LowCode.ConvertContext.1.pdf")
    .Execute();

Converter.Create(new ConverterContext())
    .From(doc)
    .To(ArtifactsDir + "LowCode.ConvertContext.2.pdf", SaveFormat.Rtf)
    .Execute();

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
Converter.Create(new ConverterContext())
    .From(doc, loadOptions)
    .To(ArtifactsDir + "LowCode.ConvertContext.3.docx", saveOptions)
    .Execute();

Converter.Create(new ConverterContext())
    .From(doc)
    .To(ArtifactsDir + "LowCode.ConvertContext.4.png", new ImageSaveOptions(SaveFormat.Png))
    .Execute();
```

展示如何使用上下文将文档合并为单个输出文档。

```csharp
//合并文档有几种方法：
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
    .From(inputDoc1)
    .From(inputDoc2)
    .To(ArtifactsDir + "LowCode.MergeContextDocuments.1.docx")
    .Execute();

LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
    .From(inputDoc1, firstLoadOptions)
    .From(inputDoc2, secondLoadOptions)
    .To(ArtifactsDir + "LowCode.MergeContextDocuments.2.docx", SaveFormat.Docx)
    .Execute();

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
    .From(inputDoc1)
    .From(inputDoc2)
    .To(ArtifactsDir + "LowCode.MergeContextDocuments.3.docx", saveOptions)
    .Execute();
```

### 也可以看看

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Processor](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## To(*string, [SaveFormat](../../../aspose.words/saveformat/)*) {#to_4}

指定处理器的输出文件。

```csharp
public Processor To(string output, SaveFormat saveFormat)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| output | String | 输出文件名。 |
| saveFormat | SaveFormat | 保存格式。如果未指定，则保存格式由文件扩展名决定。 |

### 返回值

返回具有指定输出文件的处理器。

## 评论

如果输出由多个文件组成，则使用指定的输出文件名为每个部分生成文件名 ，遵循规则：'outputFile_partIndex.extension'.

## 例子

展示如何使用上下文将文档合并为单个输出文档。

```csharp
//合并文档有几种方法：
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
    .From(inputDoc1)
    .From(inputDoc2)
    .To(ArtifactsDir + "LowCode.MergeContextDocuments.1.docx")
    .Execute();

LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
    .From(inputDoc1, firstLoadOptions)
    .From(inputDoc2, secondLoadOptions)
    .To(ArtifactsDir + "LowCode.MergeContextDocuments.2.docx", SaveFormat.Docx)
    .Execute();

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
    .From(inputDoc1)
    .From(inputDoc2)
    .To(ArtifactsDir + "LowCode.MergeContextDocuments.3.docx", saveOptions)
    .Execute();
```

### 也可以看看

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Processor](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## To(*Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#to_3}

指定处理器的输出流。

```csharp
public Processor To(Stream output, SaveOptions saveOptions)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| output | Stream | 输出流。 |
| saveOptions | SaveOptions | 保存选项。 |

### 返回值

返回具有指定输出流的处理器。

## 评论

如果输出由多个文件组成，则只有第一部分将保存到指定的流。

## 例子

展示如何使用上下文通过一行代码从流中转换文档。

```csharp
string doc = MyDir + "Document.docx";
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertContextStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Create(new ConverterContext())
            .From(streamIn)
            .To(streamOut, SaveFormat.Rtf)
            .Execute();

    OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
    LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertContextStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Create(new ConverterContext())
            .From(streamIn, loadOptions)
            .To(streamOut, saveOptions)
            .Execute();

    List<Stream> pages = new List<Stream>();
    Converter.Create(new ConverterContext())
        .From(doc)
        .To(pages, new ImageSaveOptions(SaveFormat.Png))
        .Execute();
}
```

展示如何使用上下文将流中的文档合并为单个输出文档。

```csharp
//合并文档有几种方法：
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

using (FileStream firstStreamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Tables.docx", FileMode.Open, FileAccess.Read))
    {
        OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamContextDocuments.1.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
            .From(firstStreamIn)
            .From(secondStreamIn)
            .To(streamOut, saveOptions)
            .Execute();

        LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
        LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamContextDocuments.2.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
            .From(firstStreamIn, firstLoadOptions)
            .From(secondStreamIn, secondLoadOptions)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
    }
}
```

### 也可以看看

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Processor](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## To(*Stream, [SaveFormat](../../../aspose.words/saveformat/)*) {#to_2}

指定处理器的输出流。

```csharp
public Processor To(Stream output, SaveFormat saveFormat)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| output | Stream | 输出流。 |
| saveFormat | SaveFormat | 保存格式。 |

### 返回值

返回具有指定输出流的处理器。

## 评论

如果输出由多个文件组成，则只有第一部分将保存到指定的流。

## 例子

展示如何使用上下文通过一行代码从流中转换文档。

```csharp
string doc = MyDir + "Document.docx";
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertContextStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Create(new ConverterContext())
            .From(streamIn)
            .To(streamOut, SaveFormat.Rtf)
            .Execute();

    OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
    LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertContextStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Create(new ConverterContext())
            .From(streamIn, loadOptions)
            .To(streamOut, saveOptions)
            .Execute();

    List<Stream> pages = new List<Stream>();
    Converter.Create(new ConverterContext())
        .From(doc)
        .To(pages, new ImageSaveOptions(SaveFormat.Png))
        .Execute();
}
```

展示如何使用上下文将流中的文档合并为单个输出文档。

```csharp
//合并文档有几种方法：
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

using (FileStream firstStreamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Tables.docx", FileMode.Open, FileAccess.Read))
    {
        OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamContextDocuments.1.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
            .From(firstStreamIn)
            .From(secondStreamIn)
            .To(streamOut, saveOptions)
            .Execute();

        LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
        LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamContextDocuments.2.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
            .From(firstStreamIn, firstLoadOptions)
            .From(secondStreamIn, secondLoadOptions)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
    }
}
```

### 也可以看看

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Processor](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## To(*List&lt;Stream&gt;, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#to_1}

指定输出文档流列表。

```csharp
public Processor To(List<Stream> output, SaveOptions saveOptions)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| output | List`1 | 输出文档流列表。 |
| saveOptions | SaveOptions | 保存选项。 |

### 返回值

返回具有指定输出文档流列表的处理器。

## 评论

如果输出包含多个文件（例如图像或拆分的文档部分），则每个部分的流都会添加到指定的列表中。 如果输出是单个文件，则只有一个流会添加到列表中。 最终用户有责任处理已创建的流。

### 也可以看看

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Processor](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## To(*List&lt;Stream&gt;, [SaveFormat](../../../aspose.words/saveformat/)*) {#to}

指定输出文档流列表。

```csharp
public Processor To(List<Stream> output, SaveFormat saveFormat)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| output | List`1 | 输出文档流列表。 |
| saveFormat | SaveFormat | 保存格式。 |

### 返回值

返回具有指定输出文档流列表的处理器。

## 评论

如果输出包含多个文件（例如图像或拆分的文档部分），则每个部分的流都会添加到指定的列表中。 如果输出是单个文件，则只有一个流会添加到列表中。 最终用户有责任处理已创建的流。

### 也可以看看

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Processor](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)
