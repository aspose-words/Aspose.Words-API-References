---
title: AiModel Class
linktitle: AiModel
articleTitle: AiModel
second_title: .NET için Aspose.Words
description: Gelişmiş Üretken Dil Modellerini kullanarak gelişmiş metin üretimi ve otomasyonu için anahtarınız olan Aspose.Words.AI.AiModel sınıfını keşfedin.
type: docs
weight: 20
url: /tr/net/aspose.words.ai/aimodel/
---
## AiModel class

Üretken Dil Modeli hakkında bilgi temsil eder.

```csharp
public abstract class AiModel
```

## yöntemler

| İsim | Tanım |
| --- | --- |
| static [Create](../../aspose.words.ai/aimodel/create/)(*[AiModelType](../aimodeltype/)*) | Yeni bir örnek oluşturur`AiModel` sınıf. |
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

* ad alanı [Aspose.Words.AI](../../aspose.words.ai/)
* toplantı [Aspose.Words](../../)
