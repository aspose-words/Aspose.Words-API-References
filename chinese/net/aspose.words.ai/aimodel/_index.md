---
title: AiModel Class
linktitle: AiModel
articleTitle: AiModel
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.AI.AiModel 类，这是利用高级生成语言模型增强文本生成和自动化的关键。
type: docs
weight: 20
url: /zh/net/aspose.words.ai/aimodel/
---
## AiModel class

表示有关生成语言模型的信息。

```csharp
public abstract class AiModel
```

## 方法

| 姓名 | 描述 |
| --- | --- |
| static [Create](../../aspose.words.ai/aimodel/create/)(*[AiModelType](../aimodeltype/)*) | 创建一个新的实例`AiModel`类. |
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

* 命名空间 [Aspose.Words.AI](../../aspose.words.ai/)
* 部件 [Aspose.Words](../../)
