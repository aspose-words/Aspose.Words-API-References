---
title: SummaryLength Enum
linktitle: SummaryLength
articleTitle: SummaryLength
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aufzählung Aspose.Words.AI.SummaryLength, die flexible Optionen für die Zusammenfassungslänge für eine verbesserte Dokumentzusammenfassung und verbesserte Inhaltsübersichtlichkeit bietet.
type: docs
weight: 110
url: /de/net/aspose.words.ai/summarylength/
---
## SummaryLength enumeration

Listet mögliche Längen der Zusammenfassung auf.

```csharp
public enum SummaryLength
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| VeryShort | `0` | Versuchen Sie, 1-2 Sätze zu bilden. |
| Short | `1` | Versuchen Sie, 3-4 Sätze zu bilden. |
| Medium | `2` | Versuchen Sie, 5-6 Sätze zu bilden. |
| Long | `3` | Versuchen Sie, 7-10 Sätze zu bilden. |
| VeryLong | `4` | Versuchen Sie, 11–20 Sätze zu bilden. |

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
