---
title: SummaryLength Enum
linktitle: SummaryLength
articleTitle: SummaryLength
second_title: Aspose.Words för .NET
description: Upptäck enumerationen Aspose.Words.AI.SummaryLength, som erbjuder flexibla alternativ för sammanfattningslängd för förbättrad dokumentsammanfattning och förbättrad innehållstydlighet.
type: docs
weight: 110
url: /sv/net/aspose.words.ai/summarylength/
---
## SummaryLength enumeration

Räknar upp möjliga längder på sammanfattningen.

```csharp
public enum SummaryLength
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| VeryShort | `0` | Försök att generera 1-2 meningar. |
| Short | `1` | Försök att skapa 3–4 meningar. |
| Medium | `2` | Försök att skapa 5–6 meningar. |
| Long | `3` | Försök att generera 7–10 meningar. |
| VeryLong | `4` | Försök att generera 11–20 meningar. |

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
