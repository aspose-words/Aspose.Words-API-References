---
title: AiModel.WithApiKey
linktitle: WithApiKey
articleTitle: WithApiKey
second_title: .NET için Aspose.Words
description: WithApiKey yöntemiyle AiModel'in gücünü açığa çıkarın. Gelişmiş işlevsellik ve sorunsuz entegrasyon için API anahtarınızı zahmetsizce ayarlayın.
type: docs
weight: 20
url: /tr/net/aspose.words.ai/aimodel/withapikey/
---
## AiModel.WithApiKey method

Modele belirtilen bir API anahtarı ayarlar.

```csharp
public AiModel WithApiKey(string apiKey)
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

* class [AiModel](../)
* ad alanı [Aspose.Words.AI](../../../aspose.words.ai/)
* toplantı [Aspose.Words](../../../)
