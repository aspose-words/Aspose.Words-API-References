---
title: Replacer Class
linktitle: Replacer
articleTitle: Replacer
second_title: Aspose.Words for .NET
description: 使用 Aspose.Words.LowCode.Replacer 轻松替换文档中的文本。立即简化您的工作流程并增强文档管理！
type: docs
weight: 4340
url: /zh/net/aspose.words.lowcode/replacer/
---
## Replacer class

提供用于查找和替换文档中的文本的方法。

```csharp
public class Replacer : Processor
```

## 方法

| 姓名 | 描述 |
| --- | --- |
| static [Create](../../aspose.words.lowcode/replacer/create/)(*[ReplacerContext](../replacercontext/)*) | 创建替换处理器的新实例。 |
| [Execute](../../aspose.words.lowcode/processor/execute/)() | 执行处理器操作。 |
| [From](../../aspose.words.lowcode/processor/from/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | 指定要处理的输入文档。 |
| [From](../../aspose.words.lowcode/processor/from/)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | 指定要处理的输入文档。 |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveFormat](../../aspose.words/saveformat/)*) | 指定输出文档流列表。 |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | 指定输出文档流列表。 |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveFormat](../../aspose.words/saveformat/)*) | 指定处理器的输出流。 |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | 指定处理器的输出流。 |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveFormat](../../aspose.words/saveformat/)*) | 指定处理器的输出文件。 |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | 指定处理器的输出文件。 |
| static [Replace](../../aspose.words.lowcode/replacer/replace/#replace_9)(*string, string, Regex, string*) | 使用正则表达式将输入文件中所有出现的指定字符串模式替换为替换字符串。 |
| static [Replace](../../aspose.words.lowcode/replacer/replace/#replace_8)(*string, string, string, string*) | 用替换字符串替换输入文件中所有出现的指定字符串模式。 |
| static [Replace](../../aspose.words.lowcode/replacer/replace/#replace_1)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), Regex, string, [FindReplaceOptions](../../aspose.words.replacing/findreplaceoptions/)*) | 使用正则表达式、指定的保存格式和附加选项，将输入流中所有出现的指定字符串模式替换为替换字符串。 |
| static [Replace](../../aspose.words.lowcode/replacer/replace/#replace)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), string, string, [FindReplaceOptions](../../aspose.words.replacing/findreplaceoptions/)*) | 使用指定的保存格式和附加选项，用替换字符串替换输入流中所有出现的指定字符串模式。 |
| static [Replace](../../aspose.words.lowcode/replacer/replace/#replace_3)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), Regex, string, [FindReplaceOptions](../../aspose.words.replacing/findreplaceoptions/)*) | 使用正则表达式、指定的保存格式和附加选项，将输入流中所有出现的指定字符串模式替换为替换字符串。 |
| static [Replace](../../aspose.words.lowcode/replacer/replace/#replace_2)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), string, string, [FindReplaceOptions](../../aspose.words.replacing/findreplaceoptions/)*) | 使用指定的保存格式和附加选项，用替换字符串替换输入流中所有出现的指定字符串模式。 |
| static [Replace](../../aspose.words.lowcode/replacer/replace/#replace_5)(*string, string, [SaveFormat](../../aspose.words/saveformat/), Regex, string, [FindReplaceOptions](../../aspose.words.replacing/findreplaceoptions/)*) | 使用正则表达式、指定的保存格式和附加选项，将输入文件中所有出现的指定字符串模式替换为替换字符串。 |
| static [Replace](../../aspose.words.lowcode/replacer/replace/#replace_4)(*string, string, [SaveFormat](../../aspose.words/saveformat/), string, string, [FindReplaceOptions](../../aspose.words.replacing/findreplaceoptions/)*) | 使用指定的保存格式和附加选项，用替换字符串替换输入文件中所有出现的指定字符串模式。 |
| static [Replace](../../aspose.words.lowcode/replacer/replace/#replace_7)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), Regex, string, [FindReplaceOptions](../../aspose.words.replacing/findreplaceoptions/)*) | 使用正则表达式、指定的保存格式和附加选项，将输入文件中所有出现的指定字符串模式替换为替换字符串。 |
| static [Replace](../../aspose.words.lowcode/replacer/replace/#replace_6)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), string, string, [FindReplaceOptions](../../aspose.words.replacing/findreplaceoptions/)*) | 使用指定的保存格式和附加选项，用替换字符串替换输入文件中所有出现的指定字符串模式。 |
| static [ReplaceToImages](../../aspose.words.lowcode/replacer/replacetoimages/#replacetoimages_1)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), Regex, string, [FindReplaceOptions](../../aspose.words.replacing/findreplaceoptions/)*) | 用替换字符串替换输入文件中所有出现的指定正则表达式模式。 将输出呈现为图像。 |
| static [ReplaceToImages](../../aspose.words.lowcode/replacer/replacetoimages/#replacetoimages)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), string, string, [FindReplaceOptions](../../aspose.words.replacing/findreplaceoptions/)*) | 用替换字符串替换输入文件中所有出现的指定字符串模式。 将输出渲染为图像。 |
| static [ReplaceToImages](../../aspose.words.lowcode/replacer/replacetoimages/#replacetoimages_3)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), Regex, string, [FindReplaceOptions](../../aspose.words.replacing/findreplaceoptions/)*) | 用替换字符串替换输入文件中所有出现的指定正则表达式模式。 将输出呈现为图像。 |
| static [ReplaceToImages](../../aspose.words.lowcode/replacer/replacetoimages/#replacetoimages_2)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), string, string, [FindReplaceOptions](../../aspose.words.replacing/findreplaceoptions/)*) | 用替换字符串替换输入文件中所有出现的指定字符串模式。 将输出渲染为图像。 |

### 也可以看看

* class [Processor](../processor/)
* 命名空间 [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../)
