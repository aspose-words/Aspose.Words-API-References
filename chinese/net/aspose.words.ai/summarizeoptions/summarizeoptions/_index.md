---
title: SummarizeOptions
linktitle: SummarizeOptions
articleTitle: SummarizeOptions
second_title: Aspose.Words for .NET
description: 探索 SummarizeOptions 构造函数，用于创建 SummarizeOptions 类的自定义实例，从而提高编码效率和灵活性。
type: docs
weight: 10
url: /zh/net/aspose.words.ai/summarizeoptions/summarizeoptions/
---
## SummarizeOptions constructor

初始化一个新的实例[`SummarizeOptions`](../)类.

```csharp
public SummarizeOptions()
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

* class [SummarizeOptions](../)
* 命名空间 [Aspose.Words.AI](../../../aspose.words.ai/)
* 部件 [Aspose.Words](../../../)
