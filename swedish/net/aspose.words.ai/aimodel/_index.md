---
title: AiModel Class
linktitle: AiModel
articleTitle: AiModel
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.AI.AiModel, din nyckel till att utnyttja avancerade generativa språkmodeller för förbättrad textgenerering och automatisering.
type: docs
weight: 20
url: /sv/net/aspose.words.ai/aimodel/
---
## AiModel class

Representerar information om en generativ språkmodell.

```csharp
public abstract class AiModel
```

## Metoder

| namn | Beskrivning |
| --- | --- |
| static [Create](../../aspose.words.ai/aimodel/create/)(*[AiModelType](../aimodeltype/)*) | Skapar en ny instans av`AiModel` klass. |
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

* namnutrymme [Aspose.Words.AI](../../aspose.words.ai/)
* hopsättning [Aspose.Words](../../)
