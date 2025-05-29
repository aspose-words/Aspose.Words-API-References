---
title: IAiModelText.Summarize
linktitle: Summarize
articleTitle: Summarize
second_title: .NET için Aspose.Words
description: IAiModelText ile belgeleri zahmetsizce özetleyin. Hassas içerik çıkarma ve gelişmiş okunabilirlik için gelişmiş AI kullanarak özet uzunluğunu özelleştirin.
type: docs
weight: 20
url: /tr/net/aspose.words.ai/iaimodeltext/summarize/
---
## Summarize(*[Document](../../../aspose.words/document/), [SummarizeOptions](../../summarizeoptions/)*) {#summarize}

Özetin uzunluğunu ayarlama seçenekleriyle belirtilen belgenin bir özetini oluşturur. Bu işlem, içerik işleme için bağlı AI modelini kullanır.

```csharp
public Document Summarize(Document sourceDocument, SummarizeOptions options = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| sourceDocument | Document | Özetlenecek belge. |
| options | SummarizeOptions | Özet uzunluğunu ve diğer parametreleri kontrol etmek için isteğe bağlı ayarlar. |

### Geri dönüş değeri

Belgenin içeriğinin özetlenmiş hali.

## Örnekler

OpenAI ve Google modelleri kullanılarak metnin nasıl özetleneceğini gösterir.

```csharp
Document firstDoc = new Document(MyDir + "Big document.docx");
Document secondDoc = new Document(MyDir + "Document.docx");

string apiKey = Environment.GetEnvironmentVariable("API_KEY");
// OpenAI veya Google üretici dil modellerini kullanın.
IAiModelText model = ((OpenAiModel)AiModel.Create(AiModelType.Gpt4OMini).WithApiKey(apiKey)).WithOrganization("Organization").WithProject("Project");

SummarizeOptions options = new SummarizeOptions();

options.SummaryLength = SummaryLength.Short;
Document oneDocumentSummary = model.Summarize(firstDoc, options);
oneDocumentSummary.Save(ArtifactsDir + "AI.AiSummarize.One.docx");

options.SummaryLength = SummaryLength.Long;
Document multiDocumentSummary = model.Summarize(new Document[] { firstDoc, secondDoc }, options);
multiDocumentSummary.Save(ArtifactsDir + "AI.AiSummarize.Multi.docx");
```

### Ayrıca bakınız

* class [Document](../../../aspose.words/document/)
* class [SummarizeOptions](../../summarizeoptions/)
* interface [IAiModelText](../)
* ad alanı [Aspose.Words.AI](../../../aspose.words.ai/)
* toplantı [Aspose.Words](../../../)

---

## Summarize(*Document[], [SummarizeOptions](../../summarizeoptions/)*) {#summarize_1}

Özet uzunluğunu ve diğer ayarları kontrol etme seçenekleriyle bir dizi belge için özetler üretir. Bu yöntem, dizideki her belgeyi işlemek için bağlı AI modelini kullanır.

```csharp
public Document Summarize(Document[] sourceDocuments, SummarizeOptions options = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| sourceDocuments | Document[] | Özetlenmesi gereken bir dizi belge. |
| options | SummarizeOptions | Özet uzunluğunu ve diğer parametreleri kontrol etmek için isteğe bağlı ayarlar |

### Geri dönüş değeri

Belgenin içeriğinin özetlenmiş hali.

## Örnekler

OpenAI ve Google modelleri kullanılarak metnin nasıl özetleneceğini gösterir.

```csharp
Document firstDoc = new Document(MyDir + "Big document.docx");
Document secondDoc = new Document(MyDir + "Document.docx");

string apiKey = Environment.GetEnvironmentVariable("API_KEY");
// OpenAI veya Google üretici dil modellerini kullanın.
IAiModelText model = ((OpenAiModel)AiModel.Create(AiModelType.Gpt4OMini).WithApiKey(apiKey)).WithOrganization("Organization").WithProject("Project");

SummarizeOptions options = new SummarizeOptions();

options.SummaryLength = SummaryLength.Short;
Document oneDocumentSummary = model.Summarize(firstDoc, options);
oneDocumentSummary.Save(ArtifactsDir + "AI.AiSummarize.One.docx");

options.SummaryLength = SummaryLength.Long;
Document multiDocumentSummary = model.Summarize(new Document[] { firstDoc, secondDoc }, options);
multiDocumentSummary.Save(ArtifactsDir + "AI.AiSummarize.Multi.docx");
```

### Ayrıca bakınız

* class [Document](../../../aspose.words/document/)
* class [SummarizeOptions](../../summarizeoptions/)
* interface [IAiModelText](../)
* ad alanı [Aspose.Words.AI](../../../aspose.words.ai/)
* toplantı [Aspose.Words](../../../)
