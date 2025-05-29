---
title: SummarizeOptions Class
linktitle: SummarizeOptions
articleTitle: SummarizeOptions
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.AI.SummarizeOptions, um Ihre Dokumentzusammenfassung anzupassen und zu verbessern, um klarere Erkenntnisse und ein verbessertes Inhaltsmanagement zu erzielen.
type: docs
weight: 100
url: /de/net/aspose.words.ai/summarizeoptions/
---
## SummarizeOptions class

Ermöglicht die Angabe verschiedener Optionen zum Zusammenfassen von Dokumentinhalten.

```csharp
public class SummarizeOptions
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [SummarizeOptions](summarizeoptions/)() | Initialisiert eine neue Instanz von`SummarizeOptions` Klasse. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [SummaryLength](../../aspose.words.ai/summarizeoptions/summarylength/) { get; set; } | Ermöglicht die Angabe der Zusammenfassungslänge. Der Standardwert istMedium . |

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
