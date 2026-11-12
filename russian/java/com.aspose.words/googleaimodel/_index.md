---
title: "GoogleAiModel"
linktitle: "GoogleAiModel"
second_title: "Aspose.Words для Java"
description: "Класс, представляющий интеграцию Google AI Models Gemini в Aspose.Words для Java."
type: docs
weight: 361
url: /ru/java/com.aspose.words/googleaimodel/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.AiModel](../../com.aspose.words/aimodel/)
```
public class GoogleAiModel extends AiModel
```

Класс, представляющий интеграцию моделей Google AI (Gemini) в Aspose.Words.

 **Remarks:** 

Смотрите https://ai.google.dev/gemini-api/docs/models для получения деталей о моделях Gemini.

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

Показывает, как использовать модель Google AI.

```

 String apiKey = System.getenv("API_KEY");
 GoogleAiModel model = new GoogleAiModel("gemini-flash-latest", apiKey);

 Document doc = new Document(getMyDir() + "Big document.docx");
 SummarizeOptions summarizeOptions = new SummarizeOptions(); { summarizeOptions.setSummaryLength(SummaryLength.VERY_SHORT); }
 Document summary = model.summarize(doc, summarizeOptions);
 
```
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [GoogleAiModel(String name)](#GoogleAiModel-java.lang.String) | Инициализирует новый экземпляр класса [GoogleAiModel](../../com.aspose.words/googleaimodel/). |
| [GoogleAiModel(String name, String apiKey)](#GoogleAiModel-java.lang.String-java.lang.String) | Инициализирует новый экземпляр класса [GoogleAiModel](../../com.aspose.words/googleaimodel/). |
## Методы

| Метод | Описание |
| --- | --- |
| [checkGrammar(Document sourceDocument, CheckGrammarOptions options)](#checkGrammar-com.aspose.words.Document-com.aspose.words.CheckGrammarOptions) | Проверяет грамматику предоставленного документа. |
| [create(int modelType)](#create-int) |  |
| [getTimeout()](#getTimeout) | Получает количество миллисекунд ожидания до истечения времени запроса к AI‑модели. |
| [getUrl()](#getUrl) | Получает URL модели. |
| [setTimeout(int value)](#setTimeout-int) | Устанавливает количество миллисекунд ожидания до истечения времени запроса к AI‑модели. |
| [setUrl(String value)](#setUrl-java.lang.String) | Устанавливает URL модели. |
| [summarize(Document doc)](#summarize-com.aspose.words.Document) |  |
| [summarize(Document doc, SummarizeOptions options)](#summarize-com.aspose.words.Document-com.aspose.words.SummarizeOptions) | Сводит указанный объект [Document](../../com.aspose.words/document/). |
| [summarize(Document[] docs)](#summarize-com.aspose.words.Document) |  |
| [summarize(Document[] docs, SummarizeOptions options)](#summarize-com.aspose.words.Document---com.aspose.words.SummarizeOptions) | Сводит указанные объекты [Document](../../com.aspose.words/document/). |
| [translate(Document doc, int language)](#translate-com.aspose.words.Document-int) |  |
| [withApiKey(String apiKey)](#withApiKey-java.lang.String) | Устанавливает указанный API‑ключ для модели. |
### GoogleAiModel(String name) {#GoogleAiModel-java.lang.String}
```
public GoogleAiModel(String name)
```


Инициализирует новый экземпляр класса [GoogleAiModel](../../com.aspose.words/googleaimodel/).

 **Examples:** 

Показывает, как использовать модель Google AI.

```

 String apiKey = System.getenv("API_KEY");
 GoogleAiModel model = new GoogleAiModel("gemini-flash-latest", apiKey);

 Document doc = new Document(getMyDir() + "Big document.docx");
 SummarizeOptions summarizeOptions = new SummarizeOptions(); { summarizeOptions.setSummaryLength(SummaryLength.VERY_SHORT); }
 Document summary = model.summarize(doc, summarizeOptions);
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | Имя модели. Например, gemini-2.5-flash. |

### GoogleAiModel(String name, String apiKey) {#GoogleAiModel-java.lang.String-java.lang.String}
```
public GoogleAiModel(String name, String apiKey)
```


Инициализирует новый экземпляр класса [GoogleAiModel](../../com.aspose.words/googleaimodel/).

 **Examples:** 

Показывает, как использовать модель Google AI.

```

 String apiKey = System.getenv("API_KEY");
 GoogleAiModel model = new GoogleAiModel("gemini-flash-latest", apiKey);

 Document doc = new Document(getMyDir() + "Big document.docx");
 SummarizeOptions summarizeOptions = new SummarizeOptions(); { summarizeOptions.setSummaryLength(SummaryLength.VERY_SHORT); }
 Document summary = model.summarize(doc, summarizeOptions);
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | Имя модели. Например, gemini-2.5-flash. |
| apiKey | java.lang.String | API‑ключ для использования Gemini API. Смотрите https://ai.google.dev/gemini-api/docs/api-key для деталей. |

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


Получает URL модели. Значение по умолчанию: "https://generativelanguage.googleapis.com/v1beta/models/".

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


Устанавливает URL модели. Значение по умолчанию: "https://generativelanguage.googleapis.com/v1beta/models/".

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | URL модели. |

### summarize(Document doc) {#summarize-com.aspose.words.Document}
```
public Document summarize(Document doc)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| doc | [Document](../../com.aspose.words/document/) |  |

**Returns:**
[Document](../../com.aspose.words/document/)
### summarize(Document doc, SummarizeOptions options) {#summarize-com.aspose.words.Document-com.aspose.words.SummarizeOptions}
```
public Document summarize(Document doc, SummarizeOptions options)
```


Сводит указанный объект [Document](../../com.aspose.words/document/).

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| doc | [Document](../../com.aspose.words/document/) |  |
| options | [SummarizeOptions](../../com.aspose.words/summarizeoptions/) |  |

**Returns:**
[Document](../../com.aspose.words/document/)
### summarize(Document[] docs) {#summarize-com.aspose.words.Document}
```
public Document summarize(Document[] docs)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| docs | [Document\[\]](../../com.aspose.words/document/) |  |

**Returns:**
[Document](../../com.aspose.words/document/)
### summarize(Document[] docs, SummarizeOptions options) {#summarize-com.aspose.words.Document---com.aspose.words.SummarizeOptions}
```
public Document summarize(Document[] docs, SummarizeOptions options)
```


Сводит указанные объекты [Document](../../com.aspose.words/document/).

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| docs | [Document\[\]](../../com.aspose.words/document/) |  |
| options | [SummarizeOptions](../../com.aspose.words/summarizeoptions/) |  |

**Returns:**
[Document](../../com.aspose.words/document/)
### translate(Document doc, int language) {#translate-com.aspose.words.Document-int}
```
public Document translate(Document doc, int language)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| doc | [Document](../../com.aspose.words/document/) |  |
| language | int |  |

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
