---
title: "AnthropicAiModel"
linktitle: "AnthropicAiModel"
second_title: "Aspose.Words для Java"
description: "Абстрактный класс, представляющий интеграцию с AI‑моделями Anthropicu2019 в Aspose.Words на Java."
type: docs
weight: 16
url: /ru/java/com.aspose.words/anthropicaimodel/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.AiModel](../../com.aspose.words/aimodel/)
```
public abstract class AnthropicAiModel extends AiModel
```

Абстрактный класс, представляющий интеграцию с AI‑моделями Anthropic в Aspose.Words.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [AnthropicAiModel()](#AnthropicAiModel) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [checkGrammar(Document sourceDocument, CheckGrammarOptions options)](#checkGrammar-com.aspose.words.Document-com.aspose.words.CheckGrammarOptions) | Проверяет грамматику предоставленного документа. |
| [create(int modelType)](#create-int) |  |
| [getTimeout()](#getTimeout) | Получает количество миллисекунд ожидания до истечения времени запроса к AI‑модели. |
| [getUrl()](#getUrl) | Получает URL модели. |
| [setTimeout(int value)](#setTimeout-int) | Устанавливает количество миллисекунд ожидания до истечения времени запроса к AI‑модели. |
| [setUrl(String value)](#setUrl-java.lang.String) | Устанавливает URL модели. |
| [summarize(Document sourceDocument)](#summarize-com.aspose.words.Document) |  |
| [summarize(Document sourceDocument, SummarizeOptions options)](#summarize-com.aspose.words.Document-com.aspose.words.SummarizeOptions) | Создаёт краткое содержание указанного документа с возможностью регулировать его длину. |
| [summarize(Document[] sourceDocuments)](#summarize-com.aspose.words.Document) |  |
| [summarize(Document[] sourceDocuments, SummarizeOptions options)](#summarize-com.aspose.words.Document---com.aspose.words.SummarizeOptions) | Создаёт краткие содержания для массива документов с возможностью управлять длиной резюме и другими параметрами. |
| [translate(Document sourceDocument, int targetLanguage)](#translate-com.aspose.words.Document-int) |  |
| [withApiKey(String apiKey)](#withApiKey-java.lang.String) | Устанавливает указанный API‑ключ для модели. |
### AnthropicAiModel() {#AnthropicAiModel}
```
public AnthropicAiModel()
```


### checkGrammar(Document sourceDocument, CheckGrammarOptions options) {#checkGrammar-com.aspose.words.Document-com.aspose.words.CheckGrammarOptions}
```
public Document checkGrammar(Document sourceDocument, CheckGrammarOptions options)
```


Проверяет грамматику предоставленного документа. Эта операция использует подключённую AI‑модель для проверки грамматики документа.

 **Examples:** 

Показывает, как проверить грамматику документа.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 String apiKey = System.getenv("API_KEY");
 // Use OpenAI generative language models.
 AiModel model = AiModel.create(AiModelType.GPT_4_O_MINI).withApiKey(apiKey);

 CheckGrammarOptions grammarOptions = new CheckGrammarOptions();
 grammarOptions.setImproveStylistics(true);

 Document proofedDoc = model.checkGrammar(doc, grammarOptions);
 proofedDoc.save(getArtifactsDir() + "AI.AiGrammar.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| sourceDocument | [Document](../../com.aspose.words/document/) | Документ, проверяемый на грамматику. |
| options | [CheckGrammarOptions](../../com.aspose.words/checkgrammaroptions/) | Необязательные настройки, позволяющие контролировать процесс проверки грамматики. |

**Returns:**
[Document](../../com.aspose.words/document/) - A new [Document](../../com.aspose.words/document/) with checked grammar.
### create(int modelType) {#create-int}
```
public static AiModel create(int modelType)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| modelType | int |  |

**Returns:**
[AiModel](../../com.aspose.words/aimodel/)
### getTimeout() {#getTimeout}
```
public int getTimeout()
```


Получает количество миллисекунд, которое следует ждать до истечения времени запроса к модели ИИ. Значение по умолчанию — 100 000 миллисекунд (100 секунд).

 **Examples:** 

Показывает, как изменить значение тайм‑аута модели по умолчанию.

```

 String apiKey = System.getenv("API_KEY");
 AiModel model = AiModel.create(AiModelType.GPT_4_O_MINI).withApiKey(apiKey);
 // Default value 100000ms.
 model.setTimeout(250000);
 
```

**Returns:**
int — количество миллисекунд, которое следует ждать до истечения времени запроса к модели ИИ.
### getUrl() {#getUrl}
```
public String getUrl()
```


Получает URL модели. Значение по умолчанию — "https://api.anthropic.com/".

**Returns:**
java.lang.String — URL модели.
### setTimeout(int value) {#setTimeout-int}
```
public void setTimeout(int value)
```


Устанавливает количество миллисекунд, которое следует ждать до истечения времени запроса к модели ИИ. Значение по умолчанию — 100 000 миллисекунд (100 секунд).

 **Examples:** 

Показывает, как изменить значение тайм‑аута модели по умолчанию.

```

 String apiKey = System.getenv("API_KEY");
 AiModel model = AiModel.create(AiModelType.GPT_4_O_MINI).withApiKey(apiKey);
 // Default value 100000ms.
 model.setTimeout(250000);
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | int | Количество миллисекунд, которое следует ждать до истечения времени запроса к модели ИИ. |

### setUrl(String value) {#setUrl-java.lang.String}
```
public void setUrl(String value)
```


Устанавливает URL модели. Значение по умолчанию — "https://api.anthropic.com/".

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | URL модели. |

### summarize(Document sourceDocument) {#summarize-com.aspose.words.Document}
```
public Document summarize(Document sourceDocument)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| sourceDocument | [Document](../../com.aspose.words/document/) |  |

**Returns:**
[Document](../../com.aspose.words/document/)
### summarize(Document sourceDocument, SummarizeOptions options) {#summarize-com.aspose.words.Document-com.aspose.words.SummarizeOptions}
```
public Document summarize(Document sourceDocument, SummarizeOptions options)
```


Создаёт краткое содержание указанного документа с возможностью регулировать его длину. Эта операция использует подключённую AI‑модель для обработки контента.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| sourceDocument | [Document](../../com.aspose.words/document/) | Документ, подлежащий резюмированию. |
| options | [SummarizeOptions](../../com.aspose.words/summarizeoptions/) | Необязательные настройки для контроля длины резюме и других параметров. |

**Returns:**
[Document](../../com.aspose.words/document/) - A summarized version of the document's content.
### summarize(Document[] sourceDocuments) {#summarize-com.aspose.words.Document}
```
public Document summarize(Document[] sourceDocuments)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| sourceDocuments | [Document\[\]](../../com.aspose.words/document/) |  |

**Returns:**
[Document](../../com.aspose.words/document/)
### summarize(Document[] sourceDocuments, SummarizeOptions options) {#summarize-com.aspose.words.Document---com.aspose.words.SummarizeOptions}
```
public Document summarize(Document[] sourceDocuments, SummarizeOptions options)
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
public Document translate(Document sourceDocument, int targetLanguage)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| sourceDocument | [Document](../../com.aspose.words/document/) |  |
| targetLanguage | int |  |

**Returns:**
[Document](../../com.aspose.words/document/)
### withApiKey(String apiKey) {#withApiKey-java.lang.String}
```
public AiModel withApiKey(String apiKey)
```


Устанавливает указанный API‑ключ для модели.

 **Examples:** 

Показывает, как суммировать текст с использованием моделей OpenAI и Google.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| apiKey | java.lang.String |  |

**Returns:**
[AiModel](../../com.aspose.words/aimodel/)
