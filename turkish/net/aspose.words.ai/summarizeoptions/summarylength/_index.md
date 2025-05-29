---
title: SummarizeOptions.SummaryLength
linktitle: SummaryLength
articleTitle: SummaryLength
second_title: .NET için Aspose.Words
description: Özetinizin uzunluğunu SummarizeOptions SummaryLength özelliğiyle kontrol edin. İçeriğinizi netlik ve etki için özelleştirin. Varsayılan Orta'dır.
type: docs
weight: 20
url: /tr/net/aspose.words.ai/summarizeoptions/summarylength/
---
## SummarizeOptions.SummaryLength property

Özet uzunluğunu belirtmeye izin verir. Varsayılan değerMedium .

```csharp
public SummaryLength SummaryLength { get; set; }
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

* enum [SummaryLength](../../summarylength/)
* class [SummarizeOptions](../)
* ad alanı [Aspose.Words.AI](../../../aspose.words.ai/)
* toplantı [Aspose.Words](../../../)
