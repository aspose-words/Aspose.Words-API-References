---
title: Merger.Merge
linktitle: Merge
articleTitle: Merge
second_title: Aspose.Words for .NET
description: 使用我们的“合并”方法，轻松将多个文档合并为一个。立即使用可自定义的文件选项，简化您的工作流程！
type: docs
weight: 20
url: /zh/net/aspose.words.lowcode/merger/merge/
---
## Merge(*string, string[]*) {#merge_8}

使用指定的输入 和输出文件名将给定的输入文档合并为单个输出文档KeepSourceFormatting.

```csharp
public static void Merge(string outputFile, string[] inputFiles)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| outputFile | String | 输出文件名。 |
| inputFiles | String[] | 输入文件名。 |

## 评论

如果输出格式为图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则输出的每一页都将保存为单独的文件。指定的输出文件名将用于生成每个部分的文件名，并遵循以下规则：outputFile_partIndex.extension。

如果输出格式为 TIFF，则输出将保存为单个多帧 TIFF 文件。

## 例子

展示如何将文档合并为单个输出文档。

```csharp
//合并文档有几种方法：
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.1.docx", new[] { inputDoc1, inputDoc2 });

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.2.docx", new[] { inputDoc1, inputDoc2 }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.3.pdf", new[] { inputDoc1, inputDoc2 }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.4.docx", new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Document doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.5.docx");

doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.6.docx");
```

### 也可以看看

* class [Merger](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## Merge(*string, string[], [SaveFormat](../../../aspose.words/saveformat/), [MergeFormatMode](../../mergeformatmode/)*) {#merge_10}

使用指定的输入输出文件名和最终文档格式将给定的输入文档合并为单个输出文档。

```csharp
public static void Merge(string outputFile, string[] inputFiles, SaveFormat saveFormat, 
    MergeFormatMode mergeFormatMode)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| outputFile | String | 输出文件名。 |
| inputFiles | String[] | 输入文件名。 |
| saveFormat | SaveFormat | 保存格式。 |
| mergeFormatMode | MergeFormatMode | 指定如何合并冲突的格式。 |

## 评论

如果输出格式为图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则输出的每一页都将保存为单独的文件。指定的输出文件名将用于生成每个部分的文件名，并遵循以下规则：outputFile_partIndex.extension。

如果输出格式为 TIFF，则输出将保存为单个多帧 TIFF 文件。

## 例子

展示如何将文档合并为单个输出文档。

```csharp
//合并文档有几种方法：
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.1.docx", new[] { inputDoc1, inputDoc2 });

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.2.docx", new[] { inputDoc1, inputDoc2 }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.3.pdf", new[] { inputDoc1, inputDoc2 }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.4.docx", new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Document doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.5.docx");

doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.6.docx");
```

### 也可以看看

* enum [SaveFormat](../../../aspose.words/saveformat/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## Merge(*string, string[], [SaveOptions](../../../aspose.words.saving/saveoptions/), [MergeFormatMode](../../mergeformatmode/)*) {#merge_11}

使用指定的输入输出文件名和保存选项将给定的输入文档合并为单个输出文档。

```csharp
public static void Merge(string outputFile, string[] inputFiles, SaveOptions saveOptions, 
    MergeFormatMode mergeFormatMode)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| outputFile | String | 输出文件名。 |
| inputFiles | String[] | 输入文件名。 |
| saveOptions | SaveOptions | 保存选项。 |
| mergeFormatMode | MergeFormatMode | 指定如何合并冲突的格式。 |

## 评论

如果输出格式为图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则输出的每一页都将保存为单独的文件。指定的输出文件名将用于生成每个部分的文件名，并遵循以下规则：outputFile_partIndex.extension。

如果输出格式为 TIFF，则输出将保存为单个多帧 TIFF 文件。

## 例子

展示如何将文档合并为单个输出文档。

```csharp
//合并文档有几种方法：
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.1.docx", new[] { inputDoc1, inputDoc2 });

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.2.docx", new[] { inputDoc1, inputDoc2 }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.3.pdf", new[] { inputDoc1, inputDoc2 }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.4.docx", new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Document doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.5.docx");

doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.6.docx");
```

### 也可以看看

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## Merge(*string, string[], LoadOptions[], [SaveOptions](../../../aspose.words.saving/saveoptions/), [MergeFormatMode](../../mergeformatmode/)*) {#merge_9}

使用指定的输入输出文件名和保存选项将给定的输入文档合并为单个输出文档。

```csharp
public static void Merge(string outputFile, string[] inputFiles, LoadOptions[] loadOptions, 
    SaveOptions saveOptions, MergeFormatMode mergeFormatMode)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| outputFile | String | 输出文件名。 |
| inputFiles | String[] | 输入文件名。 |
| loadOptions | LoadOptions[] | 输入文件的加载选项。 |
| saveOptions | SaveOptions | 保存选项。 |
| mergeFormatMode | MergeFormatMode | 指定如何合并冲突的格式。 |

## 评论

如果输出格式为图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则输出的每一页都将保存为单独的文件。指定的输出文件名将用于生成每个部分的文件名，并遵循以下规则：outputFile_partIndex.extension。

