---
title: OpenAiModel Class
linktitle: OpenAiModel
articleTitle: OpenAiModel
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.AI.OpenAiModel su puerta de entrada a una integración perfecta con los potentes modelos de lenguaje de OpenAI para un mejor procesamiento de documentos.
type: docs
weight: 90
url: /es/net/aspose.words.ai/openaimodel/
---
## OpenAiModel class

Una clase abstracta que representa la integración con los grandes modelos de lenguaje de OpenAI dentro de Aspose.Words.

```csharp
public abstract class OpenAiModel : AiModel, IAiModelText
```

## Métodos

| Nombre | Descripción |
| --- | --- |
| [WithApiKey](../../aspose.words.ai/aimodel/withapikey/)(*string*) | Establece una clave API específica para el modelo. |
| [WithOrganization](../../aspose.words.ai/openaimodel/withorganization/)(*string*) | Establece una organización específica para el modelo. |
| [WithProject](../../aspose.words.ai/openaimodel/withproject/)(*string*) | Establece un proyecto específico para el modelo. |

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
