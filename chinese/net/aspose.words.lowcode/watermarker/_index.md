---
title: Watermarker Class
linktitle: Watermarker
articleTitle: Watermarker
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.LowCode.Watermarker 类，轻松在文档中插入水印。轻松提升文档呈现效果！
type: docs
weight: 4440
url: /zh/net/aspose.words.lowcode/watermarker/
---
## Watermarker class

提供用于在文档中插入水印的方法。

```csharp
public class Watermarker : Processor
```

## 方法

| 姓名 | 描述 |
| --- | --- |
| static [Create](../../aspose.words.lowcode/watermarker/create/)(*[WatermarkerContext](../watermarkercontext/)*) | 创建水印处理器的新实例。 |
| [Execute](../../aspose.words.lowcode/processor/execute/)() | 执行处理器操作。 |
| [From](../../aspose.words.lowcode/processor/from/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | 指定要处理的输入文档。 |
| [From](../../aspose.words.lowcode/processor/from/)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | 指定要处理的输入文档。 |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveFormat](../../aspose.words/saveformat/)*) | 指定输出文档流列表。 |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | 指定输出文档流列表。 |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveFormat](../../aspose.words/saveformat/)*) | 指定处理器的输出流。 |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | 指定处理器的输出流。 |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveFormat](../../aspose.words/saveformat/)*) | 指定处理器的输出文件。 |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | 指定处理器的输出文件。 |
| static [SetImage](../../aspose.words.lowcode/watermarker/setimage/#setimage_6)(*string, string, string*) | 在文档中添加图像水印。 |
| static [SetImage](../../aspose.words.lowcode/watermarker/setimage/#setimage_7)(*string, string, string, [ImageWatermarkOptions](../../aspose.words/imagewatermarkoptions/)*) | 使用选项将图像水印添加到文档中。 |
| static [SetImage](../../aspose.words.lowcode/watermarker/setimage/#setimage)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), Image, [ImageWatermarkOptions](../../aspose.words/imagewatermarkoptions/)*) | 使用选项从流中将图像水印添加到文档中。 |
| static [SetImage](../../aspose.words.lowcode/watermarker/setimage/#setimage_1)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), Stream, [ImageWatermarkOptions](../../aspose.words/imagewatermarkoptions/)*) | 使用选项从流中将图像水印添加到文档中。 |
| static [SetImage](../../aspose.words.lowcode/watermarker/setimage/#setimage_2)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), Image, [ImageWatermarkOptions](../../aspose.words/imagewatermarkoptions/)*) | 使用选项从流中将图像水印添加到文档中。 |
| static [SetImage](../../aspose.words.lowcode/watermarker/setimage/#setimage_3)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), Stream, [ImageWatermarkOptions](../../aspose.words/imagewatermarkoptions/)*) | 使用选项从流中将图像水印添加到文档中。 |
| static [SetImage](../../aspose.words.lowcode/watermarker/setimage/#setimage_4)(*string, string, [SaveFormat](../../aspose.words/saveformat/), string, [ImageWatermarkOptions](../../aspose.words/imagewatermarkoptions/)*) | 使用选项和指定的保存格式将图像水印添加到文档中。 |
| static [SetImage](../../aspose.words.lowcode/watermarker/setimage/#setimage_5)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), string, [ImageWatermarkOptions](../../aspose.words/imagewatermarkoptions/)*) | 使用选项和指定的保存格式将图像水印添加到文档中。 |
| static [SetText](../../aspose.words.lowcode/watermarker/settext/#settext_4)(*string, string, string*) | 在文档中添加文本水印。 |
| static [SetText](../../aspose.words.lowcode/watermarker/settext/#settext_5)(*string, string, string, [TextWatermarkOptions](../../aspose.words/textwatermarkoptions/)*) | 使用选项在文档中添加文本水印。 |
| static [SetText](../../aspose.words.lowcode/watermarker/settext/#settext)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), string, [TextWatermarkOptions](../../aspose.words/textwatermarkoptions/)*) | 使用选项从流中将文本水印添加到文档中。 |
| static [SetText](../../aspose.words.lowcode/watermarker/settext/#settext_1)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), string, [TextWatermarkOptions](../../aspose.words/textwatermarkoptions/)*) | 使用选项从流中将文本水印添加到文档中。 |
| static [SetText](../../aspose.words.lowcode/watermarker/settext/#settext_2)(*string, string, [SaveFormat](../../aspose.words/saveformat/), string, [TextWatermarkOptions](../../aspose.words/textwatermarkoptions/)*) | 使用选项和指定的保存格式在文档中添加文本水印。 |
| static [SetText](../../aspose.words.lowcode/watermarker/settext/#settext_3)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), string, [TextWatermarkOptions](../../aspose.words/textwatermarkoptions/)*) | 使用选项和指定的保存格式在文档中添加文本水印。 |
| static [SetWatermarkToImages](../../aspose.words.lowcode/watermarker/setwatermarktoimages/#setwatermarktoimages)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), Stream, [ImageWatermarkOptions](../../aspose.words/imagewatermarkoptions/)*) | 使用选项在文档中添加图像水印。将输出渲染为图像。 |
| static [SetWatermarkToImages](../../aspose.words.lowcode/watermarker/setwatermarktoimages/#setwatermarktoimages_1)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), string, [TextWatermarkOptions](../../aspose.words/textwatermarkoptions/)*) | 使用选项在文档中添加文本水印。将输出渲染为图像。 |
| static [SetWatermarkToImages](../../aspose.words.lowcode/watermarker/setwatermarktoimages/#setwatermarktoimages_2)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), byte[], [ImageWatermarkOptions](../../aspose.words/imagewatermarkoptions/)*) | 使用选项在文档中添加图像水印。将输出渲染为图像。 |
| static [SetWatermarkToImages](../../aspose.words.lowcode/watermarker/setwatermarktoimages/#setwatermarktoimages_3)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), string, [TextWatermarkOptions](../../aspose.words/textwatermarkoptions/)*) | 使用选项在文档中添加文本水印。将输出渲染为图像。 |

### 也可以看看

* class [Processor](../processor/)
* 命名空间 [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../)
