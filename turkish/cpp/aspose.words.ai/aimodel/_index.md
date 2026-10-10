---
title: "Aspose::Words::AI::AiModel sınıfı"
linktitle: "AiModel"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::AI::AiModel sınıfı. C++'daki Aspose.Words içinde çeşitli AI modelleriyle entegrasyonu temsil eden soyut bir sınıf."
type: docs
weight: 1000
url: /tr/cpp/aspose.words.ai/aimodel/
---
## AiModel class


Farklı [AI](../) modelleriyle entegrasyonu temsil eden soyut bir sınıf, [Aspose.Words](../../aspose.words/) içinde.

```cpp
class AiModel : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| virtual [CheckGrammar](./checkgrammar/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::CheckGrammarOptions\>) | Sağlanan belgenin dilbilgisini kontrol eder. Bu işlem, belgenin dilbilgisini kontrol etmek için bağlı [AI](../) modelini kullanır. |
| static [Create](./create/)(Aspose::Words::AI::AiModelType) | [AiModel](./) sınıfının yeni bir örneğini oluşturur. |
| [get_Timeout](./get_timeout/)() const | [AI](../) modeline yapılan isteğin zaman aşımına uğramadan önce beklenecek milisaniye sayısını alır veya ayarlar. Varsayılan değer 100.000 milisaniyedir (100 saniye). |
| virtual [get_Url](./get_url/)() | Modelin URL'sini alır veya ayarlar. Varsayılan değer model için özeldir. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Timeout](./set_timeout/)(int32_t) | [Aspose::Words::AI::AiModel::get_Timeout](./get_timeout/) için ayarlayıcı. |
| virtual [set_Url](./set_url/)(System::String) | [Aspose::Words::AI::AiModel::get_Url](./get_url/) için ayarlayıcı. |
| virtual [Summarize](./summarize/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) | Belirtilen belgenin özetini oluşturur, özetin uzunluğunu ayarlama seçenekleriyle. Bu işlem, içerik işleme için bağlı [AI](../) modelini kullanır. |
| virtual [Summarize](./summarize/)(System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) | Belge dizisi için özetler oluşturur, özet uzunluğunu ve diğer ayarları kontrol etme seçenekleriyle. Bu yöntem, dizi içindeki her belgeyi işlemek için bağlı [AI](../) modelini kullanır. |
| virtual [Translate](./translate/)(System::SharedPtr\<Aspose::Words::Document\>, Aspose::Words::AI::Language) | Sağlanan belgeyi belirtilen hedef dile çevirir. Bu işlem, içerik çevirisi için bağlı [AI](../) modelini kullanır. |
| static [Type](./type/)() |  |
| [WithApiKey](./withapikey/)(const System::String\&) | Model için belirtilen API anahtarını ayarlar. |

## Örnekler



OpenAI ve Google modellerini kullanarak metni nasıl özetleyeceğinizi gösterir.
```cpp
auto firstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");
auto secondDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
// OpenAI veya Google üretken dil modellerini kullanın.
System::SharedPtr<Aspose::Words::AI::AiModel> model = (System::ExplicitCast<Aspose::Words::AI::OpenAiModel>(Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::Gpt4OMini)->WithApiKey(apiKey)))->WithOrganization(u"Organization")->WithProject(u"Project");

auto options = System::MakeObject<Aspose::Words::AI::SummarizeOptions>();

options->set_SummaryLength(Aspose::Words::AI::SummaryLength::Short);
System::SharedPtr<Aspose::Words::Document> oneDocumentSummary = model->Summarize(firstDoc, options);
oneDocumentSummary->Save(get_ArtifactsDir() + u"AI.AiSummarize.One.docx");

options->set_SummaryLength(Aspose::Words::AI::SummaryLength::Long);
System::SharedPtr<Aspose::Words::Document> multiDocumentSummary = model->Summarize(System::MakeArray<System::SharedPtr<Aspose::Words::Document>>({firstDoc, secondDoc}), options);
multiDocumentSummary->Save(get_ArtifactsDir() + u"AI.AiSummarize.Multi.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::AI](../)
* Library [Aspose.Words for C++](../../)