如果输出格式为 TIFF，则输出将保存为单个多帧 TIFF 文件。

## 例子

展示如何将文档合并为单个输出文档。

```csharp
//合并文档有几种方法：
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.1.docx", new[] { inputDoc1, inputDoc2 });

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.2.docx", new[] { inputDoc1, inputDoc2 }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.3.pdf", new[] { inputDoc1, inputDoc2 }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.4.docx", new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Document doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.5.docx");

doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.6.docx");
```

### 也可以看看

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## Merge(*string[], [MergeFormatMode](../../mergeformatmode/)*) {#merge_4}

将给定的输入文档合并为一个文档并返回[`Document`](../../../aspose.words/document/)最终文档的实例。

```csharp
public static Document Merge(string[] inputFiles, MergeFormatMode mergeFormatMode)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputFiles | String[] | 输入文件名。 |
| mergeFormatMode | MergeFormatMode | 指定如何合并冲突的格式。 |

## 例子

展示如何将文档合并为单个输出文档。

```csharp
//合并文档有几种方法：
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.1.docx", new[] { inputDoc1, inputDoc2 });

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.2.docx", new[] { inputDoc1, inputDoc2 }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.3.pdf", new[] { inputDoc1, inputDoc2 }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.4.docx", new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Document doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.5.docx");

doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.6.docx");
```

### 也可以看看

* class [Document](../../../aspose.words/document/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## Merge(*string[], LoadOptions[], [MergeFormatMode](../../mergeformatmode/)*) {#merge_3}

将给定的输入文档合并为一个文档并返回[`Document`](../../../aspose.words/document/)最终文档的实例。

```csharp
public static Document Merge(string[] inputFiles, LoadOptions[] loadOptions, 
    MergeFormatMode mergeFormatMode)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputFiles | String[] | 输入文件名。 |
| loadOptions | LoadOptions[] | 输入文件的加载选项。 |
| mergeFormatMode | MergeFormatMode | 指定如何合并冲突的格式。 |

## 例子

展示如何将文档合并为单个输出文档。

```csharp
//合并文档有几种方法：
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.1.docx", new[] { inputDoc1, inputDoc2 });

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.2.docx", new[] { inputDoc1, inputDoc2 }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.3.pdf", new[] { inputDoc1, inputDoc2 }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.4.docx", new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Document doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.5.docx");

doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.6.docx");
```

### 也可以看看

* class [Document](../../../aspose.words/document/)
* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## Merge(*Document[], [MergeFormatMode](../../mergeformatmode/)*) {#merge}

将给定的输入文档合并为一个文档并返回[`Document`](../../../aspose.words/document/)最终文档的实例。

```csharp
public static Document Merge(Document[] inputDocuments, MergeFormatMode mergeFormatMode)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputDocuments | Document[] | 输入文件。 |
| mergeFormatMode | MergeFormatMode | 指定如何合并冲突的格式。 |

## 例子

展示如何将输入文档合并为单个文档实例。

```csharp
DocumentBuilder firstDoc = new DocumentBuilder();
firstDoc.Font.Size = 16;
firstDoc.Font.Color = Color.Blue;
firstDoc.Write("Hello first word!");

DocumentBuilder secondDoc = new DocumentBuilder();
secondDoc.Write("Hello second word!");

Document mergedDoc = Merger.Merge(new Document[] { firstDoc.Document, secondDoc.Document }, MergeFormatMode.KeepSourceLayout);
Assert.AreEqual("Hello first word!\fHello second word!\f", mergedDoc.GetText());
```

### 也可以看看

* class [Document](../../../aspose.words/document/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## Merge(*Stream, Stream[], [SaveFormat](../../../aspose.words/saveformat/)*) {#merge_6}

使用指定的输入输出流和最终文档格式将给定的输入文档合并为单个输出文档。

```csharp
public static void Merge(Stream outputStream, Stream[] inputStreams, SaveFormat saveFormat)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| outputStream | Stream | 输出流。 |
| inputStreams | Stream[] | 输入流。 |
| saveFormat | SaveFormat | 保存格式。 |

## 评论

如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则只有输出的第一页会保存到指定的流。

如果输出格式为 TIFF，则输出将作为单个多帧 TIFF 保存到指定的流。

## 例子

展示如何将流中的文档合并为单个输出文档。

```csharp
//有几种方法可以从流中合并文档：
using (FileStream firstStreamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Tables.docx", FileMode.Open, FileAccess.Read))
    {
        OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.1.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, saveOptions, MergeFormatMode.KeepSourceFormatting);

        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.2.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, SaveFormat.Docx);

        LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
        LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.3.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

        Document firstDoc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, MergeFormatMode.MergeFormatting);
        firstDoc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.4.docx");

        Document secondDoc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
        secondDoc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.5.docx");
    }
}
```

