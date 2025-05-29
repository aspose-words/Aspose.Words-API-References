---
title: SummarizeOptions Class
linktitle: SummarizeOptions
articleTitle: SummarizeOptions
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.AI.SummarizeOptions 类来定制和增强您的文档摘要，以获得更清晰的见解和改进的内容管理。
type: docs
weight: 100
url: /zh/net/aspose.words.ai/summarizeoptions/
---
## SummarizeOptions class

允许指定用于总结文档内容的各种选项。

```csharp
public class SummarizeOptions
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [SummarizeOptions](summarizeoptions/)() | 初始化一个新的实例`SummarizeOptions`类. |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [SummaryLength](../../aspose.words.ai/summarizeoptions/summarylength/) { get; set; } | 允许指定摘要长度。 默认值为Medium. |

## 例子

展示如何使用 OpenAI 和 Google 模型总结文本。

```csharp
Document firstDoc = new Document(MyDir + "Big document.docx");
Document secondDoc = new Document(MyDir + "Document.docx");

string apiKey = Environment.GetEnvironmentVariable("API_KEY");
// 使用 OpenAI 或 Google 生成语言模型。
IAiModelText model = ((OpenAiModel)AiModel.Create(AiModelType.Gpt4OMini).WithApiKey(apiKey)).WithOrganization("Organization").WithProject("Project");

SummarizeOptions options = new SummarizeOptions();

options.SummaryLength = SummaryLength.Short;
Document oneDocumentSummary = model.Summarize(firstDoc, options);
oneDocumentSummary.Save(ArtifactsDir + "AI.AiSummarize.One.docx");

options.SummaryLength = SummaryLength.Long;
Document multiDocumentSummary = model.Summarize(new Document[] { firstDoc, secondDoc }, options);
multiDocumentSummary.Save(ArtifactsDir + "AI.AiSummarize.Multi.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words.AI](../../aspose.words.ai/)
* 部件 [Aspose.Words](../../)
