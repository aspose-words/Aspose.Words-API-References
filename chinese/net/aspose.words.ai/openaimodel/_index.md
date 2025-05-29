---
title: OpenAiModel Class
linktitle: OpenAiModel
articleTitle: OpenAiModel
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.AI.OpenAiModel 类——与 OpenAI 强大的语言模型无缝集成以增强文档处理的门户。
type: docs
weight: 90
url: /zh/net/aspose.words.ai/openaimodel/
---
## OpenAiModel class

一个抽象类，表示与 Aspose.Words 中的 OpenAI 大型语言模型的集成。

```csharp
public abstract class OpenAiModel : AiModel, IAiModelText
```

## 方法

| 姓名 | 描述 |
| --- | --- |
| [WithApiKey](../../aspose.words.ai/aimodel/withapikey/)(*string*) | 将指定的 API 密钥设置为模型。 |
| [WithOrganization](../../aspose.words.ai/openaimodel/withorganization/)(*string*) | 将指定的组织设置为模型。 |
| [WithProject](../../aspose.words.ai/openaimodel/withproject/)(*string*) | 将指定的项目设置为模型。 |

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
