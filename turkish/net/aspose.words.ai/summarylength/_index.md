---
title: SummaryLength Enum
linktitle: SummaryLength
articleTitle: SummaryLength
second_title: .NET için Aspose.Words
description: Gelişmiş belge özetleme ve iyileştirilmiş içerik netliği için esnek özet uzunluğu seçenekleri sunan Aspose.Words.AI.SummaryLength enum'ını keşfedin.
type: docs
weight: 110
url: /tr/net/aspose.words.ai/summarylength/
---
## SummaryLength enumeration

Özetin olası uzunluklarını sıralar.

```csharp
public enum SummaryLength
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| VeryShort | `0` | 1-2 cümle üretmeye çalışın. |
| Short | `1` | 3-4 cümle üretmeye çalışın. |
| Medium | `2` | 5-6 cümle üretmeye çalışın. |
| Long | `3` | 7-10 cümle üretmeye çalışın. |
| VeryLong | `4` | 11-20 cümle üretmeye çalışın. |

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
