---
title: IAiModelText Interface
linktitle: IAiModelText
articleTitle: IAiModelText
second_title: Aspose.Words för .NET
description: Frigör kreativ potential med Aspose.Words.AI.IAiModelText, det mångsidiga gränssnittet för AI-modeller som enkelt genererar varierat, högkvalitativt textinnehåll.
type: docs
weight: 70
url: /sv/net/aspose.words.ai/iaimodeltext/
---
## IAiModelText interface

Det gemensamma gränssnittet för AI-modeller utformade för att generera en mängd olika textbaserade innehåll.

```csharp
public interface IAiModelText
```

## Metoder

| namn | Beskrivning |
| --- | --- |
| [CheckGrammar](../../aspose.words.ai/iaimodeltext/checkgrammar/)(*[Document](../../aspose.words/document/), [CheckGrammarOptions](../checkgrammaroptions/)*) | Kontrollerar grammatiken i det angivna dokumentet. Den här åtgärden utnyttjar den anslutna AI-modellen för att kontrollera dokumentets grammatik. |
| [Summarize](../../aspose.words.ai/iaimodeltext/summarize/#summarize)(*[Document](../../aspose.words/document/), [SummarizeOptions](../summarizeoptions/)*) | Genererar en sammanfattning av det angivna dokumentet, med alternativ för att justera sammanfattningens längd. Den här åtgärden utnyttjar den anslutna AI-modellen för innehållsbearbetning. |
| [Summarize](../../aspose.words.ai/iaimodeltext/summarize/#summarize_1)(*Document[], [SummarizeOptions](../summarizeoptions/)*) | Genererar sammanfattningar för en array av dokument, med alternativ för att kontrollera sammanfattningens längd och andra inställningar. Den här metoden använder den anslutna AI-modellen för att bearbeta varje dokument i arrayen. |
| [Translate](../../aspose.words.ai/iaimodeltext/translate/)(*[Document](../../aspose.words/document/), [Language](../language/)*) | Översätter det angivna dokumentet till det angivna målspråket. Denna åtgärd utnyttjar den anslutna AI-modellen för innehållsöversättning. |

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
