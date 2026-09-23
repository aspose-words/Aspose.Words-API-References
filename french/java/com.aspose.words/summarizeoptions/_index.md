---
title: "SummarizeOptions"
linktitle: "SummarizeOptions"
second_title: "Aspose.Words pour Java"
description: "Permet de spécifier diverses options pour résumer le contenu du document en Java."
type: docs
weight: 646
url: /fr/java/com.aspose.words/summarizeoptions/
---

**Inheritance:**
java.lang.Object
```
public class SummarizeOptions
```

Permet de spécifier diverses options pour résumer le contenu du document.

 **Examples:** 

Montre comment résumer le texte en utilisant les modèles OpenAI et Google.

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
## Constructors

| Constructor | Description |
| --- | --- |
| [SummarizeOptions()](#SummarizeOptions) | Initialise une nouvelle instance de la classe [SummarizeOptions](../../com.aspose.words/summarizeoptions/). |
## Méthodes

| Méthode | Description |
| --- | --- |
| [getSummaryLength()](#getSummaryLength) | Permet de spécifier la longueur du résumé. |
| [setSummaryLength(int value)](#setSummaryLength-int) | Permet de spécifier la longueur du résumé. |
### SummarizeOptions() {#SummarizeOptions}
```
public SummarizeOptions()
```


Initialise une nouvelle instance de la classe [SummarizeOptions](../../com.aspose.words/summarizeoptions/).

 **Examples:** 

Montre comment résumer le texte en utilisant les modèles OpenAI et Google.

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


Permet de spécifier la longueur du résumé. La valeur par défaut est [SummaryLength.MEDIUM](../../com.aspose.words/summarylength/\#MEDIUM).

 **Examples:** 

Montre comment résumer le texte en utilisant les modèles OpenAI et Google.

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
int - La valeur  int  correspondante. La valeur retournée est l'une des constantes [SummaryLength](../../com.aspose.words/summarylength/) constants.
### setSummaryLength(int value) {#setSummaryLength-int}
```
public void setSummaryLength(int value)
```


Permet de spécifier la longueur du résumé. La valeur par défaut est [SummaryLength.MEDIUM](../../com.aspose.words/summarylength/\#MEDIUM).

 **Examples:** 

Montre comment résumer le texte en utilisant les modèles OpenAI et Google.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | La valeur  int  correspondante. La valeur doit être l'une des constantes [SummaryLength](../../com.aspose.words/summarylength/) constants. |

