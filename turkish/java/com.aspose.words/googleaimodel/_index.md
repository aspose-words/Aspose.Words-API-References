---
title: "GoogleAiModel"
linktitle: "GoogleAiModel"
second_title: "Aspose.Words Java için"
description: "Java'da Aspose.Words içinde Google AI Models Gemini entegrasyonunu temsil eden sınıf."
type: docs
weight: 361
url: /tr/java/com.aspose.words/googleaimodel/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.AiModel](../../com.aspose.words/aimodel/)
```
public class GoogleAiModel extends AiModel
```

Aspose.Words içinde Google AI Modelleri (Gemini) entegrasyonunu temsil eden sınıf.

 **Remarks:** 

Gemini modelleriyle ilgili ayrıntılar için https://ai.google.dev/gemini-api/docs/models adresine bakın.

 **Examples:** 

OpenAI ve Google modellerini kullanarak metni nasıl özetleyeceğinizi gösterir.

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

Google AI modelinin nasıl kullanılacağını gösterir.

```

 String apiKey = System.getenv("API_KEY");
 GoogleAiModel model = new GoogleAiModel("gemini-flash-latest", apiKey);

 Document doc = new Document(getMyDir() + "Big document.docx");
 SummarizeOptions summarizeOptions = new SummarizeOptions(); { summarizeOptions.setSummaryLength(SummaryLength.VERY_SHORT); }
 Document summary = model.summarize(doc, summarizeOptions);
 
```
## Yapıcılar

