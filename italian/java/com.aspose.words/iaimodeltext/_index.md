---
title: "IAiModelText"
linktitle: "IAiModelText"
second_title: "Aspose.Words per Java"
description: "L'interfaccia comune per i modelli AI progettati per generare una varietà di contenuti basati su testo in Java."
type: docs
weight: 748
url: /it/java/com.aspose.words/iaimodeltext/
---
```
public interface IAiModelText
```

L'interfaccia comune per i modelli AI progettati per generare una varietà di contenuti basati su testo.
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [checkGrammar(Document sourceDocument, CheckGrammarOptions options)](#checkGrammar-com.aspose.words.Document-com.aspose.words.CheckGrammarOptions) | Verifica la grammatica del documento fornito. |
| [summarize(Document sourceDocument, SummarizeOptions options)](#summarize-com.aspose.words.Document-com.aspose.words.SummarizeOptions) | Genera un riepilogo del documento specificato, con opzioni per regolare la lunghezza del riepilogo. |
| [summarize(Document[] sourceDocuments, SummarizeOptions options)](#summarize-com.aspose.words.Document---com.aspose.words.SummarizeOptions) | Genera riepiloghi per un array di documenti, con opzioni per controllare la lunghezza del riepilogo e altre impostazioni. |
| [translate(Document sourceDocument, int targetLanguage)](#translate-com.aspose.words.Document-int) |  |
### checkGrammar(Document sourceDocument, CheckGrammarOptions options) {#checkGrammar-com.aspose.words.Document-com.aspose.words.CheckGrammarOptions}
```
public abstract Document checkGrammar(Document sourceDocument, CheckGrammarOptions options)
```


Verifica la grammatica del documento fornito. Questa operazione utilizza il modello AI connesso per la verifica della grammatica del documento.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| sourceDocument | [Document](../../com.aspose.words/document/) | Il documento in fase di verifica grammaticale. |
| options | [CheckGrammarOptions](../../com.aspose.words/checkgrammaroptions/) | Impostazioni opzionali per controllare come verrà verificata la grammatica. |

**Returns:**
[Document](../../com.aspose.words/document/) - A new [Document](../../com.aspose.words/document/) with checked grammar.
### summarize(Document sourceDocument, SummarizeOptions options) {#summarize-com.aspose.words.Document-com.aspose.words.SummarizeOptions}
```
public abstract Document summarize(Document sourceDocument, SummarizeOptions options)
```


Genera un riepilogo del documento specificato, con opzioni per regolare la lunghezza del riepilogo. Questa operazione utilizza il modello AI connesso per l'elaborazione dei contenuti.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| sourceDocument | [Document](../../com.aspose.words/document/) | Il documento da riepilogare. |
| options | [SummarizeOptions](../../com.aspose.words/summarizeoptions/) | Impostazioni opzionali per controllare la lunghezza del riepilogo e altri parametri. |

**Returns:**
[Document](../../com.aspose.words/document/) - A summarized version of the document's content.
### summarize(Document[] sourceDocuments, SummarizeOptions options) {#summarize-com.aspose.words.Document---com.aspose.words.SummarizeOptions}
```
public abstract Document summarize(Document[] sourceDocuments, SummarizeOptions options)
```


Genera riepiloghi per un array di documenti, con opzioni per controllare la lunghezza del riepilogo e altre impostazioni. Questo metodo utilizza il modello AI connesso per l'elaborazione di ciascun documento nell'array.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| sourceDocuments | [Document\[\]](../../com.aspose.words/document/) | Un array di documenti da riepilogare. |
| options | [SummarizeOptions](../../com.aspose.words/summarizeoptions/) | Impostazioni opzionali per controllare la lunghezza del riepilogo e altri parametri |

**Returns:**
[Document](../../com.aspose.words/document/) - A summarized version of the document's content.
### translate(Document sourceDocument, int targetLanguage) {#translate-com.aspose.words.Document-int}
```
public abstract Document translate(Document sourceDocument, int targetLanguage)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| sourceDocument | [Document](../../com.aspose.words/document/) |  |
| targetLanguage | int |  |

**Returns:**
[Document](../../com.aspose.words/document/)
