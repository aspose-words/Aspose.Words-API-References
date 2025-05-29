---
title: IAiModelText Interface
linktitle: IAiModelText
articleTitle: IAiModelText
second_title: Aspose.Words für .NET
description: Entfesseln Sie Ihr kreatives Potenzial mit Aspose.Words.AI.IAiModelText, der vielseitigen Schnittstelle für KI-Modelle, die mühelos vielfältige, hochwertige Textinhalte generieren.
type: docs
weight: 70
url: /de/net/aspose.words.ai/iaimodeltext/
---
## IAiModelText interface

Die gemeinsame Schnittstelle für KI-Modelle zur Generierung einer Vielzahl textbasierter Inhalte.

```csharp
public interface IAiModelText
```

## Methoden

| Name | Beschreibung |
| --- | --- |
| [CheckGrammar](../../aspose.words.ai/iaimodeltext/checkgrammar/)(*[Document](../../aspose.words/document/), [CheckGrammarOptions](../checkgrammaroptions/)*) | Überprüft die Grammatik des bereitgestellten Dokuments. Dieser Vorgang nutzt das verbundene KI-Modell zur Überprüfung der Grammatik des Dokuments. |
| [Summarize](../../aspose.words.ai/iaimodeltext/summarize/#summarize)(*[Document](../../aspose.words/document/), [SummarizeOptions](../summarizeoptions/)*) | Generiert eine Zusammenfassung des angegebenen Dokuments mit Optionen zum Anpassen der Länge der Zusammenfassung. Dieser Vorgang nutzt das verbundene KI-Modell zur Inhaltsverarbeitung. |
| [Summarize](../../aspose.words.ai/iaimodeltext/summarize/#summarize_1)(*Document[], [SummarizeOptions](../summarizeoptions/)*) | Generiert Zusammenfassungen für ein Array von Dokumenten, mit Optionen zur Steuerung der Zusammenfassungslänge und anderer Einstellungen. Diese Methode nutzt das verbundene KI-Modell zur Verarbeitung jedes Dokuments im Array. |
| [Translate](../../aspose.words.ai/iaimodeltext/translate/)(*[Document](../../aspose.words/document/), [Language](../language/)*) | Übersetzt das bereitgestellte Dokument in die angegebene Zielsprache. Dieser Vorgang nutzt das verbundene KI-Modell zur Inhaltsübersetzung. |

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
