---
title: "GoogleAiModel"
linktitle: "GoogleAiModel"
second_title: "Aspose.Words لـ Java"
description: "فئة تمثل تكامل نماذج Google AI Gemini داخل Aspose.Words في Java."
type: docs
weight: 361
url: /ar/java/com.aspose.words/googleaimodel/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.AiModel](../../com.aspose.words/aimodel/)
```
public class GoogleAiModel extends AiModel
```

فئة تمثل تكامل نماذج Google AI (Gemini) داخل Aspose.Words.

 **Remarks:** 

يرجى الرجوع إلى https://ai.google.dev/gemini-api/docs/models للحصول على تفاصيل نماذج Gemini.

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

يظهر كيفية استخدام نموذج Google AI.

```

 String apiKey = System.getenv("API_KEY");
 GoogleAiModel model = new GoogleAiModel("gemini-flash-latest", apiKey);

 Document doc = new Document(getMyDir() + "Big document.docx");
 SummarizeOptions summarizeOptions = new SummarizeOptions(); { summarizeOptions.setSummaryLength(SummaryLength.VERY_SHORT); }
 Document summary = model.summarize(doc, summarizeOptions);
 
```
## المنشئات

| المنشئ | الوصف |
| --- | --- |
| [GoogleAiModel(String name)](#GoogleAiModel-java.lang.String) | يُنشئ مثيلًا جديدًا من الفئة [GoogleAiModel](../../com.aspose.words/googleaimodel/). |
| [GoogleAiModel(String name, String apiKey)](#GoogleAiModel-java.lang.String-java.lang.String) | يُنشئ مثيلًا جديدًا من الفئة [GoogleAiModel](../../com.aspose.words/googleaimodel/). |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [checkGrammar(Document sourceDocument, CheckGrammarOptions options)](#checkGrammar-com.aspose.words.Document-com.aspose.words.CheckGrammarOptions) | يتحقق من قواعد اللغة في المستند المقدم. |
| [create(int modelType)](#create-int) |  |
| [getTimeout()](#getTimeout) | يحصل على عدد المللي ثانية للانتظار قبل أن ينتهي مهلة الطلب إلى نموذج AI. |
| [getUrl()](#getUrl) | يحصل على عنوان URL للنموذج. |
| [setTimeout(int value)](#setTimeout-int) | يضبط عدد المللي ثانية للانتظار قبل أن ينتهي مهلة الطلب إلى نموذج AI. |
| [setUrl(String value)](#setUrl-java.lang.String) | يضبط عنوان URL للنموذج. |
| [summarize(Document doc)](#summarize-com.aspose.words.Document) |  |
| [summarize(Document doc, SummarizeOptions options)](#summarize-com.aspose.words.Document-com.aspose.words.SummarizeOptions) | يلخص كائن [Document](../../com.aspose.words/document/) المحدد. |
| [summarize(Document[] docs)](#summarize-com.aspose.words.Document) |  |
| [summarize(Document[] docs, SummarizeOptions options)](#summarize-com.aspose.words.Document---com.aspose.words.SummarizeOptions) | يلخص كائنات [Document](../../com.aspose.words/document/) المحددة. |
| [translate(Document doc, int language)](#translate-com.aspose.words.Document-int) |  |
| [withApiKey(String apiKey)](#withApiKey-java.lang.String) | يضبط مفتاح API المحدد للنموذج. |
### GoogleAiModel(String name) {#GoogleAiModel-java.lang.String}
```
public GoogleAiModel(String name)
```


يُنشئ مثيلًا جديدًا من الفئة [GoogleAiModel](../../com.aspose.words/googleaimodel/).

 **Examples:** 

يظهر كيفية استخدام نموذج Google AI.

```

 String apiKey = System.getenv("API_KEY");
 GoogleAiModel model = new GoogleAiModel("gemini-flash-latest", apiKey);

 Document doc = new Document(getMyDir() + "Big document.docx");
 SummarizeOptions summarizeOptions = new SummarizeOptions(); { summarizeOptions.setSummaryLength(SummaryLength.VERY_SHORT); }
 Document summary = model.summarize(doc, summarizeOptions);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| الاسم | java.lang.String | اسم النموذج. على سبيل المثال، gemini-2.5-flash. |

### GoogleAiModel(String name, String apiKey) {#GoogleAiModel-java.lang.String-java.lang.String}
```
public GoogleAiModel(String name, String apiKey)
```


يُنشئ مثيلًا جديدًا من الفئة [GoogleAiModel](../../com.aspose.words/googleaimodel/).

 **Examples:** 

يظهر كيفية استخدام نموذج Google AI.

```

 String apiKey = System.getenv("API_KEY");
 GoogleAiModel model = new GoogleAiModel("gemini-flash-latest", apiKey);

 Document doc = new Document(getMyDir() + "Big document.docx");
 SummarizeOptions summarizeOptions = new SummarizeOptions(); { summarizeOptions.setSummaryLength(SummaryLength.VERY_SHORT); }
 Document summary = model.summarize(doc, summarizeOptions);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| الاسم | java.lang.String | اسم النموذج. على سبيل المثال، gemini-2.5-flash. |
| apiKey | java.lang.String | مفتاح API لاستخدام Gemini API. يرجى الرجوع إلى https://ai.google.dev/gemini-api/docs/api-key للحصول على التفاصيل. |

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


يحصل على عنوان URL للنموذج. القيمة الافتراضية هي "https://generativelanguage.googleapis.com/v1beta/models/".

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


يضبط عنوان URL للنموذج. القيمة الافتراضية هي "https://generativelanguage.googleapis.com/v1beta/models/".

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | عنوان URL للنموذج. |

### summarize(Document doc) {#summarize-com.aspose.words.Document}
```
public Document summarize(Document doc)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| doc | [Document](../../com.aspose.words/document/) |  |

**Returns:**
[Document](../../com.aspose.words/document/)
### summarize(Document doc, SummarizeOptions options) {#summarize-com.aspose.words.Document-com.aspose.words.SummarizeOptions}
```
public Document summarize(Document doc, SummarizeOptions options)
```


يلخص كائن [Document](../../com.aspose.words/document/) المحدد.

**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| docs | [Document\[\]](../../com.aspose.words/document/) |  |

**Returns:**
[Document](../../com.aspose.words/document/)
### summarize(Document[] docs, SummarizeOptions options) {#summarize-com.aspose.words.Document---com.aspose.words.SummarizeOptions}
```
public Document summarize(Document[] docs, SummarizeOptions options)
```


يلخص كائنات [Document](../../com.aspose.words/document/) المحددة.

**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| doc | [Document](../../com.aspose.words/document/) |  |
| اللغة | int |  |

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
