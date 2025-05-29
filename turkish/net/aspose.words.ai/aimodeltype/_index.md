---
title: AiModelType Enum
linktitle: AiModelType
articleTitle: AiModelType
second_title: .NET için Aspose.Words
description: Belge işleme süreçlerinde AI modellerinin kusursuz entegrasyonunu sağlamak, verimliliği ve üretkenliği artırmak için Aspose.Words.AI.AiModelType enum'unu keşfedin.
type: docs
weight: 30
url: /tr/net/aspose.words.ai/aimodeltype/
---
## AiModelType enumeration

Türleri temsil eder[`AiModel`](../aimodel/) belge işleme iş akışına entegre edilebilir.

```csharp
public enum AiModelType
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Gpt4O | `0` | GPT-4o üretken model türü. |
| Gpt4OMini | `1` | GPT-4o mini üretken model türü. |
| Gpt4Turbo | `2` | GPT-4 Turbo üretken model türü. |
| Gpt35Turbo | `3` | GPT-3.5 Turbo üretken model türü. |
| Gemini15Flash | `4` | Gemini 1.5 Flash üretken model türü. |
| Gemini15Flash8B | `5` | Gemini 1.5 Flash-8B üretken model türü. |
| Gemini15Pro | `6` | Gemini 1.5 Pro üretken model türü. |
| Claude35Sonnet | `7` | Claude 3.5 Sone üretken model türü. |
| Claude35Haiku | `8` | Claude 3.5 Haiku üretken model türü. |
| Claude3Opus | `9` | Claude 3 Opus üretken model türü. |
| Claude3Sonnet | `10` | Claude 3 Sone üretken model türü. |
| Claude3Haiku | `11` | Claude 3 Haiku üretken model türü. |

## Notlar

Bu sayım, özetleme, çeviri ve içerik oluşturma gibi görevler için hangi büyük dil modelinin (LLM) kullanılacağını tanımlamak için kullanılır.

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
