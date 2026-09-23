---
title: "SummarizeOptions"
linktitle: "SummarizeOptions"
second_title: "Aspose.Words per Java"
description: "Consente di specificare varie opzioni per riassumere il contenuto del documento in Java."
type: docs
weight: 646
url: /it/java/com.aspose.words/summarizeoptions/
---

**Inheritance:**
java.lang.Object
```
public class SummarizeOptions
```

Consente di specificare varie opzioni per riassumere il contenuto del documento.

 **Examples:** 

Mostra come riassumere il testo utilizzando i modelli OpenAI e Google.

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
## Costruttori

| Costruttore | Descrizione |
| --- | --- |
| [SummarizeOptions()](#SummarizeOptions) | Inizializza una nuova istanza della classe [SummarizeOptions](../../com.aspose.words/summarizeoptions/). |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getSummaryLength()](#getSummaryLength) | Consente di specificare la lunghezza del riassunto. |
| [setSummaryLength(int value)](#setSummaryLength-int) | Consente di specificare la lunghezza del riassunto. |
### SummarizeOptions() {#SummarizeOptions}
```
public SummarizeOptions()
```


Inizializza una nuova istanza della classe [SummarizeOptions](../../com.aspose.words/summarizeoptions/).

 **Examples:** 

Mostra come riassumere il testo utilizzando i modelli OpenAI e Google.

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


Consente di specificare la lunghezza del riassunto. Il valore predefinito è [SummaryLength.MEDIUM](../../com.aspose.words/summarylength/\#MEDIUM).

 **Examples:** 

Mostra come riassumere il testo utilizzando i modelli OpenAI e Google.

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
int - Il valore  int  corrispondente. Il valore restituito è una delle costanti [SummaryLength](../../com.aspose.words/summarylength/).
### setSummaryLength(int value) {#setSummaryLength-int}
```
public void setSummaryLength(int value)
```


Consente di specificare la lunghezza del riassunto. Il valore predefinito è [SummaryLength.MEDIUM](../../com.aspose.words/summarylength/\#MEDIUM).

 **Examples:** 

Mostra come riassumere il testo utilizzando i modelli OpenAI e Google.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Il valore  int  corrispondente. Il valore deve essere una delle costanti [SummaryLength](../../com.aspose.words/summarylength/). |

