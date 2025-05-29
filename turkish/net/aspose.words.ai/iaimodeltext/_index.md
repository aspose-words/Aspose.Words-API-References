---
title: IAiModelText Interface
linktitle: IAiModelText
articleTitle: IAiModelText
second_title: .NET için Aspose.Words
description: Yapay zeka modelleri için çeşitli ve yüksek kaliteli metin içeriklerini zahmetsizce üreten çok yönlü arayüz Aspose.Words.AI.IAiModelText ile yaratıcı potansiyelinizi açığa çıkarın.
type: docs
weight: 70
url: /tr/net/aspose.words.ai/iaimodeltext/
---
## IAiModelText interface

Çeşitli metin tabanlı içerikler üretmek üzere tasarlanmış AI modelleri için ortak arayüz.

```csharp
public interface IAiModelText
```

## yöntemler

| İsim | Tanım |
| --- | --- |
| [CheckGrammar](../../aspose.words.ai/iaimodeltext/checkgrammar/)(*[Document](../../aspose.words/document/), [CheckGrammarOptions](../checkgrammaroptions/)*) | Sağlanan belgenin dilbilgisini kontrol eder. Bu işlem, belgenin dilbilgisini kontrol etmek için bağlı AI modelini kullanır. |
| [Summarize](../../aspose.words.ai/iaimodeltext/summarize/#summarize)(*[Document](../../aspose.words/document/), [SummarizeOptions](../summarizeoptions/)*) | Özetin uzunluğunu ayarlama seçenekleriyle belirtilen belgenin bir özetini oluşturur. Bu işlem, içerik işleme için bağlı AI modelini kullanır. |
| [Summarize](../../aspose.words.ai/iaimodeltext/summarize/#summarize_1)(*Document[], [SummarizeOptions](../summarizeoptions/)*) | Özet uzunluğunu ve diğer ayarları kontrol etme seçenekleriyle bir dizi belge için özetler üretir. Bu yöntem, dizideki her belgeyi işlemek için bağlı AI modelini kullanır. |
| [Translate](../../aspose.words.ai/iaimodeltext/translate/)(*[Document](../../aspose.words/document/), [Language](../language/)*) | Sağlanan belgeyi belirtilen hedef dile çevirir. Bu işlem, içerik çevirisi için bağlı AI modelinden yararlanır. |

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

* ad alanı [Aspose.Words.AI](../../aspose.words.ai/)
* toplantı [Aspose.Words](../../)
