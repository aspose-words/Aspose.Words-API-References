---
title: IAiModelText.Summarize
linktitle: Summarize
articleTitle: Summarize
second_title: Aspose.Words för .NET
description: Sammanfatta dokument enkelt med IAiModelText. Anpassa sammanfattningslängden med avancerad AI för exakt innehållsutvinning och förbättrad läsbarhet.
type: docs
weight: 20
url: /sv/net/aspose.words.ai/iaimodeltext/summarize/
---
## Summarize(*[Document](../../../aspose.words/document/), [SummarizeOptions](../../summarizeoptions/)*) {#summarize}

Genererar en sammanfattning av det angivna dokumentet, med alternativ för att justera sammanfattningens längd. Den här åtgärden utnyttjar den anslutna AI-modellen för innehållsbearbetning.

```csharp
public Document Summarize(Document sourceDocument, SummarizeOptions options = null)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| sourceDocument | Document | Dokumentet som ska sammanfattas. |
| options | SummarizeOptions | Valfria inställningar för att styra sammanfattningens längd och andra parametrar. |

### Returvärde

En sammanfattad version av dokumentets innehåll.

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

* class [Document](../../../aspose.words/document/)
* class [SummarizeOptions](../../summarizeoptions/)
* interface [IAiModelText](../)
* namnutrymme [Aspose.Words.AI](../../../aspose.words.ai/)
* hopsättning [Aspose.Words](../../../)

---

## Summarize(*Document[], [SummarizeOptions](../../summarizeoptions/)*) {#summarize_1}

Genererar sammanfattningar för en array av dokument, med alternativ för att kontrollera sammanfattningens längd och andra inställningar. Den här metoden använder den anslutna AI-modellen för att bearbeta varje dokument i arrayen.

```csharp
public Document Summarize(Document[] sourceDocuments, SummarizeOptions options = null)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| sourceDocuments | Document[] | En uppsättning dokument som ska sammanfattas. |
| options | SummarizeOptions | Valfria inställningar för att styra sammanfattningens längd och andra parametrar |

### Returvärde

En sammanfattad version av dokumentets innehåll.

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

* class [Document](../../../aspose.words/document/)
* class [SummarizeOptions](../../summarizeoptions/)
* interface [IAiModelText](../)
* namnutrymme [Aspose.Words.AI](../../../aspose.words.ai/)
* hopsättning [Aspose.Words](../../../)
