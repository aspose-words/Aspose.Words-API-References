---
title: IAiModelText.Summarize
linktitle: Summarize
articleTitle: Summarize
second_title: Aspose.Words para .NET
description: Resuma documentos fácilmente con IAiModelText. Personalice la longitud del resumen con IA avanzada para una extracción precisa del contenido y una legibilidad mejorada.
type: docs
weight: 20
url: /es/net/aspose.words.ai/iaimodeltext/summarize/
---
## Summarize(*[Document](../../../aspose.words/document/), [SummarizeOptions](../../summarizeoptions/)*) {#summarize}

Genera un resumen del documento especificado, con opciones para ajustar la longitud del resumen. Esta operación aprovecha el modelo de IA conectado para el procesamiento de contenido.

```csharp
public Document Summarize(Document sourceDocument, SummarizeOptions options = null)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| sourceDocument | Document | El documento que se va a resumir. |
| options | SummarizeOptions | Configuraciones opcionales para controlar la longitud del resumen y otros parámetros. |

### Valor_devuelto

Una versión resumida del contenido del documento.

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

* class [Document](../../../aspose.words/document/)
* class [SummarizeOptions](../../summarizeoptions/)
* interface [IAiModelText](../)
* espacio de nombres [Aspose.Words.AI](../../../aspose.words.ai/)
* asamblea [Aspose.Words](../../../)

---

## Summarize(*Document[], [SummarizeOptions](../../summarizeoptions/)*) {#summarize_1}

Genera resúmenes para una matriz de documentos, con opciones para controlar la longitud del resumen y otras configuraciones. Este método utiliza el modelo de IA conectado para procesar cada documento en la matriz.

```csharp
public Document Summarize(Document[] sourceDocuments, SummarizeOptions options = null)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| sourceDocuments | Document[] | Un conjunto de documentos para resumir. |
| options | SummarizeOptions | Configuraciones opcionales para controlar la longitud del resumen y otros parámetros |

### Valor_devuelto

Una versión resumida del contenido del documento.

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

* class [Document](../../../aspose.words/document/)
* class [SummarizeOptions](../../summarizeoptions/)
* interface [IAiModelText](../)
* espacio de nombres [Aspose.Words.AI](../../../aspose.words.ai/)
* asamblea [Aspose.Words](../../../)
