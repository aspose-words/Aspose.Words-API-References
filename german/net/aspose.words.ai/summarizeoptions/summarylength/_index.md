---
title: SummarizeOptions.SummaryLength
linktitle: SummaryLength
articleTitle: SummaryLength
second_title: Aspose.Words für .NET
description: Steuern Sie die Länge Ihrer Zusammenfassung mit der Eigenschaft „SummarizeOptions SummaryLength“. Passen Sie Ihren Inhalt für mehr Klarheit und Wirkung an. Die Standardeinstellung ist „Mittel“.
type: docs
weight: 20
url: /de/net/aspose.words.ai/summarizeoptions/summarylength/
---
## SummarizeOptions.SummaryLength property

Ermöglicht die Angabe der Zusammenfassungslänge. Der Standardwert istMedium .

```csharp
public SummaryLength SummaryLength { get; set; }
```

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

* enum [SummaryLength](../../summarylength/)
* class [SummarizeOptions](../)
* namensraum [Aspose.Words.AI](../../../aspose.words.ai/)
* Montage [Aspose.Words](../../../)
