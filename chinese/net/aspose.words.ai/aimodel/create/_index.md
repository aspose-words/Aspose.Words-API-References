---
title: AiModel.Create
linktitle: Create
articleTitle: Create
second_title: Aspose.Words for .NET
description: 探索 AiModel Create 方法，轻松生成新的 AiModel 类实例，以简化的效率增强您的 AI 开发。
type: docs
weight: 10
url: /zh/net/aspose.words.ai/aimodel/create/
---
## AiModel.Create method

创建一个新的实例[`AiModel`](../)类.

```csharp
public static AiModel Create(AiModelType modelType)
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

* enum [AiModelType](../../aimodeltype/)
* class [AiModel](../)
* 命名空间 [Aspose.Words.AI](../../../aspose.words.ai/)
* 部件 [Aspose.Words](../../../)
