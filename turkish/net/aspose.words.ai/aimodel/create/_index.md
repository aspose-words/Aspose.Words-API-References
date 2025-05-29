---
title: AiModel.Create
linktitle: Create
articleTitle: Create
second_title: .NET için Aspose.Words
description: Yeni AiModel sınıf örneklerini zahmetsizce oluşturmak ve AI geliştirmenizi kolaylaştırılmış verimlilikle geliştirmek için AiModel Create yöntemini keşfedin.
type: docs
weight: 10
url: /tr/net/aspose.words.ai/aimodel/create/
---
## AiModel.Create method

Yeni bir örnek oluşturur[`AiModel`](../) sınıf.

```csharp
public static AiModel Create(AiModelType modelType)
```

## Örnekler

OpenAI ve Google modelleri kullanılarak metnin nasıl özetleneceğini gösterir.

```csharp
Document firstDoc = new Document(MyDir + "Big document.docx");
Document secondDoc = new Document(MyDir + "Document.docx");

string apiKey = Environment.GetEnvironmentVariable("API_KEY");
// OpenAI veya Google üretici dil modellerini kullanın.
IAiModelText model = ((OpenAiModel)AiModel.Create(AiModelType.Gpt4OMini).WithApiKey(apiKey)).WithOrganization("Organization").WithProject("Project");

SummarizeOptions options = new SummarizeOptions();

options.SummaryLength = SummaryLength.Short;
Document oneDocumentSummary = model.Summarize(firstDoc, options);
oneDocumentSummary.Save(ArtifactsDir + "AI.AiSummarize.One.docx");

options.SummaryLength = SummaryLength.Long;
Document multiDocumentSummary = model.Summarize(new Document[] { firstDoc, secondDoc }, options);
multiDocumentSummary.Save(ArtifactsDir + "AI.AiSummarize.Multi.docx");
```

### Ayrıca bakınız

* enum [AiModelType](../../aimodeltype/)
* class [AiModel](../)
* ad alanı [Aspose.Words.AI](../../../aspose.words.ai/)
* toplantı [Aspose.Words](../../../)
