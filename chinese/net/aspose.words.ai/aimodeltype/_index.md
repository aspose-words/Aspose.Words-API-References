---
title: AiModelType Enum
linktitle: AiModelType
articleTitle: AiModelType
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.AI.AiModelType 枚举，以便在文档处理中无缝集成 AI 模型，提高效率和生产力。
type: docs
weight: 30
url: /zh/net/aspose.words.ai/aimodeltype/
---
## AiModelType enumeration

代表[`AiModel`](../aimodel/)可以集成到文档处理工作流程中。

```csharp
public enum AiModelType
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Gpt4O | `0` | GPT-4o 生成模型类型. |
| Gpt4OMini | `1` | GPT-4o mini 生成模型类型。 |
| Gpt4Turbo | `2` | GPT-4 Turbo 生成模型类型。 |
| Gpt35Turbo | `3` | GPT-3.5 Turbo 生成模型类型。 |
| Gemini15Flash | `4` | Gemini 1.5 Flash 生成模型类型。 |
| Gemini15Flash8B | `5` | Gemini 1.5 Flash-8B 生成模型类型。 |
| Gemini15Pro | `6` | Gemini 1.5 Pro 生成模型类型。 |
| Claude35Sonnet | `7` | Claude 3.5 Sonnet 生成模型类型。 |
| Claude35Haiku | `8` | Claude 3.5 Haiku 生成模型类型。 |
| Claude3Opus | `9` | Claude 3 Opus 生成模型类型。 |
| Claude3Sonnet | `10` | Claude 3 Sonnet 生成模型类型。 |
| Claude3Haiku | `11` | Claude 3 Haiku 生成模型类型。 |

## 评论

此枚举用于定义应使用哪种大型语言模型 (LLM) 来完成摘要、翻译和内容生成等任务。

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
