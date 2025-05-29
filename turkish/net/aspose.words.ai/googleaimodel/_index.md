---
title: GoogleAiModel Class
linktitle: GoogleAiModel
articleTitle: GoogleAiModel
second_title: .NET için Aspose.Words
description: Google AI modellerini sorunsuz bir şekilde entegre etmek ve belge işleme yeteneklerinizi zahmetsizce geliştirmek için Aspose.Words.AI.GoogleAiModel sınıfının gücünü açığa çıkarın.
type: docs
weight: 60
url: /tr/net/aspose.words.ai/googleaimodel/
---
## GoogleAiModel class

Aspose.Words içindeki Google'ın AI modelleriyle entegrasyonu temsil eden soyut bir sınıf.

```csharp
public abstract class GoogleAiModel : AiModel, IAiModelText
```

## yöntemler

| İsim | Tanım |
| --- | --- |
| [WithApiKey](../../aspose.words.ai/aimodel/withapikey/)(*string*) | Modele belirtilen bir API anahtarı ayarlar. |

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

* class [AiModel](../aimodel/)
* interface [IAiModelText](../iaimodeltext/)
* ad alanı [Aspose.Words.AI](../../aspose.words.ai/)
* toplantı [Aspose.Words](../../)
