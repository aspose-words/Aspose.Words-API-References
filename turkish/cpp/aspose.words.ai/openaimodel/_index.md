---
title: "Aspose::Words::AI::OpenAiModel sınıfı"
linktitle: "OpenAiModel"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::AI::OpenAiModel sınıfı. Aspose.Words içinde OpenAi modellerinin entegrasyonunu temsil eden sınıf C++'da."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.ai/openaimodel/
---
## OpenAiModel class


Aspose.Words içinde OpenAi modellerinin entegrasyonunu temsil eden sınıf [Aspose.Words](../../aspose.words/).

```cpp
class OpenAiModel : public Aspose::Words::AI::AiModel
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| virtual [CheckGrammar](../aimodel/checkgrammar/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::CheckGrammarOptions\>) | Sağlanan belgenin dilbilgisini kontrol eder. Bu işlem, belgenin dilbilgisini kontrol etmek için bağlı [AI](../) modelini kullanır. |
| static [Create](../aimodel/create/)(Aspose::Words::AI::AiModelType) | [AiModel](../aimodel/) sınıfının yeni bir örneğini oluşturur. |
| [get_Timeout](../aimodel/get_timeout/)() const | [AI](../) modeline yapılan isteğin zaman aşımına uğramadan önce beklenecek milisaniye sayısını alır veya ayarlar. Varsayılan değer 100.000 milisaniyedir (100 saniye). |
| [get_Url](./get_url/)() override | Modelin URL'sini alır. Varsayılan değer "https://api.openai.com/". |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [OpenAiModel](./openaimodel/)(const System::String\&, const System::String\&) | [OpenAiModel](./) sınıfının yeni bir örneğini başlatır. |
| [OpenAiModel](./openaimodel/)(const System::String\&) | [OpenAiModel](./) sınıfının yeni bir örneğini başlatır. |
| [set_Timeout](../aimodel/set_timeout/)(int32_t) | [Aspose::Words::AI::AiModel::get_Timeout](../aimodel/get_timeout/) için ayarlayıcı. |
| [set_Url](./set_url/)(System::String) override | Modelin URL'sini ayarlar. Varsayılan değer "https://api.openai.com/". |
| [Summarize](./summarize/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) override | Belirtilen belgenin özetini oluşturur, özetin uzunluğunu ayarlama seçenekleriyle. Bu işlem, içerik işleme için bağlı [AI](../) modelini kullanır. |
| [Summarize](./summarize/)(System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) override | Belge dizisi için özetler oluşturur, özet uzunluğunu ve diğer ayarları kontrol etme seçenekleriyle. Bu yöntem, dizi içindeki her belgeyi işlemek için bağlı [AI](../) modelini kullanır. |
| [Translate](./translate/)(System::SharedPtr\<Aspose::Words::Document\>, Aspose::Words::AI::Language) override | Sağlanan belgeyi belirtilen hedef dile çevirir. Bu işlem, içerik çevirisi için bağlı [AI](../) modelini kullanır. |
| static [Type](./type/)() |  |
| [WithApiKey](../aimodel/withapikey/)(const System::String\&) | Model için belirtilen API anahtarını ayarlar. |
| [WithOrganization](./withorganization/)(const System::String\&) | Model için belirtilen Organizasyonu ayarlar. |
| [WithProject](./withproject/)(const System::String\&) | Model için belirtilen Projeyi ayarlar. |

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

* Class [AiModel](../aimodel/)
* Namespace [Aspose::Words::AI](../)
* Library [Aspose.Words for C++](../../)
