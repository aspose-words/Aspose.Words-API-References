---
title: IAiModelText.Translate
linktitle: Translate
articleTitle: Translate
second_title: .NET için Aspose.Words
description: IAiModelText Translate yöntemimizle belgeleri zahmetsizce çevirin. İstediğiniz dilde doğru ve hızlı çeviriler için AI'dan yararlanın.
type: docs
weight: 30
url: /tr/net/aspose.words.ai/iaimodeltext/translate/
---
## IAiModelText.Translate method

Sağlanan belgeyi belirtilen hedef dile çevirir. Bu işlem, içerik çevirisi için bağlı AI modelinden yararlanır.

```csharp
public Document Translate(Document sourceDocument, Language targetLanguage)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| sourceDocument | Document | Tercüme edilecek belge. |
| targetLanguage | Language | Belgenin çevrileceği dil. |

### Geri dönüş değeri

Yeni bir[`Document`](../../../aspose.words/document/)çevrilmiş belgeyi içeren nesne.

## Örnekler

Google modelleri kullanılarak metnin nasıl çevrileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Document.docx");

string apiKey = Environment.GetEnvironmentVariable("API_KEY");
// Google üretici dil modellerini kullanın.
IAiModelText model = (GoogleAiModel)AiModel.Create(AiModelType.Gemini15Flash).WithApiKey(apiKey);

Document translatedDoc = model.Translate(doc, Language.Arabic);
translatedDoc.Save(ArtifactsDir + "AI.AiTranslate.docx");
```

### Ayrıca bakınız

* class [Document](../../../aspose.words/document/)
* enum [Language](../../language/)
* interface [IAiModelText](../)
* ad alanı [Aspose.Words.AI](../../../aspose.words.ai/)
* toplantı [Aspose.Words](../../../)
