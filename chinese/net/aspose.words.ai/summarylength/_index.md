---
title: SummaryLength Enum
linktitle: SummaryLength
articleTitle: SummaryLength
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.AI.SummaryLength 枚举，提供灵活的摘要长度选项，以增强文档摘要并提高内容清晰度。
type: docs
weight: 110
url: /zh/net/aspose.words.ai/summarylength/
---
## SummaryLength enumeration

枚举摘要的可能长度。

```csharp
public enum SummaryLength
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| VeryShort | `0` | 尝试生成 1-2 个句子。 |
| Short | `1` | 尝试生成 3-4 个句子。 |
| Medium | `2` | 尝试生成 5-6 个句子。 |
| Long | `3` | 尝试生成 7-10 个句子。 |
| VeryLong | `4` | 尝试生成 11-20 个句子。 |

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
