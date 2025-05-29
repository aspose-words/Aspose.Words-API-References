---
title: GoogleAiModel Class
linktitle: GoogleAiModel
articleTitle: GoogleAiModel
second_title: Aspose.Words för .NET
description: Lås upp kraften i Aspose.Words.AI.GoogleAiModel-klassen för att sömlöst integrera Google AI-modeller och förbättra dina dokumentbehandlingsmöjligheter utan ansträngning.
type: docs
weight: 60
url: /sv/net/aspose.words.ai/googleaimodel/
---
## GoogleAiModel class

En abstrakt klass som representerar integrationen med Googles AI-modeller inom Aspose.Words.

```csharp
public abstract class GoogleAiModel : AiModel, IAiModelText
```

## Metoder

| namn | Beskrivning |
| --- | --- |
| [WithApiKey](../../aspose.words.ai/aimodel/withapikey/)(*string*) | Ställer in en specificerad API-nyckel för modellen. |

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

* class [AiModel](../aimodel/)
* interface [IAiModelText](../iaimodeltext/)
* namnutrymme [Aspose.Words.AI](../../aspose.words.ai/)
* hopsättning [Aspose.Words](../../)
