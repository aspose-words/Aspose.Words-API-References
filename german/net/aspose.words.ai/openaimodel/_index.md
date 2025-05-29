---
title: OpenAiModel Class
linktitle: OpenAiModel
articleTitle: OpenAiModel
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.AI.OpenAiModel – Ihr Tor zur nahtlosen Integration mit den leistungsstarken Sprachmodellen von OpenAI für eine verbesserte Dokumentverarbeitung.
type: docs
weight: 90
url: /de/net/aspose.words.ai/openaimodel/
---
## OpenAiModel class

Eine abstrakte Klasse, die die Integration mit den großen Sprachmodellen von OpenAI innerhalb von Aspose.Words darstellt.

```csharp
public abstract class OpenAiModel : AiModel, IAiModelText
```

## Methoden

| Name | Beschreibung |
| --- | --- |
| [WithApiKey](../../aspose.words.ai/aimodel/withapikey/)(*string*) | Legt einen angegebenen API-Schlüssel für das Modell fest. |
| [WithOrganization](../../aspose.words.ai/openaimodel/withorganization/)(*string*) | Legt eine angegebene Organisation für das Modell fest. |
| [WithProject](../../aspose.words.ai/openaimodel/withproject/)(*string*) | Legt ein angegebenes Projekt für das Modell fest. |

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
