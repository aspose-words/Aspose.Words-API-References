---
title: IAiModelText Interface
linktitle: IAiModelText
articleTitle: IAiModelText
second_title: Aspose.Words for .NET
description: 使用 Aspose.Words.AI.IAiModelText 释放创造潜力，它是 AI 模型的多功能界面，可轻松生成多样化、高质量的文本内容。
type: docs
weight: 70
url: /zh/net/aspose.words.ai/iaimodeltext/
---
## IAiModelText interface

旨在生成各种基于文本的内容的 AI 模型的通用接口。

```csharp
public interface IAiModelText
```

## 方法

| 姓名 | 描述 |
| --- | --- |
| [CheckGrammar](../../aspose.words.ai/iaimodeltext/checkgrammar/)(*[Document](../../aspose.words/document/), [CheckGrammarOptions](../checkgrammaroptions/)*) | 检查所提供文档的语法。 此操作利用连接的 AI 模型来检查文档的语法。 |
| [Summarize](../../aspose.words.ai/iaimodeltext/summarize/#summarize)(*[Document](../../aspose.words/document/), [SummarizeOptions](../summarizeoptions/)*) | 生成指定文档的摘要，并提供调整摘要长度的选项。 此操作利用连接的 AI 模型进行内容处理。 |
| [Summarize](../../aspose.words.ai/iaimodeltext/summarize/#summarize_1)(*Document[], [SummarizeOptions](../summarizeoptions/)*) | 为文档数组生成摘要，并提供控制摘要长度和其他设置的选项。 此方法利用连接的 AI 模型来处理数组中的每个文档。 |
| [Translate](../../aspose.words.ai/iaimodeltext/translate/)(*[Document](../../aspose.words/document/), [Language](../language/)*) | 将提供的文档翻译成指定的目标语言。 此操作利用连接的 AI 模型进行内容翻译。 |

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
