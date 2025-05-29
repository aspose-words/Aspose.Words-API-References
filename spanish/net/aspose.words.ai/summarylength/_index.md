---
title: SummaryLength Enum
linktitle: SummaryLength
articleTitle: SummaryLength
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.AI.SummaryLength, que ofrece opciones flexibles de longitud de resumen para mejorar el resumen del documento y mejorar la claridad del contenido.
type: docs
weight: 110
url: /es/net/aspose.words.ai/summarylength/
---
## SummaryLength enumeration

Enumera las longitudes posibles del resumen.

```csharp
public enum SummaryLength
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| VeryShort | `0` | Intenta generar 1-2 oraciones. |
| Short | `1` | Intenta generar 3-4 oraciones. |
| Medium | `2` | Intenta generar 5-6 oraciones. |
| Long | `3` | Intenta generar entre 7 y 10 oraciones. |
| VeryLong | `4` | Intenta generar entre 11 y 20 oraciones. |

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
