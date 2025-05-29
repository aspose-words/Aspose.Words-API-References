---
title: AiModel Class
linktitle: AiModel
articleTitle: AiModel
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.AI.AiModel, Ihren Schlüssel zur Nutzung fortschrittlicher generativer Sprachmodelle für eine verbesserte Textgenerierung und -automatisierung.
type: docs
weight: 20
url: /de/net/aspose.words.ai/aimodel/
---
## AiModel class

Stellt Informationen zu einem generativen Sprachmodell dar.

```csharp
public abstract class AiModel
```

## Methoden

| Name | Beschreibung |
| --- | --- |
| static [Create](../../aspose.words.ai/aimodel/create/)(*[AiModelType](../aimodeltype/)*) | Erstellt eine neue Instanz von`AiModel` Klasse. |
| [WithApiKey](../../aspose.words.ai/aimodel/withapikey/)(*string*) | Legt einen angegebenen API-Schlüssel für das Modell fest. |

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
