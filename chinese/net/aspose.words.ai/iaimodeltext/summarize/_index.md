---
title: IAiModelText.Summarize
linktitle: Summarize
articleTitle: Summarize
second_title: Aspose.Words for .NET
description: 使用 IAiModelText 轻松摘要文档。使用高级 AI 自定义摘要长度，实现精准内容提取并增强可读性。
type: docs
weight: 20
url: /zh/net/aspose.words.ai/iaimodeltext/summarize/
---
## Summarize(*[Document](../../../aspose.words/document/), [SummarizeOptions](../../summarizeoptions/)*) {#summarize}

生成指定文档的摘要，并提供调整摘要长度的选项。 此操作利用连接的 AI 模型进行内容处理。

```csharp
public Document Summarize(Document sourceDocument, SummarizeOptions options = null)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| sourceDocument | Document | 需要总结的文件。 |
| options | SummarizeOptions | 可选设置来控制摘要长度和其他参数。 |

### 返回值

该文件内容的摘要版本。

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

* class [Document](../../../aspose.words/document/)
* class [SummarizeOptions](../../summarizeoptions/)
* interface [IAiModelText](../)
* 命名空间 [Aspose.Words.AI](../../../aspose.words.ai/)
* 部件 [Aspose.Words](../../../)

---

## Summarize(*Document[], [SummarizeOptions](../../summarizeoptions/)*) {#summarize_1}

为文档数组生成摘要，并提供控制摘要长度和其他设置的选项。 此方法利用连接的 AI 模型来处理数组中的每个文档。

```csharp
public Document Summarize(Document[] sourceDocuments, SummarizeOptions options = null)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| sourceDocuments | Document[] | 需要汇总的一系列文档。 |
| options | SummarizeOptions | 控制摘要长度和其他参数的可选设置 |

### 返回值

该文件内容的摘要版本。

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

* class [Document](../../../aspose.words/document/)
* class [SummarizeOptions](../../summarizeoptions/)
* interface [IAiModelText](../)
* 命名空间 [Aspose.Words.AI](../../../aspose.words.ai/)
* 部件 [Aspose.Words](../../../)
