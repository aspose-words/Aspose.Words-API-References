---
title: IDocumentProcessorPlugin Interface
linktitle: IDocumentProcessorPlugin
articleTitle: IDocumentProcessorPlugin
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words IDocumentProcessorPlugin 接口，通过强大的外部插件增强您的文档处理能力，实现无缝集成。
type: docs
weight: 3610
url: /zh/net/aspose.words/idocumentprocessorplugin/
---
## IDocumentProcessorPlugin interface

定义外部文档处理器插件的接口。

```csharp
public interface IDocumentProcessorPlugin
```

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Append](../../aspose.words/idocumentprocessorplugin/append/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | 使用指定的加载选项附加加载文档。 |
| [Load](../../aspose.words/idocumentprocessorplugin/load/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | 使用指定的加载选项加载文档。 |
| [Save](../../aspose.words/idocumentprocessorplugin/save/)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | 保存由加载的文档[`Load`](./load/)方法使用指定的保存选项将数据保存到输出流。 |
| [SetImageWatermark](../../aspose.words/idocumentprocessorplugin/setimagewatermark/)(*Stream, [ImageWatermarkOptions](../imagewatermarkoptions/)*) | 在加载的文档的每一页上添加图像水印[`Load`](./load/)方法. |
| [SetTextWatermark](../../aspose.words/idocumentprocessorplugin/settextwatermark/)(*string, [TextWatermarkOptions](../textwatermarkoptions/)*) | 在加载的文档的每一页上添加文本水印[`Load`](./load/)方法. |
| [ToDocument](../../aspose.words/idocumentprocessorplugin/todocument/)() | 解析由加载的文档[`Load`](./load/)方法[`Document`](../document/)对象. |
| [ToPages](../../aspose.words/idocumentprocessorplugin/topages/)(*[FixedPageSaveOptions](../../aspose.words.saving/fixedpagesaveoptions/)*) | 保存由[`Load`](./load/)使用指定的固定页面保存选项的方法。 |

### 也可以看看

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
