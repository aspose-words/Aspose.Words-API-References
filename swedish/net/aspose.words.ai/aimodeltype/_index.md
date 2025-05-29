---
title: AiModelType Enum
linktitle: AiModelType
articleTitle: AiModelType
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.AI.AiModelType-enum för sömlös integration av AI-modeller i dokumentbehandling, vilket förbättrar effektiviteten och produktiviteten.
type: docs
weight: 30
url: /sv/net/aspose.words.ai/aimodeltype/
---
## AiModelType enumeration

Representerar typerna av[`AiModel`](../aimodel/) som kan integreras i dokumentbehandlingens arbetsflöde.

```csharp
public enum AiModelType
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Gpt4O | `0` | GPT-4o generativ modelltyp. |
| Gpt4OMini | `1` | GPT-4o mini generativ modelltyp. |
| Gpt4Turbo | `2` | GPT-4 Turbo generativ modelltyp. |
| Gpt35Turbo | `3` | GPT-3.5 Turbo generativ modelltyp. |
| Gemini15Flash | `4` | Gemini 1.5 Flash generativ modelltyp. |
| Gemini15Flash8B | `5` | Gemini 1.5 Flash-8B generativ modelltyp. |
| Gemini15Pro | `6` | Gemini 1.5 Pro generativ modelltyp. |
| Claude35Sonnet | `7` | Claude 3.5 Sonnet generativ modelltyp. |
| Claude35Haiku | `8` | Claude 3.5 Generativ modelltyp för Haiku. |
| Claude3Opus | `9` | Claude 3 Opus generativ modelltyp. |
| Claude3Sonnet | `10` | Claude 3 Sonnet generativ modelltyp. |
| Claude3Haiku | `11` | Claude 3 Haiku generativ modelltyp. |

## Anmärkningar

Denna uppräkning används för att definiera vilken stor språkmodell (LLM) som ska användas för uppgifter såsom sammanfattning, översättning och innehållsgenerering.

## Exempel

Visar hur man sammanfattar text med hjälp av OpenAI och Google-modeller.

```csharp
Document firstDoc = new Document(MyDir + "Big document.docx");
Document secondDoc = new Document(MyDir + "Document.docx");

string apiKey = Environment.GetEnvironmentVariable("API_KEY");
// Använd OpenAI eller Googles generativa språkmodeller.
IAiModelText model = ((OpenAiModel)AiModel.Create(AiModelType.Gpt4OMini).WithApiKey(apiKey)).WithOrganization("Organization").WithProject("Project");

SummarizeOptions options = new SummarizeOptions();

options.SummaryLength = SummaryLength.Short;
Document oneDocumentSummary = model.Summarize(firstDoc, options);
oneDocumentSummary.Save(ArtifactsDir + "AI.AiSummarize.One.docx");

options.SummaryLength = SummaryLength.Long;
Document multiDocumentSummary = model.Summarize(new Document[] { firstDoc, secondDoc }, options);
multiDocumentSummary.Save(ArtifactsDir + "AI.AiSummarize.Multi.docx");
```

### Se även

* namnutrymme [Aspose.Words.AI](../../aspose.words.ai/)
* hopsättning [Aspose.Words](../../)
