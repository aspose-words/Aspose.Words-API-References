---
title: GoogleAiModel Class
linktitle: GoogleAiModel
articleTitle: GoogleAiModel
second_title: Aspose.Words for .NET
description: 释放 Aspose.Words.AI.GoogleAiModel 类的强大功能，无缝集成 Google AI 模型，轻松增强您的文档处理能力。
type: docs
weight: 60
url: /zh/net/aspose.words.ai/googleaimodel/
---
## GoogleAiModel class

一个抽象类，代表与 Aspose.Words 中的 Google AI 模型的集成。

```csharp
public abstract class GoogleAiModel : AiModel, IAiModelText
```

## 方法

| 姓名 | 描述 |
| --- | --- |
| [WithApiKey](../../aspose.words.ai/aimodel/withapikey/)(*string*) | 将指定的 API 密钥设置为模型。 |

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

* class [AiModel](../aimodel/)
* interface [IAiModelText](../iaimodeltext/)
* 命名空间 [Aspose.Words.AI](../../aspose.words.ai/)
* 部件 [Aspose.Words](../../)
