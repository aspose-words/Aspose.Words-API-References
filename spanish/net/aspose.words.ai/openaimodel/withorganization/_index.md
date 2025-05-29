---
title: OpenAiModel.WithOrganization
linktitle: WithOrganization
articleTitle: WithOrganization
second_title: Aspose.Words para .NET
description: Descubra cómo el método OpenAiModel WithOrganization mejora su experiencia de IA al configurar fácilmente su organización para un rendimiento optimizado.
type: docs
weight: 10
url: /es/net/aspose.words.ai/openaimodel/withorganization/
---
## OpenAiModel.WithOrganization method

Establece una organización específica para el modelo.

```csharp
public OpenAiModel WithOrganization(string organizationId)
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
