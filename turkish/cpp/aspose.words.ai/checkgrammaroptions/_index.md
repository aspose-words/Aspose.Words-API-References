---
title: "Aspose::Words::AI::CheckGrammarOptions sınıfı"
linktitle: "CheckGrammarOptions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::AI::CheckGrammarOptions sınıfı. AI kullanarak C++'ta bir belgenin dilbilgisini kontrol ederken çeşitli seçenekleri belirtmeye olanak tanır."
type: docs
weight: 1500
url: /tr/cpp/aspose.words.ai/checkgrammaroptions/
---
## CheckGrammarOptions class


Bir belgeyi [AI](../) kullanarak dilbilgisi kontrol ederken çeşitli seçenekleri belirtmeye olanak tanır.

```cpp
class CheckGrammarOptions : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [CheckGrammarOptions](./checkgrammaroptions/)() |  |
| [get_ImproveStylistics](./get_improvestylistics/)() const | İncelenen metnin stilini iyileştirmeye çalışacak [AI](../) belirtmeye olanak tanır. Varsayılan değer **false**. |
| [get_MakeRevisions](./get_makerevisions/)() const | Düzeltme yapılmış metinle birlikte döndürülecek son veya revize edilmiş belgeyi belirtmeye olanak tanır. Varsayılan değer **false**. |
| [get_PreserveFormatting](./get_preserveformatting/)() const | Orijinal belgenin düzenini ve biçimlendirmesini korumaya çalışacak [CheckGrammar()](../aimodel/checkgrammar/) belirtmeye olanak tanır, ya da çalışmasın. Varsayılan değer **true**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ImproveStylistics](./set_improvestylistics/)(bool) | İncelenen metnin stilini iyileştirmeye çalışacak [AI](../) belirtmeye olanak tanır. Varsayılan değer **false**. |
| [set_MakeRevisions](./set_makerevisions/)(bool) | Düzeltme yapılmış metinle birlikte döndürülecek son veya revize edilmiş belgeyi belirtmeye olanak tanır. Varsayılan değer **false**. |
| [set_PreserveFormatting](./set_preserveformatting/)(bool) | Orijinal belgenin düzenini ve biçimlendirmesini korumaya çalışacak [CheckGrammar()](../aimodel/checkgrammar/) belirtmeye olanak tanır, ya da çalışmasın. Varsayılan değer **true**. |
| static [Type](./type/)() |  |

## Örnekler



Bir belgenin dilbilgisini nasıl kontrol edeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
// OpenAI üretken dil modellerini kullanın.
System::SharedPtr<Aspose::Words::AI::AiModel> model = Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::Gpt4OMini)->WithApiKey(apiKey);

auto grammarOptions = System::MakeObject<Aspose::Words::AI::CheckGrammarOptions>();
grammarOptions->set_ImproveStylistics(true);

System::SharedPtr<Aspose::Words::Document> proofedDoc = model->CheckGrammar(doc, grammarOptions);
proofedDoc->Save(get_ArtifactsDir() + u"AI.AiGrammar.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::AI](../)
* Library [Aspose.Words for C++](../../)
