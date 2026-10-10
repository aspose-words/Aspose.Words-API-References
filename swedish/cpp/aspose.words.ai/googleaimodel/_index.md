---
title: "Aspose::Words::AI::GoogleAiModel class"
linktitle: "GoogleAiModel"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::AI::GoogleAiModel klass. Klass som representerar Google AI-modeller (Gemini) integration inom Aspose.Words i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.ai/googleaimodel/
---
## GoogleAiModel class


Klass som representerar Google [AI](../) modeller (Gemini) integration inom [Aspose.Words](../../aspose.words/).

```cpp
class GoogleAiModel : public Aspose::Words::AI::AiModel
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| virtual [CheckGrammar](../aimodel/checkgrammar/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::CheckGrammarOptions\>) | Kontrollerar grammatiken i det angivna dokumentet. Denna operation utnyttjar den anslutna [AI](../)-modellen för att kontrollera dokumentets grammatik. |
| static [Create](../aimodel/create/)(Aspose::Words::AI::AiModelType) | Skapar en ny instans av klassen [AiModel](../aimodel/). |
| [get_Timeout](../aimodel/get_timeout/)() const | Hämtar eller anger antalet millisekunder att vänta innan begäran till [AI](../)-modellen får timeout. Standardvärdet är 100 000 millisekunder (100 sekunder). |
| [get_Url](./get_url/)() override | Hämtar en URL för modellen. Standardvärdet är "https://generativelanguage.googleapis.com/v1beta/models/". |
| [GetType](./gettype/)() const override |  |
| [GoogleAiModel](./googleaimodel/)(const System::String\&) | Initierar en ny instans av [GoogleAiModel](./) klass. |
| [GoogleAiModel](./googleaimodel/)(const System::String\&, const System::String\&) | Initierar en ny instans av [GoogleAiModel](./) klass. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Timeout](../aimodel/set_timeout/)(int32_t) | Sättare för [Aspose::Words::AI::AiModel::get_Timeout](../aimodel/get_timeout/). |
| [set_Url](./set_url/)(System::String) override | Ställer in en URL för modellen. Standardvärdet är "https://generativelanguage.googleapis.com/v1beta/models/". |
| [Summarize](./summarize/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) override | Sammanfattar angivet [Document](../../aspose.words/document/) objekt. |
| [Summarize](./summarize/)(System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) override | Sammanfattar angivna [Document](../../aspose.words/document/) objekt. |
| [Translate](./translate/)(System::SharedPtr\<Aspose::Words::Document\>, Aspose::Words::AI::Language) override | Översätter ett angivet dokument. |
| static [Type](./type/)() |  |
| [WithApiKey](../aimodel/withapikey/)(const System::String\&) | Anger en specificerad API-nyckel för modellen. |

## Exempel



Visar hur man sammanfattar text med hjälp av OpenAI- och Google-modeller.
```cpp
auto firstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");
auto secondDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
// Använd generativa språkmodeller från OpenAI eller Google.
System::SharedPtr<Aspose::Words::AI::AiModel> model = (System::ExplicitCast<Aspose::Words::AI::OpenAiModel>(Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::Gpt4OMini)->WithApiKey(apiKey)))->WithOrganization(u"Organization")->WithProject(u"Project");

auto options = System::MakeObject<Aspose::Words::AI::SummarizeOptions>();

options->set_SummaryLength(Aspose::Words::AI::SummaryLength::Short);
System::SharedPtr<Aspose::Words::Document> oneDocumentSummary = model->Summarize(firstDoc, options);
oneDocumentSummary->Save(get_ArtifactsDir() + u"AI.AiSummarize.One.docx");

options->set_SummaryLength(Aspose::Words::AI::SummaryLength::Long);
System::SharedPtr<Aspose::Words::Document> multiDocumentSummary = model->Summarize(System::MakeArray<System::SharedPtr<Aspose::Words::Document>>({firstDoc, secondDoc}), options);
multiDocumentSummary->Save(get_ArtifactsDir() + u"AI.AiSummarize.Multi.docx");
```


Visar hur man använder Google [AI](../) modell.
```cpp
System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
auto model = System::MakeObject<Aspose::Words::AI::GoogleAiModel>(u"gemini-flash-latest", apiKey);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");
auto summarizeOptions = System::MakeObject<Aspose::Words::AI::SummarizeOptions>();
summarizeOptions->set_SummaryLength(Aspose::Words::AI::SummaryLength::VeryShort);
System::SharedPtr<Aspose::Words::Document> summary = model->Summarize(doc, summarizeOptions);
```

## Se även

* Class [AiModel](../aimodel/)
* Namespace [Aspose::Words::AI](../)
* Library [Aspose.Words for C++](../../)
