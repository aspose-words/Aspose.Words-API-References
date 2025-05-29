---
title: AiModel.Create
linktitle: Create
articleTitle: Create
second_title: Aspose.Words para .NET
description: Descubra el método AiModel Create para generar fácilmente nuevas instancias de clase AiModel y mejorar su desarrollo de IA con una eficiencia optimizada.
type: docs
weight: 10
url: /es/net/aspose.words.ai/aimodel/create/
---
## AiModel.Create method

Crea una nueva instancia de[`AiModel`](../) clase.

```csharp
public static AiModel Create(AiModelType modelType)
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

* enum [AiModelType](../../aimodeltype/)
* class [AiModel](../)
* espacio de nombres [Aspose.Words.AI](../../../aspose.words.ai/)
* asamblea [Aspose.Words](../../../)
