---
title: Comparer Class
linktitle: Comparer
articleTitle: Comparer
second_title: Aspose.Words for .NET
description: 使用 Aspose.Words LowCode Comparer 类轻松比较文档。解锁强大的方法，实现无缝的文档分析和协作。
type: docs
weight: 4210
url: /zh/net/aspose.words.lowcode/comparer/
---
## Comparer class

提供用于比较文档的方法。

```csharp
public class Comparer : Processor
```

## 方法

| 姓名 | 描述 |
| --- | --- |
| static [Create](../../aspose.words.lowcode/comparer/create/#create)() | 创建转换器处理器的新实例。 |
| static [Create](../../aspose.words.lowcode/comparer/create/#create_1)(*[ComparerContext](../comparercontext/)*) | 创建比较器处理器的新实例。 |
| [Execute](../../aspose.words.lowcode/processor/execute/)() | 执行处理器操作。 |
| [From](../../aspose.words.lowcode/processor/from/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | 指定要处理的输入文档。 |
| [From](../../aspose.words.lowcode/processor/from/)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | 指定要处理的输入文档。 |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveFormat](../../aspose.words/saveformat/)*) | 指定输出文档流列表。 |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | 指定输出文档流列表。 |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveFormat](../../aspose.words/saveformat/)*) | 指定处理器的输出流。 |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | 指定处理器的输出流。 |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveFormat](../../aspose.words/saveformat/)*) | 指定处理器的输出文件。 |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | 指定处理器的输出文件。 |
| static [Compare](../../aspose.words.lowcode/comparer/compare/#compare_4)(*string, string, string, string, DateTime, [CompareOptions](../../aspose.words.comparing/compareoptions/)*) | 使用附加选项比较两个文档，并将差异保存到指定的输出文件， 产生许多编辑和格式修订的更改。 |
| static [Compare](../../aspose.words.lowcode/comparer/compare/#compare)(*Stream, Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), string, DateTime, [CompareOptions](../../aspose.words.comparing/compareoptions/)*) | 使用附加选项比较从流中加载的两个文档，并将差异以指定的保存格式保存到提供的输出流中， 产生许多编辑和格式修订的更改。 |
| static [Compare](../../aspose.words.lowcode/comparer/compare/#compare_1)(*Stream, Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), string, DateTime, [CompareOptions](../../aspose.words.comparing/compareoptions/)*) | 使用附加选项比较从流中加载的两个文档，并将差异以指定的保存格式保存到提供的输出流中， 产生许多编辑和格式修订的更改。 |
| static [Compare](../../aspose.words.lowcode/comparer/compare/#compare_2)(*string, string, string, [SaveFormat](../../aspose.words/saveformat/), string, DateTime, [CompareOptions](../../aspose.words.comparing/compareoptions/)*) | 使用附加选项比较两个文档，并将差异以提供的保存格式保存到指定的输出文件中， 产生许多编辑和格式修订的更改。 |
| static [Compare](../../aspose.words.lowcode/comparer/compare/#compare_3)(*string, string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), string, DateTime, [CompareOptions](../../aspose.words.comparing/compareoptions/)*) | 使用附加选项比较两个文档，并将差异以提供的保存格式保存到指定的输出文件中， 产生许多编辑和格式修订的更改。 |
| static [CompareToImages](../../aspose.words.lowcode/comparer/comparetoimages/#comparetoimages)(*Stream, Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), string, DateTime, [CompareOptions](../../aspose.words.comparing/compareoptions/)*) | 比较两个文档并将差异保存为图像。 返回数组中的每个项目都代表以图像形式呈现的输出的单个页面。 |
| static [CompareToImages](../../aspose.words.lowcode/comparer/comparetoimages/#comparetoimages_1)(*string, string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), string, DateTime, [CompareOptions](../../aspose.words.comparing/compareoptions/)*) | 比较两个文档并将差异保存为图像。 返回数组中的每个项目都代表以图像形式呈现的输出的单个页面。 |

### 也可以看看

* class [Processor](../processor/)
* 命名空间 [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../)
