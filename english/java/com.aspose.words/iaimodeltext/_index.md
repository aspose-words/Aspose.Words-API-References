---
title: IAiModelText
linktitle: IAiModelText
second_title: Aspose.Words for Java
description: The common interface for AI models designed to generate a variety of text-based content in Java.
type: docs
weight: 744
url: /java/com.aspose.words/iaimodeltext/
---
```
public interface IAiModelText
```

The common interface for AI models designed to generate a variety of text-based content.
## Methods

| Method | Description |
| --- | --- |
| [checkGrammar(Document sourceDocument, CheckGrammarOptions options)](#checkGrammar-com.aspose.words.Document-com.aspose.words.CheckGrammarOptions) | Checks grammar of the provided document. |
| [summarize(Document sourceDocument, SummarizeOptions options)](#summarize-com.aspose.words.Document-com.aspose.words.SummarizeOptions) | Generates a summary of the specified document, with options to adjust the length of the summary. |
| [summarize(Document[] sourceDocuments, SummarizeOptions options)](#summarize-com.aspose.words.Document---com.aspose.words.SummarizeOptions) | Generates summaries for an array of documents, with options to control the summary length and other settings. |
| [translate(Document sourceDocument, int targetLanguage)](#translate-com.aspose.words.Document-int) |  |
### checkGrammar(Document sourceDocument, CheckGrammarOptions options) {#checkGrammar-com.aspose.words.Document-com.aspose.words.CheckGrammarOptions}
```
public abstract Document checkGrammar(Document sourceDocument, CheckGrammarOptions options)
```


Checks grammar of the provided document. This operation leverages the connected AI model for checking grammar of document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| sourceDocument | [Document](../../com.aspose.words/document/) | The document being checked for grammar. |
| options | [CheckGrammarOptions](../../com.aspose.words/checkgrammaroptions/) | Optional settings to control how grammar will be checked. |

**Returns:**
[Document](../../com.aspose.words/document/) - A new [Document](../../com.aspose.words/document/) with checked grammar.
### summarize(Document sourceDocument, SummarizeOptions options) {#summarize-com.aspose.words.Document-com.aspose.words.SummarizeOptions}
```
public abstract Document summarize(Document sourceDocument, SummarizeOptions options)
```


Generates a summary of the specified document, with options to adjust the length of the summary. This operation leverages the connected AI model for content processing.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| sourceDocument | [Document](../../com.aspose.words/document/) | The document to be summarized. |
| options | [SummarizeOptions](../../com.aspose.words/summarizeoptions/) | Optional settings to control the summary length and other parameters. |

**Returns:**
[Document](../../com.aspose.words/document/) - A summarized version of the document's content.
### summarize(Document[] sourceDocuments, SummarizeOptions options) {#summarize-com.aspose.words.Document---com.aspose.words.SummarizeOptions}
```
public abstract Document summarize(Document[] sourceDocuments, SummarizeOptions options)
```


Generates summaries for an array of documents, with options to control the summary length and other settings. This method utilizes the connected AI model for processing each document in the array.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| sourceDocuments | [Document\[\]](../../com.aspose.words/document/) | An array of documents to be summarized. |
| options | [SummarizeOptions](../../com.aspose.words/summarizeoptions/) | Optional settings to control the summary length and other parameters |

**Returns:**
[Document](../../com.aspose.words/document/) - A summarized version of the document's content.
### translate(Document sourceDocument, int targetLanguage) {#translate-com.aspose.words.Document-int}
```
public abstract Document translate(Document sourceDocument, int targetLanguage)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| sourceDocument | [Document](../../com.aspose.words/document/) |  |
| targetLanguage | int |  |

**Returns:**
[Document](../../com.aspose.words/document/)
