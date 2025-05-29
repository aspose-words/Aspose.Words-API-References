---
title: SummarizeOptions Class
linktitle: SummarizeOptions
articleTitle: SummarizeOptions
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.AI.SummarizeOptions för att anpassa och förbättra din dokumentsammanfattning för tydligare insikter och förbättrad innehållshantering.
type: docs
weight: 100
url: /sv/net/aspose.words.ai/summarizeoptions/
---
## SummarizeOptions class

Gör det möjligt att ange olika alternativ för att sammanfatta dokumentinnehåll.

```csharp
public class SummarizeOptions
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [SummarizeOptions](summarizeoptions/)() | Initierar en ny instans av`SummarizeOptions` klass. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [SummaryLength](../../aspose.words.ai/summarizeoptions/summarylength/) { get; set; } | Gör det möjligt att ange sammanfattningens längd. Standardvärdet ärMedium . |

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
