---
title: OpenAiModel Class
linktitle: OpenAiModel
articleTitle: OpenAiModel
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.AI.OpenAiModel – din inkörsport till sömlös integration med OpenAI:s kraftfulla språkmodeller för förbättrad dokumentbehandling.
type: docs
weight: 90
url: /sv/net/aspose.words.ai/openaimodel/
---
## OpenAiModel class

En abstrakt klass som representerar integrationen med OpenAI:s stora språkmodeller inom Aspose.Words.

```csharp
public abstract class OpenAiModel : AiModel, IAiModelText
```

## Metoder

| namn | Beskrivning |
| --- | --- |
| [WithApiKey](../../aspose.words.ai/aimodel/withapikey/)(*string*) | Ställer in en specificerad API-nyckel för modellen. |
| [WithOrganization](../../aspose.words.ai/openaimodel/withorganization/)(*string*) | Ställer in en specificerad organisation för modellen. |
| [WithProject](../../aspose.words.ai/openaimodel/withproject/)(*string*) | Ställer in ett angivet projekt till modellen. |

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
