---
title: IAiModelText Interface
linktitle: IAiModelText
articleTitle: IAiModelText
second_title: Aspose.Words para .NET
description: Desbloquee el potencial creativo con Aspose.Words.AI.IAiModelText, la interfaz versátil para modelos de IA que generan contenido de texto diverso y de alta calidad sin esfuerzo.
type: docs
weight: 70
url: /es/net/aspose.words.ai/iaimodeltext/
---
## IAiModelText interface

La interfaz común para modelos de IA diseñada para generar una variedad de contenido basado en texto.

```csharp
public interface IAiModelText
```

## Métodos

| Nombre | Descripción |
| --- | --- |
| [CheckGrammar](../../aspose.words.ai/iaimodeltext/checkgrammar/)(*[Document](../../aspose.words/document/), [CheckGrammarOptions](../checkgrammaroptions/)*) | Comprueba la gramática del documento proporcionado. Esta operación aprovecha el modelo de IA conectado para comprobar la gramática del documento. |
| [Summarize](../../aspose.words.ai/iaimodeltext/summarize/#summarize)(*[Document](../../aspose.words/document/), [SummarizeOptions](../summarizeoptions/)*) | Genera un resumen del documento especificado, con opciones para ajustar la longitud del resumen. Esta operación aprovecha el modelo de IA conectado para el procesamiento de contenido. |
| [Summarize](../../aspose.words.ai/iaimodeltext/summarize/#summarize_1)(*Document[], [SummarizeOptions](../summarizeoptions/)*) | Genera resúmenes para una matriz de documentos, con opciones para controlar la longitud del resumen y otras configuraciones. Este método utiliza el modelo de IA conectado para procesar cada documento en la matriz. |
| [Translate](../../aspose.words.ai/iaimodeltext/translate/)(*[Document](../../aspose.words/document/), [Language](../language/)*) | Traduce el documento proporcionado al idioma de destino especificado. Esta operación aprovecha el modelo de IA conectado para la traducción de contenido. |

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
