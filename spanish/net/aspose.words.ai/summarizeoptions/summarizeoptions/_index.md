---
title: SummarizeOptions
linktitle: SummarizeOptions
articleTitle: SummarizeOptions
second_title: Aspose.Words para .NET
description: Descubra el constructor SummarizeOptions para crear instancias personalizadas de la clase SummarizeOptions, mejorando la eficiencia y flexibilidad de su codificación.
type: docs
weight: 10
url: /es/net/aspose.words.ai/summarizeoptions/summarizeoptions/
---
## SummarizeOptions constructor

Inicializa una nueva instancia de[`SummarizeOptions`](../) clase.

```csharp
public SummarizeOptions()
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

* class [SummarizeOptions](../)
* espacio de nombres [Aspose.Words.AI](../../../aspose.words.ai/)
* asamblea [Aspose.Words](../../../)