| Yapıcı | Açıklama |
| --- | --- |
| [GoogleAiModel(String name)](#GoogleAiModel-java.lang.String) | [GoogleAiModel](../../com.aspose.words/googleaimodel/) sınıfının yeni bir örneğini başlatır. |
| [GoogleAiModel(String name, String apiKey)](#GoogleAiModel-java.lang.String-java.lang.String) | [GoogleAiModel](../../com.aspose.words/googleaimodel/) sınıfının yeni bir örneğini başlatır. |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [checkGrammar(Document sourceDocument, CheckGrammarOptions options)](#checkGrammar-com.aspose.words.Document-com.aspose.words.CheckGrammarOptions) | Sağlanan belgenin dilbilgisini kontrol eder. |
| [create(int modelType)](#create-int) |  |
| [getTimeout()](#getTimeout) | AI modeline yapılan isteğin zaman aşımına uğramadan önce beklenmesi gereken milisaniye sayısını alır. |
| [getUrl()](#getUrl) | Modelin URL'sini alır. |
| [setTimeout(int value)](#setTimeout-int) | AI modeline yapılan isteğin zaman aşımına uğramadan önce beklenmesi gereken milisaniye sayısını ayarlar. |
| [setUrl(String value)](#setUrl-java.lang.String) | Modelin URL'sini ayarlar. |
| [summarize(Document doc)](#summarize-com.aspose.words.Document) |  |
| [summarize(Document doc, SummarizeOptions options)](#summarize-com.aspose.words.Document-com.aspose.words.SummarizeOptions) | Belirtilen [Document](../../com.aspose.words/document/) nesnesini özetler. |
| [summarize(Document[] docs)](#summarize-com.aspose.words.Document) |  |
| [summarize(Document[] docs, SummarizeOptions options)](#summarize-com.aspose.words.Document---com.aspose.words.SummarizeOptions) | Belirtilen [Document](../../com.aspose.words/document/) nesnelerini özetler. |
| [translate(Document doc, int language)](#translate-com.aspose.words.Document-int) |  |
| [withApiKey(String apiKey)](#withApiKey-java.lang.String) | Model için belirtilen API anahtarını ayarlar. |
### GoogleAiModel(String name) {#GoogleAiModel-java.lang.String}
```
public GoogleAiModel(String name)
```


[GoogleAiModel](../../com.aspose.words/googleaimodel/) sınıfının yeni bir örneğini başlatır.

 **Examples:** 

Google AI modelinin nasıl kullanılacağını gösterir.

```

 String apiKey = System.getenv("API_KEY");
 GoogleAiModel model = new GoogleAiModel("gemini-flash-latest", apiKey);

 Document doc = new Document(getMyDir() + "Big document.docx");
 SummarizeOptions summarizeOptions = new SummarizeOptions(); { summarizeOptions.setSummaryLength(SummaryLength.VERY_SHORT); }
 Document summary = model.summarize(doc, summarizeOptions);
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | java.lang.String | Modelin adı. Örneğin, gemini-2.5-flash. |

### GoogleAiModel(String name, String apiKey) {#GoogleAiModel-java.lang.String-java.lang.String}
```
public GoogleAiModel(String name, String apiKey)
```


[GoogleAiModel](../../com.aspose.words/googleaimodel/) sınıfının yeni bir örneğini başlatır.

 **Examples:** 

Google AI modelinin nasıl kullanılacağını gösterir.

```

 String apiKey = System.getenv("API_KEY");
 GoogleAiModel model = new GoogleAiModel("gemini-flash-latest", apiKey);

 Document doc = new Document(getMyDir() + "Big document.docx");
 SummarizeOptions summarizeOptions = new SummarizeOptions(); { summarizeOptions.setSummaryLength(SummaryLength.VERY_SHORT); }
 Document summary = model.summarize(doc, summarizeOptions);
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | java.lang.String | Modelin adı. Örneğin, gemini-2.5-flash. |
| apiKey | java.lang.String | Gemini API'sini kullanmak için API anahtarı. Ayrıntılar için https://ai.google.dev/gemini-api/docs/api-key adresine bakın. |

### checkGrammar(Document sourceDocument, CheckGrammarOptions options) {#checkGrammar-com.aspose.words.Document-com.aspose.words.CheckGrammarOptions}
```
public Document checkGrammar(Document sourceDocument, CheckGrammarOptions options)
```


Sağlanan belgenin dilbilgisini kontrol eder. Bu işlem, belgenin dilbilgisini kontrol etmek için bağlı AI modelini kullanır.

 **Examples:** 

Bir belgenin dilbilgisinin nasıl kontrol edileceğini gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| sourceDocument | [Document](../../com.aspose.words/document/) | Dilbilgisi kontrolü yapılan belge. |
| options | [CheckGrammarOptions](../../com.aspose.words/checkgrammaroptions/) | Dilbilgisinin nasıl kontrol edileceğini belirleyen isteğe bağlı ayarlar. |

**Returns:**
[Document](../../com.aspose.words/document/) - A new [Document](../../com.aspose.words/document/) with checked grammar.
### create(int modelType) {#create-int}
```
public static AiModel create(int modelType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| modelType | int |  |

**Returns:**
[AiModel](../../com.aspose.words/aimodel/)
### getTimeout() {#getTimeout}
```
public int getTimeout()
```


AI modeline yapılan isteğin zaman aşımına uğramadan önce beklenmesi gereken milisaniye sayısını alır. Varsayılan değer 100.000 milisaniyedir (100 saniye).

 **Examples:** 

Modelin varsayılan zaman aşımının nasıl değiştirileceğini gösterir.

```

 String apiKey = System.getenv("API_KEY");
 AiModel model = AiModel.create(AiModelType.GPT_4_O_MINI).withApiKey(apiKey);
 // Default value 100000ms.
 model.setTimeout(250000);
 
```

**Returns:**
int - AI modeline yapılan isteğin zaman aşımına uğramadan önce beklenmesi gereken milisaniye sayısı.
### getUrl() {#getUrl}
```
public String getUrl()
```


Modelin URL'sini alır. Varsayılan değer "https://generativelanguage.googleapis.com/v1beta/models/".

**Returns:**
java.lang.String - Modelin bir URL'si.
### setTimeout(int value) {#setTimeout-int}
```
public void setTimeout(int value)
```


AI modeline yapılan isteğin zaman aşımına uğramadan önce beklenmesi gereken milisaniye sayısını ayarlar. Varsayılan değer 100.000 milisaniyedir (100 saniye).

 **Examples:** 

Modelin varsayılan zaman aşımının nasıl değiştirileceğini gösterir.

```

 String apiKey = System.getenv("API_KEY");
 AiModel model = AiModel.create(AiModelType.GPT_4_O_MINI).withApiKey(apiKey);
 // Default value 100000ms.
 model.setTimeout(250000);
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | int | AI modeline yapılan isteğin zaman aşımına uğramadan önce beklenmesi gereken milisaniye sayısı. |

### setUrl(String value) {#setUrl-java.lang.String}
```
public void setUrl(String value)
```


Modelin URL'sini ayarlar. Varsayılan değer "https://generativelanguage.googleapis.com/v1beta/models/".

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | Modelin bir URL'si. |

### summarize(Document doc) {#summarize-com.aspose.words.Document}
```
public Document summarize(Document doc)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| doc | [Document](../../com.aspose.words/document/) |  |

**Returns:**
[Document](../../com.aspose.words/document/)
### summarize(Document doc, SummarizeOptions options) {#summarize-com.aspose.words.Document-com.aspose.words.SummarizeOptions}
```
public Document summarize(Document doc, SummarizeOptions options)
```


Belirtilen [Document](../../com.aspose.words/document/) nesnesini özetler.

**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| docs | [Document\[\]](../../com.aspose.words/document/) |  |

**Returns:**
[Document](../../com.aspose.words/document/)
### summarize(Document[] docs, SummarizeOptions options) {#summarize-com.aspose.words.Document---com.aspose.words.SummarizeOptions}
```
public Document summarize(Document[] docs, SummarizeOptions options)
```


Belirtilen [Document](../../com.aspose.words/document/) nesnelerini özetler.

**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| doc | [Document](../../com.aspose.words/document/) |  |
| dil | int |  |

**Returns:**
[Document](../../com.aspose.words/document/)
### withApiKey(String apiKey) {#withApiKey-java.lang.String}
```
public AiModel withApiKey(String apiKey)
```


Model için belirtilen API anahtarını ayarlar.

 **Examples:** 

OpenAI ve Google modellerini kullanarak metni nasıl özetleyeceğinizi gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| apiKey | java.lang.String |  |

**Returns:**
[AiModel](../../com.aspose.words/aimodel/)
