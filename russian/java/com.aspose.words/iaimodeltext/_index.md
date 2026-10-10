---
title: "IAiModelText"
linktitle: "IAiModelText"
second_title: "Aspose.Words для Java"
description: "Общий интерфейс для AI‑моделей, предназначенных для создания разнообразного текстового контента на Java."
type: docs
weight: 748
url: /ru/java/com.aspose.words/iaimodeltext/
---
```
public interface IAiModelText
```

Общий интерфейс для AI‑моделей, предназначенных для создания разнообразного текстового контента.
## Методы

| Метод | Описание |
| --- | --- |
| [checkGrammar(Document sourceDocument, CheckGrammarOptions options)](#checkGrammar-com.aspose.words.Document-com.aspose.words.CheckGrammarOptions) | Проверяет грамматику предоставленного документа. |
| [summarize(Document sourceDocument, SummarizeOptions options)](#summarize-com.aspose.words.Document-com.aspose.words.SummarizeOptions) | Создаёт краткое содержание указанного документа с возможностью регулировать его длину. |
| [summarize(Document[] sourceDocuments, SummarizeOptions options)](#summarize-com.aspose.words.Document---com.aspose.words.SummarizeOptions) | Создаёт краткие содержания для массива документов с возможностью управлять длиной резюме и другими параметрами. |
| [translate(Document sourceDocument, int targetLanguage)](#translate-com.aspose.words.Document-int) |  |
### checkGrammar(Document sourceDocument, CheckGrammarOptions options) {#checkGrammar-com.aspose.words.Document-com.aspose.words.CheckGrammarOptions}
```
public abstract Document checkGrammar(Document sourceDocument, CheckGrammarOptions options)
```


Проверяет грамматику предоставленного документа. Эта операция использует подключённую AI‑модель для проверки грамматики документа.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| sourceDocument | [Document](../../com.aspose.words/document/) | Документ, проверяемый на грамматику. |
| options | [CheckGrammarOptions](../../com.aspose.words/checkgrammaroptions/) | Необязательные настройки, позволяющие контролировать процесс проверки грамматики. |

**Returns:**
[Document](../../com.aspose.words/document/) - A new [Document](../../com.aspose.words/document/) with checked grammar.
### summarize(Document sourceDocument, SummarizeOptions options) {#summarize-com.aspose.words.Document-com.aspose.words.SummarizeOptions}
```
public abstract Document summarize(Document sourceDocument, SummarizeOptions options)
```


Создаёт краткое содержание указанного документа с возможностью регулировать его длину. Эта операция использует подключённую AI‑модель для обработки контента.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| sourceDocument | [Document](../../com.aspose.words/document/) | Документ, подлежащий резюмированию. |
| options | [SummarizeOptions](../../com.aspose.words/summarizeoptions/) | Необязательные настройки для контроля длины резюме и других параметров. |

**Returns:**
[Document](../../com.aspose.words/document/) - A summarized version of the document's content.
### summarize(Document[] sourceDocuments, SummarizeOptions options) {#summarize-com.aspose.words.Document---com.aspose.words.SummarizeOptions}
```
public abstract Document summarize(Document[] sourceDocuments, SummarizeOptions options)
```


Создаёт резюме для массива документов с возможностью управлять длиной резюме и другими настройками. Этот метод использует подключённую AI‑модель для обработки каждого документа в массиве.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| sourceDocuments | [Document\[\]](../../com.aspose.words/document/) | Массив документов, подлежащих резюмированию. |
| options | [SummarizeOptions](../../com.aspose.words/summarizeoptions/) | Необязательные настройки для контроля длины резюме и других параметров |

**Returns:**
[Document](../../com.aspose.words/document/) - A summarized version of the document's content.
### translate(Document sourceDocument, int targetLanguage) {#translate-com.aspose.words.Document-int}
```
public abstract Document translate(Document sourceDocument, int targetLanguage)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| sourceDocument | [Document](../../com.aspose.words/document/) |  |
| targetLanguage | int |  |

**Returns:**
[Document](../../com.aspose.words/document/)
