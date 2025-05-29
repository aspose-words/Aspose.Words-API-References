---
title: OpenAiModel.WithOrganization
linktitle: WithOrganization
articleTitle: WithOrganization
second_title: .NET için Aspose.Words
description: OpenAiModel WithOrganization yönteminin, kuruluşunuzu optimize edilmiş performans için kolayca ayarlayarak yapay zeka deneyiminizi nasıl geliştirdiğini keşfedin.
type: docs
weight: 10
url: /tr/net/aspose.words.ai/openaimodel/withorganization/
---
## OpenAiModel.WithOrganization method

Modele belirli bir Organizasyon ayarlar.

```csharp
public OpenAiModel WithOrganization(string organizationId)
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

* class [OpenAiModel](../)
* ad alanı [Aspose.Words.AI](../../../aspose.words.ai/)
* toplantı [Aspose.Words](../../../)
