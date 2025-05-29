---
title: Splitter Class
linktitle: Splitter
articleTitle: Splitter
second_title: Aspose.Words for .NET
description: 使用 Aspose.Words.LowCode.Splitter 类轻松拆分文档。利用多种方法实现精准的文档管理，提升工作流程效率。
type: docs
weight: 4420
url: /zh/net/aspose.words.lowcode/splitter/
---
## Splitter class

提供使用不同标准将文档拆分成多个部分的方法。

```csharp
public class Splitter : Processor
```

## 方法

| 姓名 | 描述 |
| --- | --- |
| static [Create](../../aspose.words.lowcode/splitter/create/)(*[SplitterContext](../splittercontext/)*) | 创建分离器处理器的新实例。 |
| [Execute](../../aspose.words.lowcode/processor/execute/)() | 执行处理器操作。 |
| [From](../../aspose.words.lowcode/processor/from/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | 指定要处理的输入文档。 |
| [From](../../aspose.words.lowcode/processor/from/)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | 指定要处理的输入文档。 |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveFormat](../../aspose.words/saveformat/)*) | 指定输出文档流列表。 |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | 指定输出文档流列表。 |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveFormat](../../aspose.words/saveformat/)*) | 指定处理器的输出流。 |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | 指定处理器的输出流。 |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveFormat](../../aspose.words/saveformat/)*) | 指定处理器的输出文件。 |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | 指定处理器的输出文件。 |
| static [ExtractPages](../../aspose.words.lowcode/splitter/extractpages/#extractpages_4)(*string, string, int, int*) | 从文档文件中提取指定范围的页面，并将提取的页面 保存到新文件。输出文件格式由输出文件的扩展名决定。 |
| static [ExtractPages](../../aspose.words.lowcode/splitter/extractpages/#extractpages)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), int, int*) | 从文档流中提取指定范围的页面，并使用指定的保存格式将提取的页面 保存到输出流。 |
| static [ExtractPages](../../aspose.words.lowcode/splitter/extractpages/#extractpages_1)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), int, int*) | 从文档流中提取指定范围的页面，并使用指定的保存格式将提取的页面 保存到输出流。 |
| static [ExtractPages](../../aspose.words.lowcode/splitter/extractpages/#extractpages_2)(*string, string, [SaveFormat](../../aspose.words/saveformat/), int, int*) | 从文档文件中提取指定范围的页面，并使用指定的保存格式将提取的页面 保存到新文件中。 |
| static [ExtractPages](../../aspose.words.lowcode/splitter/extractpages/#extractpages_3)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), int, int*) | 从文档文件中提取指定范围的页面，并使用指定的保存格式将提取的页面 保存到新文件中。 |
| static [RemoveBlankPages](../../aspose.words.lowcode/splitter/removeblankpages/#removeblankpages_2)(*string, string*) | 从文档中删除空白页并保存输出。返回已删除页码的列表。 |
| static [RemoveBlankPages](../../aspose.words.lowcode/splitter/removeblankpages/#removeblankpages)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/)*) | 从输入流提供的文档中删除空白页，并将更新后的文档 以指定的保存格式保存到输出流。返回已删除页码的列表。 |
| static [RemoveBlankPages](../../aspose.words.lowcode/splitter/removeblankpages/#removeblankpages_1)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | 从输入流提供的文档中删除空白页，并将更新后的文档 以指定的保存格式保存到输出流。返回已删除页码的列表。 |
| static [RemoveBlankPages](../../aspose.words.lowcode/splitter/removeblankpages/#removeblankpages_3)(*string, string, [SaveFormat](../../aspose.words/saveformat/)*) | 从文档中删除空白页，并以指定格式保存输出。返回已删除页码的列表。 |
| static [RemoveBlankPages](../../aspose.words.lowcode/splitter/removeblankpages/#removeblankpages_4)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | 从文档中删除空白页，并以指定格式保存输出。返回已删除页码的列表。 |
| static [Split](../../aspose.words.lowcode/splitter/split/#split)(*Stream, [SaveFormat](../../aspose.words/saveformat/), [SplitOptions](../splitoptions/)*) | 根据指定的拆分选项将输入流中的文档拆分为多个部分，并且 将结果部分作为指定保存格式的流数组返回。 |
| static [Split](../../aspose.words.lowcode/splitter/split/#split_1)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), [SplitOptions](../splitoptions/)*) | 根据指定的拆分选项将输入流中的文档拆分为多个部分，并且 将结果部分作为指定保存格式的流数组返回。 |
| static [Split](../../aspose.words.lowcode/splitter/split/#split_2)(*string, string, [SplitOptions](../splitoptions/)*) | 根据指定的拆分选项将文档拆分为多个部分，并将拆分后的部分保存到文件中。输出文件格式由输出文件的扩展名决定。 |
| static [Split](../../aspose.words.lowcode/splitter/split/#split_3)(*string, string, [SaveFormat](../../aspose.words/saveformat/), [SplitOptions](../splitoptions/)*) | 根据指定的拆分选项将文档拆分为多个部分，并将拆分后的部分保存为指定保存格式的文件中。 |
| static [Split](../../aspose.words.lowcode/splitter/split/#split_4)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), [SplitOptions](../splitoptions/)*) | 根据指定的拆分选项将文档拆分为多个部分，并将拆分后的部分保存为指定保存格式的文件中。 |

### 也可以看看

* class [Processor](../processor/)
* 命名空间 [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../)
