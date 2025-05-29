---
title: AiModelType Enum
linktitle: AiModelType
articleTitle: AiModelType
second_title: Aspose.Words für .NET
description: Entdecken Sie Aspose.Words.AI.AiModelType-Enumeration für die nahtlose Integration von KI-Modellen in die Dokumentenverarbeitung und steigern Sie so Effizienz und Produktivität.
type: docs
weight: 30
url: /de/net/aspose.words.ai/aimodeltype/
---
## AiModelType enumeration

Stellt die Typen von[`AiModel`](../aimodel/) die in den Workflow der Dokumentenverarbeitung integriert werden können.

```csharp
public enum AiModelType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Gpt4O | `0` | GPT-4o generativer Modelltyp. |
| Gpt4OMini | `1` | GPT-4o Mini-generativer Modelltyp. |
| Gpt4Turbo | `2` | GPT-4 Turbo generativer Modelltyp. |
| Gpt35Turbo | `3` | GPT-3.5 Turbo-generativer Modelltyp. |
| Gemini15Flash | `4` | Gemini 1.5 Flash generativer Modelltyp. |
| Gemini15Flash8B | `5` | Gemini 1.5 Flash-8B generativer Modelltyp. |
| Gemini15Pro | `6` | Gemini 1.5 Pro generativer Modelltyp. |
| Claude35Sonnet | `7` | Claude 3.5 Sonnet, generativer Modelltyp. |
| Claude35Haiku | `8` | Claude 3.5 Haiku generativer Modelltyp. |
| Claude3Opus | `9` | Claude 3 Opus generativer Modelltyp. |
| Claude3Sonnet | `10` | Claude 3 Sonett, generativer Modelltyp. |
| Claude3Haiku | `11` | Claude 3 Haiku generativer Modelltyp. |

## Bemerkungen

Diese Aufzählung wird verwendet, um zu definieren, welches große Sprachmodell (LLM) für Aufgaben wie Zusammenfassung, Übersetzung und Inhaltsgenerierung verwendet werden soll.

## Beispiele

Zeigt, wie Text mithilfe von OpenAI- und Google-Modellen zusammengefasst wird.

```csharp
Document firstDoc = new Document(MyDir + "Big document.docx");
Document secondDoc = new Document(MyDir + "Document.docx");

string apiKey = Environment.GetEnvironmentVariable("API_KEY");
// Verwenden Sie generative Sprachmodelle von OpenAI oder Google.
IAiModelText model = ((OpenAiModel)AiModel.Create(AiModelType.Gpt4OMini).WithApiKey(apiKey)).WithOrganization("Organization").WithProject("Project");

SummarizeOptions options = new SummarizeOptions();

options.SummaryLength = SummaryLength.Short;
Document oneDocumentSummary = model.Summarize(firstDoc, options);
oneDocumentSummary.Save(ArtifactsDir + "AI.AiSummarize.One.docx");

options.SummaryLength = SummaryLength.Long;
Document multiDocumentSummary = model.Summarize(new Document[] { firstDoc, secondDoc }, options);
multiDocumentSummary.Save(ArtifactsDir + "AI.AiSummarize.Multi.docx");
```

### Siehe auch

* namensraum [Aspose.Words.AI](../../aspose.words.ai/)
* Montage [Aspose.Words](../../)
