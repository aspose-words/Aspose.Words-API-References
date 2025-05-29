---
title: IAiModelText.Summarize
linktitle: Summarize
articleTitle: Summarize
second_title: Aspose.Words für .NET
description: Fassen Sie Dokumente mühelos mit IAiModelText zusammen. Passen Sie die Länge der Zusammenfassung mithilfe fortschrittlicher KI an, um Inhalte präzise zu extrahieren und die Lesbarkeit zu verbessern.
type: docs
weight: 20
url: /de/net/aspose.words.ai/iaimodeltext/summarize/
---
## Summarize(*[Document](../../../aspose.words/document/), [SummarizeOptions](../../summarizeoptions/)*) {#summarize}

Generiert eine Zusammenfassung des angegebenen Dokuments mit Optionen zum Anpassen der Länge der Zusammenfassung. Dieser Vorgang nutzt das verbundene KI-Modell zur Inhaltsverarbeitung.

```csharp
public Document Summarize(Document sourceDocument, SummarizeOptions options = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| sourceDocument | Document | Das zusammenzufassende Dokument. |
| options | SummarizeOptions | Optionale Einstellungen zur Steuerung der Zusammenfassungslänge und anderer Parameter. |

### Rückgabewert

Eine zusammengefasste Version des Dokumentinhalts.

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

* class [Document](../../../aspose.words/document/)
* class [SummarizeOptions](../../summarizeoptions/)
* interface [IAiModelText](../)
* namensraum [Aspose.Words.AI](../../../aspose.words.ai/)
* Montage [Aspose.Words](../../../)

---

## Summarize(*Document[], [SummarizeOptions](../../summarizeoptions/)*) {#summarize_1}

Generiert Zusammenfassungen für ein Array von Dokumenten, mit Optionen zur Steuerung der Zusammenfassungslänge und anderer Einstellungen. Diese Methode nutzt das verbundene KI-Modell zur Verarbeitung jedes Dokuments im Array.

```csharp
public Document Summarize(Document[] sourceDocuments, SummarizeOptions options = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| sourceDocuments | Document[] | Ein Array von Dokumenten, die zusammengefasst werden sollen. |
| options | SummarizeOptions | Optionale Einstellungen zur Steuerung der Zusammenfassungslänge und anderer Parameter |

### Rückgabewert

Eine zusammengefasste Version des Dokumentinhalts.

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

* class [Document](../../../aspose.words/document/)
* class [SummarizeOptions](../../summarizeoptions/)
* interface [IAiModelText](../)
* namensraum [Aspose.Words.AI](../../../aspose.words.ai/)
* Montage [Aspose.Words](../../../)
