---
title: IAiModelText.CheckGrammar
linktitle: CheckGrammar
articleTitle: CheckGrammar
second_title: .NET için Aspose.Words
description: Yazınızı IAiModelText'in CheckGrammar yöntemi ile geliştirin. Gelişmiş AI dilbilgisi denetimini kullanarak belge doğruluğunu zahmetsizce iyileştirin.
type: docs
weight: 10
url: /tr/net/aspose.words.ai/iaimodeltext/checkgrammar/
---
## IAiModelText.CheckGrammar method

Sağlanan belgenin dilbilgisini kontrol eder. Bu işlem, belgenin dilbilgisini kontrol etmek için bağlı AI modelini kullanır.

```csharp
public Document CheckGrammar(Document sourceDocument, CheckGrammarOptions options = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| sourceDocument | Document | Dilbilgisi açısından kontrol edilen belge. |
| options | CheckGrammarOptions | Dilbilgisinin nasıl denetleneceğini kontrol etmek için isteğe bağlı ayarlar. |

### Geri dönüş değeri

Yeni bir[`Document`](../../../aspose.words/document/) dilbilgisi kontrol edilerek.

## Örnekler

Bir belgenin dilbilgisinin nasıl kontrol edileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

string apiKey = Environment.GetEnvironmentVariable("API_KEY");
// OpenAI üretken dil modellerini kullanın.
IAiModelText model = (OpenAiModel)AiModel.Create(AiModelType.Gpt4OMini).WithApiKey(apiKey);

CheckGrammarOptions grammarOptions = new CheckGrammarOptions();
grammarOptions.ImproveStylistics = true;

Document proofedDoc = model.CheckGrammar(doc, grammarOptions);
proofedDoc.Save(ArtifactsDir + "AI.AiGrammar.docx");
```

### Ayrıca bakınız

* class [Document](../../../aspose.words/document/)
* class [CheckGrammarOptions](../../checkgrammaroptions/)
* interface [IAiModelText](../)
* ad alanı [Aspose.Words.AI](../../../aspose.words.ai/)
* toplantı [Aspose.Words](../../../)
