---
title: AiModel Class
linktitle: AiModel
articleTitle: AiModel
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.AI.AiModel, su clave para aprovechar los modelos de lenguaje generativo avanzados para una mejor generación y automatización de texto.
type: docs
weight: 20
url: /es/net/aspose.words.ai/aimodel/
---
## AiModel class

Representa información sobre un modelo de lenguaje generativo.

```csharp
public abstract class AiModel
```

## Métodos

| Nombre | Descripción |
| --- | --- |
| static [Create](../../aspose.words.ai/aimodel/create/)(*[AiModelType](../aimodeltype/)*) | Crea una nueva instancia de`AiModel` clase. |
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

* espacio de nombres [Aspose.Words.AI](../../aspose.words.ai/)
* asamblea [Aspose.Words](../../)
