---
title: "AnthropicAiModel"
linktitle: "AnthropicAiModel"
second_title: "Aspose.Words Java için"
description: "Java'daki Aspose.Words içinde Anthropicu2019'un AI modelleriyle entegrasyonu temsil eden soyut bir sınıf."
type: docs
weight: 16
url: /tr/java/com.aspose.words/anthropicaimodel/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.AiModel](../../com.aspose.words/aimodel/)
```
public abstract class AnthropicAiModel extends AiModel
```

Anthropic’in AI modelleriyle entegrasyonu temsil eden soyut bir sınıf Aspose.Words içinde.
## Yapıcılar

| Yapıcı | Açıklama |
| --- | --- |
| [AnthropicAiModel()](#AnthropicAiModel) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [checkGrammar(Document sourceDocument, CheckGrammarOptions options)](#checkGrammar-com.aspose.words.Document-com.aspose.words.CheckGrammarOptions) | Sağlanan belgenin dilbilgisini kontrol eder. |
| [create(int modelType)](#create-int) |  |
| [getTimeout()](#getTimeout) | AI modeline yapılan isteğin zaman aşımına uğramadan önce beklenmesi gereken milisaniye sayısını alır. |
| [getUrl()](#getUrl) | Modelin URL'sini alır. |
| [setTimeout(int value)](#setTimeout-int) | AI modeline yapılan isteğin zaman aşımına uğramadan önce beklenmesi gereken milisaniye sayısını ayarlar. |
| [setUrl(String value)](#setUrl-java.lang.String) | Modelin URL'sini ayarlar. |
| [summarize(Document sourceDocument)](#summarize-com.aspose.words.Document) |  |
| [summarize(Document sourceDocument, SummarizeOptions options)](#summarize-com.aspose.words.Document-com.aspose.words.SummarizeOptions) | Belirtilen belgenin özetini oluşturur, özetin uzunluğunu ayarlama seçenekleriyle. |
| [summarize(Document[] sourceDocuments)](#summarize-com.aspose.words.Document) |  |
| [summarize(Document[] sourceDocuments, SummarizeOptions options)](#summarize-com.aspose.words.Document---com.aspose.words.SummarizeOptions) | Bir dizi belge için özetler oluşturur, özet uzunluğunu ve diğer ayarları kontrol etme seçenekleriyle. |
| [translate(Document sourceDocument, int targetLanguage)](#translate-com.aspose.words.Document-int) |  |
| [withApiKey(String apiKey)](#withApiKey-java.lang.String) | Model için belirtilen API anahtarını ayarlar. |
### AnthropicAiModel() {#AnthropicAiModel}
```
public AnthropicAiModel()
```


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


Modelin URL'sini alır. Varsayılan değer "https://api.anthropic.com/".

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


Modelin URL'sini ayarlar. Varsayılan değer "https://api.anthropic.com/".

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | Modelin bir URL'si. |

### summarize(Document sourceDocument) {#summarize-com.aspose.words.Document}
```
public Document summarize(Document sourceDocument)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| sourceDocument | [Document](../../com.aspose.words/document/) |  |

**Returns:**
[Document](../../com.aspose.words/document/)
### summarize(Document sourceDocument, SummarizeOptions options) {#summarize-com.aspose.words.Document-com.aspose.words.SummarizeOptions}
```
public Document summarize(Document sourceDocument, SummarizeOptions options)
```


Belirtilen belgenin özetini oluşturur, özetin uzunluğunu ayarlama seçenekleriyle. Bu işlem, içerik işleme için bağlı AI modelini kullanır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| sourceDocument | [Document](../../com.aspose.words/document/) | Özetlenecek belge. |
| options | [SummarizeOptions](../../com.aspose.words/summarizeoptions/) | Özet uzunluğunu ve diğer parametreleri kontrol eden isteğe bağlı ayarlar. |

**Returns:**
[Document](../../com.aspose.words/document/) - A summarized version of the document's content.
### summarize(Document[] sourceDocuments) {#summarize-com.aspose.words.Document}
```
public Document summarize(Document[] sourceDocuments)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| sourceDocuments | [Document\[\]](../../com.aspose.words/document/) |  |

**Returns:**
[Document](../../com.aspose.words/document/)
### summarize(Document[] sourceDocuments, SummarizeOptions options) {#summarize-com.aspose.words.Document---com.aspose.words.SummarizeOptions}
```
public Document summarize(Document[] sourceDocuments, SummarizeOptions options)
```


Bir dizi belge için özetler oluşturur, özet uzunluğunu ve diğer ayarları kontrol etme seçenekleriyle. Bu yöntem, dizideki her belgeyi işlemek için bağlı AI modelini kullanır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| sourceDocuments | [Document\[\]](../../com.aspose.words/document/) | Özetlenecek belgeler dizisi. |
| options | [SummarizeOptions](../../com.aspose.words/summarizeoptions/) | Özet uzunluğunu ve diğer parametreleri kontrol eden isteğe bağlı ayarlar |

**Returns:**
[Document](../../com.aspose.words/document/) - A summarized version of the document's content.
### translate(Document sourceDocument, int targetLanguage) {#translate-com.aspose.words.Document-int}
```
public Document translate(Document sourceDocument, int targetLanguage)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| sourceDocument | [Document](../../com.aspose.words/document/) |  |
| targetLanguage | int |  |

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
