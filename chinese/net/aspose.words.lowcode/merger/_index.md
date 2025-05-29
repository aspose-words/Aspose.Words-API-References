---
title: Merger Class
linktitle: Merger
articleTitle: Merger
second_title: Aspose.Words for .NET
description: 使用 Aspose.Words.LowCode.Merger 类轻松将不同类型的文档合并为一个。立即简化您的工作流程，提升工作效率！
type: docs
weight: 4300
url: /zh/net/aspose.words.lowcode/merger/
---
## Merger class

表示一组用于将各种不同类型的文档合并为单个输出文档的方法。

```csharp
public class Merger : Processor
```

## 方法

| 姓名 | 描述 |
| --- | --- |
| static [Create](../../aspose.words.lowcode/merger/create/#create)() | 创建邮件合并处理器的新实例。 |
| static [Create](../../aspose.words.lowcode/merger/create/#create_1)(*[MergerContext](../mergercontext/)*) | 创建邮件合并处理器的新实例。 |
| [Execute](../../aspose.words.lowcode/processor/execute/)() | 执行处理器操作。 |
| [From](../../aspose.words.lowcode/processor/from/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | 指定要处理的输入文档。 |
| [From](../../aspose.words.lowcode/processor/from/)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | 指定要处理的输入文档。 |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveFormat](../../aspose.words/saveformat/)*) | 指定输出文档流列表。 |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | 指定输出文档流列表。 |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveFormat](../../aspose.words/saveformat/)*) | 指定处理器的输出流。 |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | 指定处理器的输出流。 |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveFormat](../../aspose.words/saveformat/)*) | 指定处理器的输出文件。 |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | 指定处理器的输出文件。 |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge)(*Document[], [MergeFormatMode](../mergeformatmode/)*) | 将给定的输入文档合并为一个文档并返回[`Document`](../../aspose.words/document/)最终文档的实例。 |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_2)(*Stream[], [MergeFormatMode](../mergeformatmode/)*) | 将给定的输入文档合并为一个文档并返回[`Document`](../../aspose.words/document/)最终文档的实例。 |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_8)(*string, string[]*) | 使用指定的输入 和输出文件名将给定的输入文档合并为单个输出文档KeepSourceFormatting. |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_4)(*string[], [MergeFormatMode](../mergeformatmode/)*) | 将给定的输入文档合并为一个文档并返回[`Document`](../../aspose.words/document/)最终文档的实例。 |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_6)(*Stream, Stream[], [SaveFormat](../../aspose.words/saveformat/)*) | 使用指定的输入输出流和最终文档格式将给定的输入文档合并为单个输出文档。 |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_1)(*Stream[], LoadOptions[], [MergeFormatMode](../mergeformatmode/)*) | 将给定的输入文档合并为一个文档并返回[`Document`](../../aspose.words/document/)最终文档的实例。 |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_3)(*string[], LoadOptions[], [MergeFormatMode](../mergeformatmode/)*) | 将给定的输入文档合并为一个文档并返回[`Document`](../../aspose.words/document/)最终文档的实例。 |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_7)(*Stream, Stream[], [SaveOptions](../../aspose.words.saving/saveoptions/), [MergeFormatMode](../mergeformatmode/)*) | 使用指定的输入输出流和保存选项将给定的输入文档合并为单个输出文档。 |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_10)(*string, string[], [SaveFormat](../../aspose.words/saveformat/), [MergeFormatMode](../mergeformatmode/)*) | 使用指定的输入输出文件名和最终文档格式将给定的输入文档合并为单个输出文档。 |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_11)(*string, string[], [SaveOptions](../../aspose.words.saving/saveoptions/), [MergeFormatMode](../mergeformatmode/)*) | 使用指定的输入输出文件名和保存选项将给定的输入文档合并为单个输出文档。 |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_5)(*Stream, Stream[], LoadOptions[], [SaveOptions](../../aspose.words.saving/saveoptions/), [MergeFormatMode](../mergeformatmode/)*) | 使用指定的输入输出流和保存选项将给定的输入文档合并为单个输出文档。 |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_9)(*string, string[], LoadOptions[], [SaveOptions](../../aspose.words.saving/saveoptions/), [MergeFormatMode](../mergeformatmode/)*) | 使用指定的输入输出文件名和保存选项将给定的输入文档合并为单个输出文档。 |
| static [MergeToImages](../../aspose.words.lowcode/merger/mergetoimages/#mergetoimages)(*Stream[], [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), [MergeFormatMode](../mergeformatmode/)*) | 使用指定的图像保存选项将给定的输入文档流合并为单个输出文档。 将输出呈现为图像。 |
| static [MergeToImages](../../aspose.words.lowcode/merger/mergetoimages/#mergetoimages_1)(*string[], [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), [MergeFormatMode](../mergeformatmode/)*) | 使用指定的输入输出文件名和保存选项将给定的输入文档合并为单个输出文档。 将输出呈现为图像。 |

## 评论

指定的输入和输出文件或流以及所需的合并和保存选项 用于将给定的输入文档合并为单个输出文档。

合并功能支持超过 35 种不同的文件格式。

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

* class [Processor](../processor/)
* 命名空间 [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../)
