---
title: SummarizeOptions Class
linktitle: SummarizeOptions
articleTitle: SummarizeOptions
second_title: .NET için Aspose.Words
description: Daha net içgörüler ve geliştirilmiş içerik yönetimi için belge özetlemenizi özelleştirmek ve geliştirmek amacıyla Aspose.Words.AI.SummarizeOptions sınıfını keşfedin.
type: docs
weight: 100
url: /tr/net/aspose.words.ai/summarizeoptions/
---
## SummarizeOptions class

Belge içeriğini özetlemek için çeşitli seçenekleri belirtmenize olanak tanır.

```csharp
public class SummarizeOptions
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [SummarizeOptions](summarizeoptions/)() | Yeni bir örnek başlatır`SummarizeOptions` sınıf. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [SummaryLength](../../aspose.words.ai/summarizeoptions/summarylength/) { get; set; } | Özet uzunluğunu belirtmeye izin verir. Varsayılan değerMedium . |

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
