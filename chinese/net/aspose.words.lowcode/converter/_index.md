---
title: Converter Class
linktitle: Converter
articleTitle: Converter
second_title: Aspose.Words for .NET
description: 使用 Aspose.Words.LowCode.Converter 轻松转换各种文档类型。只需一行代码即可实现无缝集成，简化您的工作流程。
type: docs
weight: 4230
url: /zh/net/aspose.words.lowcode/converter/
---
## Converter class

表示一组旨在使用一行代码转换各种不同类型的文档的方法。

```csharp
public class Converter : Processor
```

## 方法

| 姓名 | 描述 |
| --- | --- |
| static [Create](../../aspose.words.lowcode/converter/create/#create)() | 创建转换器处理器的新实例。 |
| static [Create](../../aspose.words.lowcode/converter/create/#create_1)(*[ConverterContext](../convertercontext/)*) | 创建转换器处理器的新实例。 |
| [Execute](../../aspose.words.lowcode/processor/execute/)() | 执行处理器操作。 |
| [From](../../aspose.words.lowcode/processor/from/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | 指定要处理的输入文档。 |
| [From](../../aspose.words.lowcode/processor/from/)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | 指定要处理的输入文档。 |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveFormat](../../aspose.words/saveformat/)*) | 指定输出文档流列表。 |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | 指定输出文档流列表。 |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveFormat](../../aspose.words/saveformat/)*) | 指定处理器的输出流。 |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | 指定处理器的输出流。 |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveFormat](../../aspose.words/saveformat/)*) | 指定处理器的输出文件。 |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | 指定处理器的输出文件。 |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert_4)(*string, string*) | 使用指定的输入输出文件名及其扩展名将给定的输入文档转换为输出文档。 |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert_1)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/)*) | 使用指定的输入和输出流将给定的输入文档转换为单个输出文档。 |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert_2)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | 使用指定的输入和输出流将给定的输入文档转换为单个输出文档。 |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert_5)(*string, string, [SaveFormat](../../aspose.words/saveformat/)*) | 使用指定的输入输出文件名和最终文档格式将给定的输入文档转换为输出文档。 |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert_6)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | 使用指定的输入输出文件名和保存选项将给定的输入文档转换为输出文档。 |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/), Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | 使用指定的输入和输出流将给定的输入文档转换为单个输出文档。 |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert_3)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/), string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | 使用指定的输入输出文件名及其加载/保存选项将给定的输入文档转换为输出文档。 |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_1)(*[Document](../../aspose.words/document/), [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | 使用指定的保存选项将指定文档的页面转换为图像，并返回包含图像的流数组。 |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages)(*[Document](../../aspose.words/document/), [SaveFormat](../../aspose.words/saveformat/)*) | 将指定文档的页面转换为指定格式的图像，并返回包含图像的流数组。 |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_4)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | 使用指定的保存选项将指定输入流的页面转换为图像，并返回包含图像的流数组。 |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_3)(*Stream, [SaveFormat](../../aspose.words/saveformat/)*) | 将指定输入流的页面转换为指定格式的图像，并返回包含图像的流数组。 |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_6)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | 使用指定的保存选项将指定输入文件的页面转换为图像，并返回包含图像的流数组。 |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_5)(*string, [SaveFormat](../../aspose.words/saveformat/)*) | 将指定输入文件的页面转换为指定格式的图像，并返回包含图像的流数组。 |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_2)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/), [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | 使用提供的加载和保存选项将指定输入流的页面转换为图像，并返回包含图像的流数组。 |

## 评论

指定的输入和输出文件或流以及所需的保存格式 用于将一种格式的给定输入文档转换为另一种指定格式的输出文档 。

转换功能支持超过 35 种不同的文件格式。

这[`ConvertToImages`](./converttoimages/)这组方法旨在将文档转换为图像，其中每页都被转换为单独的图像文件。这些方法还可以将 PDF 文档直接转换为固定页面格式，而无需将其加载到文档模型中，从而提高性能和准确性。

和[`PageSet`](../../aspose.words.saving/imagesaveoptions/pageset/)，您可以指定一组特定的页面转换为图像。

### 也可以看看

* class [Processor](../processor/)
* 命名空间 [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../)
