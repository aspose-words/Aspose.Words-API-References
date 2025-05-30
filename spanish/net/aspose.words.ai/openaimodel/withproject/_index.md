---
title: OpenAiModel.WithProject
linktitle: WithProject
articleTitle: WithProject
second_title: Aspose.Words para .NET
description: Mejore sus capacidades de IA con el método WithProject de OpenAiModel asigne proyectos fácilmente para optimizar el rendimiento y agilizar su flujo de trabajo.
type: docs
weight: 20
url: /es/net/aspose.words.ai/openaimodel/withproject/
---
## OpenAiModel.WithProject method

Establece un proyecto específico para el modelo.

```csharp
public OpenAiModel WithProject(string projectId)
```

## Ejemplos

Muestra cómo resumir texto utilizando OpenAI y modelos de Google.

```csharp
Document firstDoc = new Document(MyDir + "Big document.docx");
Document secondDoc = new Document(MyDir + "Document.docx");

string apiKey = Environment.GetEnvironmentVariable("API_KEY");
// Utilice modelos de lenguaje generativo de OpenAI o Google.
IAiModelText model = ((OpenAiModel)AiModel.Create(AiModelType.Gpt4OMini).WithApiKey(apiKey)).WithOrganization("Organization").WithProject("Project");

SummarizeOptions options = new SummarizeOptions();

options.SummaryLength = SummaryLength.Short;
Document oneDocumentSummary = model.Summarize(firstDoc, options);
oneDocumentSummary.Save(ArtifactsDir + "AI.AiSummarize.One.docx");

options.SummaryLength = SummaryLength.Long;
Document multiDocumentSummary = model.Summarize(new Document[] { firstDoc, secondDoc }, options);
multiDocumentSummary.Save(ArtifactsDir + "AI.AiSummarize.Multi.docx");
```

### Ver también

* class [OpenAiModel](../)
* espacio de nombres [Aspose.Words.AI](../../../aspose.words.ai/)
* asamblea [Aspose.Words](../../../)
