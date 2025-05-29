---
title: CheckGrammarOptions Class
linktitle: CheckGrammarOptions
articleTitle: CheckGrammarOptions
second_title: .NET için Aspose.Words
description: Belgelerinizi Aspose.Words.AI.CheckGrammarOptions ile optimize edin. Kusursuz yazım ve gelişmiş netlik için özelleştirilebilir AI dilbilgisi kontrollerini keşfedin.
type: docs
weight: 50
url: /tr/net/aspose.words.ai/checkgrammaroptions/
---
## CheckGrammarOptions class

AI kullanılarak bir belgenin dilbilgisi kontrolü sırasında çeşitli seçeneklerin belirlenmesine olanak tanır.

```csharp
public class CheckGrammarOptions
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [CheckGrammarOptions](checkgrammaroptions/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [ImproveStylistics](../../aspose.words.ai/checkgrammaroptions/improvestylistics/) { get; set; } | AI'nın, düzeltilen metnin üslubunu iyileştirmeye çalışacağını belirtmenize olanak tanır. Varsayılan değer`YANLIŞ` . |
| [MakeRevisions](../../aspose.words.ai/checkgrammaroptions/makerevisions/) { get; set; } | Son veya revize edilmiş belgenin düzeltilmiş metinle birlikte iade edilmesini belirtmeye olanak tanır. Varsayılan değer`YANLIŞ` . |
| [PreserveFormatting](../../aspose.words.ai/checkgrammaroptions/preserveformatting/) { get; set; } | Aşağıdakileri belirtmenize olanak tanır:[`CheckGrammar`](../iaimodeltext/checkgrammar/)orijinal belgenin düzenini ve biçimlendirmesini korumaya çalışacak veya çalışmayacak. Varsayılan değer`doğru` . |

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

* ad alanı [Aspose.Words.AI](../../aspose.words.ai/)
* toplantı [Aspose.Words](../../)
