---
title: OpenAiModel.WithProject
linktitle: WithProject
articleTitle: WithProject
second_title: Aspose.Words für .NET
description: Verbessern Sie Ihre KI-Fähigkeiten mit der WithProject-Methode von OpenAiModel – weisen Sie Projekte einfach zu, um die Leistung zu optimieren und Ihren Arbeitsablauf zu rationalisieren.
type: docs
weight: 20
url: /de/net/aspose.words.ai/openaimodel/withproject/
---
## OpenAiModel.WithProject method

Legt ein angegebenes Projekt für das Modell fest.

```csharp
public OpenAiModel WithProject(string projectId)
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

* class [OpenAiModel](../)
* namensraum [Aspose.Words.AI](../../../aspose.words.ai/)
* Montage [Aspose.Words](../../../)
