---
title: AiModelType Enum
linktitle: AiModelType
articleTitle: AiModelType
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.AI.AiModelType para una integración perfecta de modelos de IA en el procesamiento de documentos, mejorando la eficiencia y la productividad.
type: docs
weight: 30
url: /es/net/aspose.words.ai/aimodeltype/
---
## AiModelType enumeration

Representa los tipos de[`AiModel`](../aimodel/) que se puede integrar en el flujo de trabajo de procesamiento de documentos.

```csharp
public enum AiModelType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Gpt4O | `0` | Tipo de modelo generativo GPT-4o. |
| Gpt4OMini | `1` | Tipo de modelo generativo mini GPT-4o. |
| Gpt4Turbo | `2` | Tipo de modelo generativo Turbo GPT-4. |
| Gpt35Turbo | `3` | Tipo de modelo generativo Turbo GPT-3.5. |
| Gemini15Flash | `4` | Tipo de modelo generativo Flash Gemini 1.5. |
| Gemini15Flash8B | `5` | Tipo de modelo generativo Gemini 1.5 Flash-8B. |
| Gemini15Pro | `6` | Tipo de modelo generativo de Gemini 1.5 Pro. |
| Claude35Sonnet | `7` | Modelo generativo tipo Claude 3.5 Sonnet. |
| Claude35Haiku | `8` | Claude 3.5 Tipo de modelo generativo de Haiku. |
| Claude3Opus | `9` | Tipo de modelo generativo Claude 3 Opus. |
| Claude3Sonnet | `10` | Modelo generativo tipo Claude 3 Sonnet. |
| Claude3Haiku | `11` | Claude 3 Haiku tipo modelo generativo. |

## Observaciones

Esta enumeración se utiliza para definir qué modelo de lenguaje grande (LLM) se debe utilizar para tareas como resumen, traducción y generación de contenido.

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
