---
title: "SummarizeOptions"
linktitle: "SummarizeOptions"
second_title: "Aspose.Words Java için"
description: "Java'da belge içeriğini özetlemek için çeşitli seçenekleri belirtmeye olanak tanır."
type: docs
weight: 646
url: /tr/java/com.aspose.words/summarizeoptions/
---

**Inheritance:**
java.lang.Object
```
public class SummarizeOptions
```

Belge içeriğini özetlemek için çeşitli seçenekleri belirtmeye izin verir.

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
## Yapıcılar

| Yapıcı | Açıklama |
| --- | --- |
| [SummarizeOptions()](#SummarizeOptions) | Yeni bir [SummarizeOptions](../../com.aspose.words/summarizeoptions/) sınıfı örneği başlatır. |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getSummaryLength()](#getSummaryLength) | Özet uzunluğunu belirtmeye olanak tanır. |
| [setSummaryLength(int value)](#setSummaryLength-int) | Özet uzunluğunu belirtmeye olanak tanır. |
### SummarizeOptions() {#SummarizeOptions}
```
public SummarizeOptions()
```


Yeni bir [SummarizeOptions](../../com.aspose.words/summarizeoptions/) sınıfı örneği başlatır.

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

### getSummaryLength() {#getSummaryLength}
```
public int getSummaryLength()
```


Özet uzunluğunu belirtmeye olanak tanır. Varsayılan değer [SummaryLength.MEDIUM](../../com.aspose.words/summarylength/\#MEDIUM)'dır.

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

**Returns:**
int - İlgili  int  değeri. Döndürülen değer [SummaryLength](../../com.aspose.words/summarylength/) sabitlerinden biridir.
### setSummaryLength(int value) {#setSummaryLength-int}
```
public void setSummaryLength(int value)
```


Özet uzunluğunu belirtmeye olanak tanır. Varsayılan değer [SummaryLength.MEDIUM](../../com.aspose.words/summarylength/\#MEDIUM)'dır.

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
| value | int | İlgili  int  değeri. Değer [SummaryLength](../../com.aspose.words/summarylength/) sabitlerinden biri olmalıdır. |

