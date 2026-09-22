---
title: "AnthropicAiModel"
linktitle: "AnthropicAiModel"
second_title: "Aspose.Words لـ Java"
description: "فئة مجردة تمثل التكامل مع نماذج AI الخاصة بـ Anthropicu2019 ضمن Aspose.Words في Java."
type: docs
weight: 16
url: /ar/java/com.aspose.words/anthropicaimodel/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.AiModel](../../com.aspose.words/aimodel/)
```
public abstract class AnthropicAiModel extends AiModel
```

فئة تجريدية تمثل التكامل مع نماذج الذكاء الاصطناعي الخاصة بـ Anthropic\u2019s ضمن Aspose.Words.
## المنشئات

| المنشئ | الوصف |
| --- | --- |
| [AnthropicAiModel()](#AnthropicAiModel) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [checkGrammar(Document sourceDocument, CheckGrammarOptions options)](#checkGrammar-com.aspose.words.Document-com.aspose.words.CheckGrammarOptions) | يتحقق من قواعد اللغة في المستند المقدم. |
| [create(int modelType)](#create-int) |  |
| [getTimeout()](#getTimeout) | يحصل على عدد المللي ثانية للانتظار قبل أن ينتهي مهلة الطلب إلى نموذج AI. |
| [getUrl()](#getUrl) | يحصل على عنوان URL للنموذج. |
| [setTimeout(int value)](#setTimeout-int) | يضبط عدد المللي ثانية للانتظار قبل أن ينتهي مهلة الطلب إلى نموذج AI. |
| [setUrl(String value)](#setUrl-java.lang.String) | يضبط عنوان URL للنموذج. |
| [summarize(Document sourceDocument)](#summarize-com.aspose.words.Document) |  |
| [summarize(Document sourceDocument, SummarizeOptions options)](#summarize-com.aspose.words.Document-com.aspose.words.SummarizeOptions) | ينشئ ملخصًا للمستند المحدد، مع خيارات لضبط طول الملخص. |
| [summarize(Document[] sourceDocuments)](#summarize-com.aspose.words.Document) |  |
| [summarize(Document[] sourceDocuments, SummarizeOptions options)](#summarize-com.aspose.words.Document---com.aspose.words.SummarizeOptions) | ينشئ ملخصات لمجموعة من المستندات، مع خيارات للتحكم في طول الملخص وإعدادات أخرى. |
| [translate(Document sourceDocument, int targetLanguage)](#translate-com.aspose.words.Document-int) |  |
| [withApiKey(String apiKey)](#withApiKey-java.lang.String) | يضبط مفتاح API المحدد للنموذج. |
### AnthropicAiModel() {#AnthropicAiModel}
```
public AnthropicAiModel()
```


### checkGrammar(Document sourceDocument, CheckGrammarOptions options) {#checkGrammar-com.aspose.words.Document-com.aspose.words.CheckGrammarOptions}
```
public Document checkGrammar(Document sourceDocument, CheckGrammarOptions options)
```


يتحقق من قواعد اللغة في المستند المقدم. تستفيد هذه العملية من نموذج الذكاء الاصطناعي المتصل للتحقق من قواعد اللغة في المستند.

 **Examples:** 

يوضح كيفية فحص قواعد اللغة لمستند.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| sourceDocument | [Document](../../com.aspose.words/document/) | المستند الذي يتم التحقق من قواعد لغته. |
| options | [CheckGrammarOptions](../../com.aspose.words/checkgrammaroptions/) | إعدادات اختيارية للتحكم في طريقة التحقق من القواعد. |

**Returns:**
[Document](../../com.aspose.words/document/) - A new [Document](../../com.aspose.words/document/) with checked grammar.
### create(int modelType) {#create-int}
```
public static AiModel create(int modelType)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| modelType | int |  |

**Returns:**
[AiModel](../../com.aspose.words/aimodel/)
### getTimeout() {#getTimeout}
```
public int getTimeout()
```


يحصل على عدد الملليثانية التي يجب الانتظار قبل انتهاء مهلة الطلب إلى نموذج الذكاء الاصطناعي. القيمة الافتراضية هي 100,000 ملليثانية (100 ثانية).

 **Examples:** 

يعرض كيفية تغيير المهلة الافتراضية للنموذج.

```

 String apiKey = System.getenv("API_KEY");
 AiModel model = AiModel.create(AiModelType.GPT_4_O_MINI).withApiKey(apiKey);
 // Default value 100000ms.
 model.setTimeout(250000);
 
```

**Returns:**
int - عدد الملليثانية التي يجب الانتظار قبل انتهاء مهلة الطلب إلى نموذج الذكاء الاصطناعي.
### getUrl() {#getUrl}
```
public String getUrl()
```


يحصل على عنوان URL للنموذج. القيمة الافتراضية هي "https://api.anthropic.com/".

**Returns:**
java.lang.String - عنوان URL للنموذج.
### setTimeout(int value) {#setTimeout-int}
```
public void setTimeout(int value)
```


يضبط عدد الملليثانية التي يجب الانتظار قبل انتهاء مهلة الطلب إلى نموذج الذكاء الاصطناعي. القيمة الافتراضية هي 100,000 ملليثانية (100 ثانية).

 **Examples:** 

يعرض كيفية تغيير المهلة الافتراضية للنموذج.

```

 String apiKey = System.getenv("API_KEY");
 AiModel model = AiModel.create(AiModelType.GPT_4_O_MINI).withApiKey(apiKey);
 // Default value 100000ms.
 model.setTimeout(250000);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | int | عدد الملليثانية التي يجب الانتظار قبل انتهاء مهلة الطلب إلى نموذج الذكاء الاصطناعي. |

### setUrl(String value) {#setUrl-java.lang.String}
```
public void setUrl(String value)
```


يضبط عنوان URL للنموذج. القيمة الافتراضية هي "https://api.anthropic.com/".

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | عنوان URL للنموذج. |

### summarize(Document sourceDocument) {#summarize-com.aspose.words.Document}
```
public Document summarize(Document sourceDocument)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| sourceDocument | [Document](../../com.aspose.words/document/) |  |

**Returns:**
[Document](../../com.aspose.words/document/)
### summarize(Document sourceDocument, SummarizeOptions options) {#summarize-com.aspose.words.Document-com.aspose.words.SummarizeOptions}
```
public Document summarize(Document sourceDocument, SummarizeOptions options)
```


ينشئ ملخصًا للمستند المحدد، مع خيارات لضبط طول الملخص. تستفيد هذه العملية من نموذج الذكاء الاصطناعي المتصل لمعالجة المحتوى.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| sourceDocument | [Document](../../com.aspose.words/document/) | المستند الذي سيُملَّخ. |
| options | [SummarizeOptions](../../com.aspose.words/summarizeoptions/) | إعدادات اختيارية للتحكم في طول الملخص ومعلمات أخرى. |

**Returns:**
[Document](../../com.aspose.words/document/) - A summarized version of the document's content.
### summarize(Document[] sourceDocuments) {#summarize-com.aspose.words.Document}
```
public Document summarize(Document[] sourceDocuments)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| sourceDocuments | [Document\[\]](../../com.aspose.words/document/) |  |

**Returns:**
[Document](../../com.aspose.words/document/)
### summarize(Document[] sourceDocuments, SummarizeOptions options) {#summarize-com.aspose.words.Document---com.aspose.words.SummarizeOptions}
```
public Document summarize(Document[] sourceDocuments, SummarizeOptions options)
```


ينشئ ملخصات لمجموعة من المستندات، مع خيارات للتحكم في طول الملخص وإعدادات أخرى. تستخدم هذه الطريقة نموذج الذكاء الاصطناعي المتصل لمعالجة كل مستند في المجموعة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| sourceDocuments | [Document\[\]](../../com.aspose.words/document/) | مجموعة من المستندات التي سيتم تلخيصها. |
| options | [SummarizeOptions](../../com.aspose.words/summarizeoptions/) | إعدادات اختيارية للتحكم في طول الملخص ومعلمات أخرى |

**Returns:**
[Document](../../com.aspose.words/document/) - A summarized version of the document's content.
### translate(Document sourceDocument, int targetLanguage) {#translate-com.aspose.words.Document-int}
```
public Document translate(Document sourceDocument, int targetLanguage)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| sourceDocument | [Document](../../com.aspose.words/document/) |  |
| targetLanguage | int |  |

**Returns:**
[Document](../../com.aspose.words/document/)
### withApiKey(String apiKey) {#withApiKey-java.lang.String}
```
public AiModel withApiKey(String apiKey)
```


يضبط مفتاح API المحدد للنموذج.

 **Examples:** 

يظهر كيفية تلخيص النص باستخدام نماذج OpenAI وGoogle.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| apiKey | java.lang.String |  |

**Returns:**
[AiModel](../../com.aspose.words/aimodel/)
