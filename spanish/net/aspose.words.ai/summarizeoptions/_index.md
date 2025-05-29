---
title: SummarizeOptions Class
linktitle: SummarizeOptions
articleTitle: SummarizeOptions
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.AI.SummarizeOptions para personalizar y mejorar el resumen de su documento para obtener información más clara y una mejor gestión del contenido.
type: docs
weight: 100
url: /es/net/aspose.words.ai/summarizeoptions/
---
## SummarizeOptions class

Permite especificar varias opciones para resumir el contenido del documento.

```csharp
public class SummarizeOptions
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [SummarizeOptions](summarizeoptions/)() | Inicializa una nueva instancia de`SummarizeOptions` clase. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [SummaryLength](../../aspose.words.ai/summarizeoptions/summarylength/) { get; set; } | Permite especificar la longitud del resumen. El valor predeterminado esMedium . |

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
