---
title: GoogleAiModel Class
linktitle: GoogleAiModel
articleTitle: GoogleAiModel
second_title: Aspose.Words für .NET
description: Nutzen Sie die Leistungsfähigkeit der Klasse Aspose.Words.AI.GoogleAiModel, um Google AI-Modelle nahtlos zu integrieren und Ihre Dokumentverarbeitungsfunktionen mühelos zu verbessern.
type: docs
weight: 60
url: /de/net/aspose.words.ai/googleaimodel/
---
## GoogleAiModel class

Eine abstrakte Klasse, die die Integration mit den KI-Modellen von Google innerhalb von Aspose.Words darstellt.

```csharp
public abstract class GoogleAiModel : AiModel, IAiModelText
```

## Methoden

| Name | Beschreibung |
| --- | --- |
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

* class [AiModel](../aimodel/)
* interface [IAiModelText](../iaimodeltext/)
* namensraum [Aspose.Words.AI](../../aspose.words.ai/)
* Montage [Aspose.Words](../../)