### 也可以看看

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Merger](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## Merge(*Stream, Stream[], [SaveOptions](../../../aspose.words.saving/saveoptions/), [MergeFormatMode](../../mergeformatmode/)*) {#merge_7}

使用指定的输入输出流和保存选项将给定的输入文档合并为单个输出文档。

```csharp
public static void Merge(Stream outputStream, Stream[] inputStreams, SaveOptions saveOptions, 
    MergeFormatMode mergeFormatMode)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| outputStream | Stream | 输出流。 |
| inputStreams | Stream[] | 输入流。 |
| saveOptions | SaveOptions | 保存选项。 |
| mergeFormatMode | MergeFormatMode | 指定如何合并冲突的格式。 |

## 评论

如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则只有输出的第一页会保存到指定的流。

如果输出格式为 TIFF，则输出将作为单个多帧 TIFF 保存到指定的流。

## 例子

展示如何将流中的文档合并为单个输出文档。

```csharp
//有几种方法可以从流中合并文档：
using (FileStream firstStreamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Tables.docx", FileMode.Open, FileAccess.Read))
    {
        OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.1.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, saveOptions, MergeFormatMode.KeepSourceFormatting);

        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.2.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, SaveFormat.Docx);

        LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
        LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.3.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

        Document firstDoc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, MergeFormatMode.MergeFormatting);
        firstDoc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.4.docx");

        Document secondDoc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
        secondDoc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.5.docx");
    }
}
```

### 也可以看看

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## Merge(*Stream, Stream[], LoadOptions[], [SaveOptions](../../../aspose.words.saving/saveoptions/), [MergeFormatMode](../../mergeformatmode/)*) {#merge_5}

使用指定的输入输出流和保存选项将给定的输入文档合并为单个输出文档。

```csharp
public static void Merge(Stream outputStream, Stream[] inputStreams, LoadOptions[] loadOptions, 
    SaveOptions saveOptions, MergeFormatMode mergeFormatMode)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| outputStream | Stream | 输出流。 |
| inputStreams | Stream[] | 输入流。 |
| loadOptions | LoadOptions[] | 输入文件的加载选项。 |
| saveOptions | SaveOptions | 保存选项。 |
| mergeFormatMode | MergeFormatMode | 指定如何合并冲突的格式。 |

## 评论

如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则只有输出的第一页会保存到指定的流。

如果输出格式为 TIFF，则输出将作为单个多帧 TIFF 保存到指定的流。

## 例子

展示如何将流中的文档合并为单个输出文档。

```csharp
//有几种方法可以从流中合并文档：
using (FileStream firstStreamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Tables.docx", FileMode.Open, FileAccess.Read))
    {
        OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.1.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, saveOptions, MergeFormatMode.KeepSourceFormatting);

        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.2.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, SaveFormat.Docx);

        LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
        LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.3.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

        Document firstDoc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, MergeFormatMode.MergeFormatting);
        firstDoc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.4.docx");

        Document secondDoc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
        secondDoc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.5.docx");
    }
}
```

### 也可以看看

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## Merge(*Stream[], [MergeFormatMode](../../mergeformatmode/)*) {#merge_2}

将给定的输入文档合并为一个文档并返回[`Document`](../../../aspose.words/document/)最终文档的实例。

```csharp
public static Document Merge(Stream[] inputStreams, MergeFormatMode mergeFormatMode)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputStreams | Stream[] | 输入流。 |
| mergeFormatMode | MergeFormatMode | 指定如何合并冲突的格式。 |

## 例子

展示如何将流中的文档合并为单个输出文档。

```csharp
//有几种方法可以从流中合并文档：
using (FileStream firstStreamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Tables.docx", FileMode.Open, FileAccess.Read))
    {
        OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.1.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, saveOptions, MergeFormatMode.KeepSourceFormatting);

        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.2.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, SaveFormat.Docx);

        LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
        LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.3.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

        Document firstDoc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, MergeFormatMode.MergeFormatting);
        firstDoc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.4.docx");

        Document secondDoc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
        secondDoc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.5.docx");
    }
}
```

### 也可以看看

* class [Document](../../../aspose.words/document/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## Merge(*Stream[], LoadOptions[], [MergeFormatMode](../../mergeformatmode/)*) {#merge_1}

将给定的输入文档合并为一个文档并返回[`Document`](../../../aspose.words/document/)最终文档的实例。

```csharp
public static Document Merge(Stream[] inputStreams, LoadOptions[] loadOptions, 
    MergeFormatMode mergeFormatMode)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputStreams | Stream[] | 输入流。 |
| loadOptions | LoadOptions[] | 输入文件的加载选项。 |
| mergeFormatMode | MergeFormatMode | 指定如何合并冲突的格式。 |

## 例子

展示如何将流中的文档合并为单个输出文档。

```csharp
//有几种方法可以从流中合并文档：
using (FileStream firstStreamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Tables.docx", FileMode.Open, FileAccess.Read))
    {
        OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.1.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, saveOptions, MergeFormatMode.KeepSourceFormatting);

        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.2.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, SaveFormat.Docx);

        LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
        LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.3.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

        Document firstDoc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, MergeFormatMode.MergeFormatting);
        firstDoc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.4.docx");

        Document secondDoc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
        secondDoc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.5.docx");
    }
}
```

### 也可以看看

* class [Document](../../../aspose.words/document/)
* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)
