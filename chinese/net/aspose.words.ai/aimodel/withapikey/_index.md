---
title: AiModel.WithApiKey
linktitle: WithApiKey
articleTitle: WithApiKey
second_title: Aspose.Words for .NET
description: 使用 WithApiKey 方法解锁 AiModel 的强大功能。轻松设置 API 密钥，增强功能并实现无缝集成。
type: docs
weight: 20
url: /zh/net/aspose.words.ai/aimodel/withapikey/
---
## AiModel.WithApiKey method

将指定的 API 密钥设置为模型。

```csharp
public AiModel WithApiKey(string apiKey)
```

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

* class [AiModel](../)
* 命名空间 [Aspose.Words.AI](../../../aspose.words.ai/)
* 部件 [Aspose.Words](../../../)
