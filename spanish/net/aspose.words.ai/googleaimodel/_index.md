---
title: GoogleAiModel Class
linktitle: GoogleAiModel
articleTitle: GoogleAiModel
second_title: Aspose.Words para .NET
description: Descubra el poder de la clase Aspose.Words.AI.GoogleAiModel para integrar sin problemas los modelos de inteligencia artificial de Google y mejorar sus capacidades de procesamiento de documentos sin esfuerzo.
type: docs
weight: 60
url: /es/net/aspose.words.ai/googleaimodel/
---
## GoogleAiModel class

Una clase abstracta que representa la integración con los modelos de IA de Google dentro de Aspose.Words.

```csharp
public abstract class GoogleAiModel : AiModel, IAiModelText
```

## Métodos

| Nombre | Descripción |
| --- | --- |
| [WithApiKey](../../aspose.words.ai/aimodel/withapikey/)(*string*) | Establece una clave API específica para el modelo. |

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

* class [AiModel](../aimodel/)
* interface [IAiModelText](../iaimodeltext/)
* espacio de nombres [Aspose.Words.AI](../../aspose.words.ai/)
* asamblea [Aspose.Words](../../)
