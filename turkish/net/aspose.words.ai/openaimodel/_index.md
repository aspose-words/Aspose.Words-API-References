---
title: OpenAiModel Class
linktitle: OpenAiModel
articleTitle: OpenAiModel
second_title: .NET için Aspose.Words
description: Gelişmiş belge işleme için OpenAI'nin güçlü dil modelleriyle kusursuz entegrasyona açılan kapınız olan Aspose.Words.AI.OpenAiModel sınıfını keşfedin.
type: docs
weight: 90
url: /tr/net/aspose.words.ai/openaimodel/
---
## OpenAiModel class

Aspose.Words içindeki OpenAI'nin büyük dil modelleriyle entegrasyonu temsil eden soyut bir sınıf.

```csharp
public abstract class OpenAiModel : AiModel, IAiModelText
```

## yöntemler

| İsim | Tanım |
| --- | --- |
| [WithApiKey](../../aspose.words.ai/aimodel/withapikey/)(*string*) | Modele belirtilen bir API anahtarı ayarlar. |
| [WithOrganization](../../aspose.words.ai/openaimodel/withorganization/)(*string*) | Modele belirli bir Organizasyon ayarlar. |
| [WithProject](../../aspose.words.ai/openaimodel/withproject/)(*string*) | Belirtilen bir Projeyi modele ayarlar. |

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
