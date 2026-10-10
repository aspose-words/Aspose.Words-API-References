---
title: "SummarizeOptions"
linktitle: "SummarizeOptions"
second_title: "Aspose.Words para Java"
description: "Permite especificar varias opciones para resumir el contenido del documento en Java."
type: docs
weight: 646
url: /es/java/com.aspose.words/summarizeoptions/
---

**Inheritance:**
java.lang.Object
```
public class SummarizeOptions
```

Permite especificar varias opciones para resumir el contenido del documento.

 **Examples:** 

Muestra cómo resumir texto usando los modelos de OpenAI y Google.

```

 Document firstDoc = new Document(getMyDir() + "Big document.docx");
 Document secondDoc = new Document(getMyDir() + "Document.docx");

 String apiKey = System.getenv("API_KEY");
 // Use OpenAI or Google generative language models.
 AiModel model = ((OpenAiModel)AiModel.create(AiModelType.GPT_4_O_MINI).withApiKey(apiKey)).withOrganization("Organization").withProject("Project");

 SummarizeOptions options = new SummarizeOptions();

 options.setSummaryLength(SummaryLength.SHORT);
 Document oneDocumentSummary = model.summarize(firstDoc, options);
 oneDocumentSummary.save(getArtifactsDir() + "AI.AiSummarize.One.docx");

 options.setSummaryLength(SummaryLength.LONG);
 Document multiDocumentSummary = model.summarize(new Document[] { firstDoc, secondDoc }, options);
 multiDocumentSummary.save(getArtifactsDir() + "AI.AiSummarize.Multi.docx");
 
```
## Constructores

| Constructor | Descripción |
| --- | --- |
| [SummarizeOptions()](#SummarizeOptions) | Inicializa una nueva instancia de la clase [SummarizeOptions](../../com.aspose.words/summarizeoptions/). |
## Métodos

| Método | Descripción |
| --- | --- |
| [getSummaryLength()](#getSummaryLength) | Permite especificar la longitud del resumen. |
| [setSummaryLength(int value)](#setSummaryLength-int) | Permite especificar la longitud del resumen. |
### SummarizeOptions() {#SummarizeOptions}
```
public SummarizeOptions()
```


Inicializa una nueva instancia de la clase [SummarizeOptions](../../com.aspose.words/summarizeoptions/).

 **Examples:** 

Muestra cómo resumir texto usando los modelos de OpenAI y Google.

```

 Document firstDoc = new Document(getMyDir() + "Big document.docx");
 Document secondDoc = new Document(getMyDir() + "Document.docx");

 String apiKey = System.getenv("API_KEY");
 // Use OpenAI or Google generative language models.
 AiModel model = ((OpenAiModel)AiModel.create(AiModelType.GPT_4_O_MINI).withApiKey(apiKey)).withOrganization("Organization").withProject("Project");

 SummarizeOptions options = new SummarizeOptions();

 options.setSummaryLength(SummaryLength.SHORT);
 Document oneDocumentSummary = model.summarize(firstDoc, options);
 oneDocumentSummary.save(getArtifactsDir() + "AI.AiSummarize.One.docx");

 options.setSummaryLength(SummaryLength.LONG);
 Document multiDocumentSummary = model.summarize(new Document[] { firstDoc, secondDoc }, options);
 multiDocumentSummary.save(getArtifactsDir() + "AI.AiSummarize.Multi.docx");
 
```

### getSummaryLength() {#getSummaryLength}
```
public int getSummaryLength()
```


Permite especificar la longitud del resumen. El valor predeterminado es [SummaryLength.MEDIUM](../../com.aspose.words/summarylength/\#MEDIUM).

 **Examples:** 

Muestra cómo resumir texto usando los modelos de OpenAI y Google.

```

 Document firstDoc = new Document(getMyDir() + "Big document.docx");
 Document secondDoc = new Document(getMyDir() + "Document.docx");

 String apiKey = System.getenv("API_KEY");
 // Use OpenAI or Google generative language models.
 AiModel model = ((OpenAiModel)AiModel.create(AiModelType.GPT_4_O_MINI).withApiKey(apiKey)).withOrganization("Organization").withProject("Project");

 SummarizeOptions options = new SummarizeOptions();

 options.setSummaryLength(SummaryLength.SHORT);
 Document oneDocumentSummary = model.summarize(firstDoc, options);
 oneDocumentSummary.save(getArtifactsDir() + "AI.AiSummarize.One.docx");

 options.setSummaryLength(SummaryLength.LONG);
 Document multiDocumentSummary = model.summarize(new Document[] { firstDoc, secondDoc }, options);
 multiDocumentSummary.save(getArtifactsDir() + "AI.AiSummarize.Multi.docx");
 
```

**Returns:**
int - El valor entero correspondiente. El valor devuelto es uno de los constantes de [SummaryLength](../../com.aspose.words/summarylength/).
### setSummaryLength(int value) {#setSummaryLength-int}
```
public void setSummaryLength(int value)
```


Permite especificar la longitud del resumen. El valor predeterminado es [SummaryLength.MEDIUM](../../com.aspose.words/summarylength/\#MEDIUM).

 **Examples:** 

Muestra cómo resumir texto usando los modelos de OpenAI y Google.

```

 Document firstDoc = new Document(getMyDir() + "Big document.docx");
 Document secondDoc = new Document(getMyDir() + "Document.docx");

 String apiKey = System.getenv("API_KEY");
 // Use OpenAI or Google generative language models.
 AiModel model = ((OpenAiModel)AiModel.create(AiModelType.GPT_4_O_MINI).withApiKey(apiKey)).withOrganization("Organization").withProject("Project");

 SummarizeOptions options = new SummarizeOptions();

 options.setSummaryLength(SummaryLength.SHORT);
 Document oneDocumentSummary = model.summarize(firstDoc, options);
 oneDocumentSummary.save(getArtifactsDir() + "AI.AiSummarize.One.docx");

 options.setSummaryLength(SummaryLength.LONG);
 Document multiDocumentSummary = model.summarize(new Document[] { firstDoc, secondDoc }, options);
 multiDocumentSummary.save(getArtifactsDir() + "AI.AiSummarize.Multi.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El valor entero correspondiente. El valor debe ser uno de los constantes de [SummaryLength](../../com.aspose.words/summarylength/). |

