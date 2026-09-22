---
title: "Aspose::Words::AI::GoogleAiModel sınıfı"
linktitle: "GoogleAiModel"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::AI::GoogleAiModel sınıfı. Aspose.Words içinde Google AI Modelleri (Gemini) entegrasyonunu temsil eden sınıf C++'da."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.ai/googleaimodel/
---
## GoogleAiModel class


Google [AI](../) Modelleri (Gemini) entegrasyonunu temsil eden sınıf [Aspose.Words](../../aspose.words/).

```cpp
class GoogleAiModel : public Aspose::Words::AI::AiModel
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| virtual [CheckGrammar](../aimodel/checkgrammar/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::CheckGrammarOptions\>) | Sağlanan belgenin dilbilgisini kontrol eder. Bu işlem, belgenin dilbilgisini kontrol etmek için bağlı [AI](../) modelini kullanır. |
| static [Create](../aimodel/create/)(Aspose::Words::AI::AiModelType) | [AiModel](../aimodel/) sınıfının yeni bir örneğini oluşturur. |
| [get_Timeout](../aimodel/get_timeout/)() const | [AI](../) modeline yapılan isteğin zaman aşımına uğramadan önce beklenecek milisaniye sayısını alır veya ayarlar. Varsayılan değer 100.000 milisaniyedir (100 saniye). |
| [get_Url](./get_url/)() override | Modelin URL'sini alır. Varsayılan değer "https://generativelanguage.googleapis.com/v1beta/models/". |
| [GetType](./gettype/)() const override |  |
| [GoogleAiModel](./googleaimodel/)(const System::String\&) | [GoogleAiModel](./) sınıfının yeni bir örneğini başlatır. |
| [GoogleAiModel](./googleaimodel/)(const System::String\&, const System::String\&) | [GoogleAiModel](./) sınıfının yeni bir örneğini başlatır. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Timeout](../aimodel/set_timeout/)(int32_t) | [Aspose::Words::AI::AiModel::get_Timeout](../aimodel/get_timeout/) için ayarlayıcı. |
| [set_Url](./set_url/)(System::String) override | Modelin URL'sini ayarlar. Varsayılan değer "https://generativelanguage.googleapis.com/v1beta/models/". |
| [Summarize](./summarize/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) override | Belirtilen [Document](../../aspose.words/document/) nesnesini özetler. |
| [Summarize](./summarize/)(System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) override | Belirtilen [Document](../../aspose.words/document/) nesnelerini özetler. |
| [Translate](./translate/)(System::SharedPtr\<Aspose::Words::Document\>, Aspose::Words::AI::Language) override | Belirtilen bir belgeyi çevirir. |
| static [Type](./type/)() |  |
| [WithApiKey](../aimodel/withapikey/)(const System::String\&) | Model için belirtilen API anahtarını ayarlar. |

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


Google [AI](../) modelinin nasıl kullanılacağını gösterir.
```cpp
System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
auto model = System::MakeObject<Aspose::Words::AI::GoogleAiModel>(u"gemini-flash-latest", apiKey);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");
auto summarizeOptions = System::MakeObject<Aspose::Words::AI::SummarizeOptions>();
summarizeOptions->set_SummaryLength(Aspose::Words::AI::SummaryLength::VeryShort);
System::SharedPtr<Aspose::Words::Document> summary = model->Summarize(doc, summarizeOptions);
```

## Ayrıca Bakınız

* Class [AiModel](../aimodel/)
* Namespace [Aspose::Words::AI](../)
* Library [Aspose.Words for C++](../../)
