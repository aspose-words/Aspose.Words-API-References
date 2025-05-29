---
title: IAiModelText.Summarize
linktitle: Summarize
articleTitle: Summarize
second_title: Aspose.Words per .NET
description: Riepiloga i documenti senza sforzo con IAiModelText. Personalizza la lunghezza del riepilogo utilizzando l'intelligenza artificiale avanzata per un'estrazione precisa dei contenuti e una migliore leggibilità.
type: docs
weight: 20
url: /it/net/aspose.words.ai/iaimodeltext/summarize/
---
## Summarize(*[Document](../../../aspose.words/document/), [SummarizeOptions](../../summarizeoptions/)*) {#summarize}

Genera un riepilogo del documento specificato, con opzioni per regolare la lunghezza del riepilogo. Questa operazione sfrutta il modello di intelligenza artificiale connesso per l'elaborazione dei contenuti.

```csharp
public Document Summarize(Document sourceDocument, SummarizeOptions options = null)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| sourceDocument | Document | Il documento da riassumere. |
| options | SummarizeOptions | Impostazioni facoltative per controllare la lunghezza del riepilogo e altri parametri. |

### Valore di ritorno

Una versione riassunta del contenuto del documento.

## Esempi

Mostra come riassumere il testo utilizzando i modelli OpenAI e Google.

```csharp
Document firstDoc = new Document(MyDir + "Big document.docx");
Document secondDoc = new Document(MyDir + "Document.docx");

string apiKey = Environment.GetEnvironmentVariable("API_KEY");
// Utilizza modelli linguistici generativi OpenAI o Google.
IAiModelText model = ((OpenAiModel)AiModel.Create(AiModelType.Gpt4OMini).WithApiKey(apiKey)).WithOrganization("Organization").WithProject("Project");

SummarizeOptions options = new SummarizeOptions();

options.SummaryLength = SummaryLength.Short;
Document oneDocumentSummary = model.Summarize(firstDoc, options);
oneDocumentSummary.Save(ArtifactsDir + "AI.AiSummarize.One.docx");

options.SummaryLength = SummaryLength.Long;
Document multiDocumentSummary = model.Summarize(new Document[] { firstDoc, secondDoc }, options);
multiDocumentSummary.Save(ArtifactsDir + "AI.AiSummarize.Multi.docx");
```

### Guarda anche

* class [Document](../../../aspose.words/document/)
* class [SummarizeOptions](../../summarizeoptions/)
* interface [IAiModelText](../)
* spazio dei nomi [Aspose.Words.AI](../../../aspose.words.ai/)
* assemblea [Aspose.Words](../../../)

---

## Summarize(*Document[], [SummarizeOptions](../../summarizeoptions/)*) {#summarize_1}

Genera riepiloghi per una matrice di documenti, con opzioni per controllare la lunghezza del riepilogo e altre impostazioni. Questo metodo utilizza il modello di intelligenza artificiale connessa per elaborare ciascun documento nella matrice.

```csharp
public Document Summarize(Document[] sourceDocuments, SummarizeOptions options = null)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| sourceDocuments | Document[] | Una serie di documenti da riassumere. |
| options | SummarizeOptions | Impostazioni opzionali per controllare la lunghezza del riepilogo e altri parametri |

### Valore di ritorno

Una versione riassunta del contenuto del documento.

## Esempi

Mostra come riassumere il testo utilizzando i modelli OpenAI e Google.

```csharp
Document firstDoc = new Document(MyDir + "Big document.docx");
Document secondDoc = new Document(MyDir + "Document.docx");

string apiKey = Environment.GetEnvironmentVariable("API_KEY");
// Utilizza modelli linguistici generativi OpenAI o Google.
IAiModelText model = ((OpenAiModel)AiModel.Create(AiModelType.Gpt4OMini).WithApiKey(apiKey)).WithOrganization("Organization").WithProject("Project");

SummarizeOptions options = new SummarizeOptions();

options.SummaryLength = SummaryLength.Short;
Document oneDocumentSummary = model.Summarize(firstDoc, options);
oneDocumentSummary.Save(ArtifactsDir + "AI.AiSummarize.One.docx");

options.SummaryLength = SummaryLength.Long;
Document multiDocumentSummary = model.Summarize(new Document[] { firstDoc, secondDoc }, options);
multiDocumentSummary.Save(ArtifactsDir + "AI.AiSummarize.Multi.docx");
```

### Guarda anche

* class [Document](../../../aspose.words/document/)
* class [SummarizeOptions](../../summarizeoptions/)
* interface [IAiModelText](../)
* spazio dei nomi [Aspose.Words.AI](../../../aspose.words.ai/)
* assemblea [Aspose.Words](../../../)
