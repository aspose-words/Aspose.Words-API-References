---
title: "Aspose::Words::AI::AiModel class"
linktitle: "AiModel"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::AI::AiModel class. En abstrakt klass som representerar integrationen med olika AI-modeller inom Aspose.Words i C++."
type: docs
weight: 1000
url: /sv/cpp/aspose.words.ai/aimodel/
---
## AiModel class


En abstrakt klass som representerar integrationen med olika [AI](../)-modeller inom [Aspose.Words](../../aspose.words/).

```cpp
class AiModel : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| virtual [CheckGrammar](./checkgrammar/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::CheckGrammarOptions\>) | Kontrollerar grammatiken i det angivna dokumentet. Denna operation utnyttjar den anslutna [AI](../)-modellen för att kontrollera dokumentets grammatik. |
| static [Create](./create/)(Aspose::Words::AI::AiModelType) | Skapar en ny instans av klassen [AiModel](./). |
| [get_Timeout](./get_timeout/)() const | Hämtar eller anger antalet millisekunder att vänta innan begäran till [AI](../)-modellen får timeout. Standardvärdet är 100 000 millisekunder (100 sekunder). |
| virtual [get_Url](./get_url/)() | Hämtar eller anger en URL för modellen. Standardvärdet är specifikt för modellen. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Timeout](./set_timeout/)(int32_t) | Sättare för [Aspose::Words::AI::AiModel::get_Timeout](./get_timeout/). |
| virtual [set_Url](./set_url/)(System::String) | Sättare för [Aspose::Words::AI::AiModel::get_Url](./get_url/). |
| virtual [Summarize](./summarize/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) | Genererar en sammanfattning av det angivna dokumentet, med alternativ för att justera sammanfattningens längd. Denna operation utnyttjar den anslutna [AI](../)-modellen för innehållsbehandling. |
| virtual [Summarize](./summarize/)(System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) | Genererar sammanfattningar för en matris av dokument, med alternativ för att styra sammanfattningens längd och andra inställningar. Denna metod använder den anslutna [AI](../)-modellen för att bearbeta varje dokument i matrisen. |
| virtual [Translate](./translate/)(System::SharedPtr\<Aspose::Words::Document\>, Aspose::Words::AI::Language) | Översätter det angivna dokumentet till det specificerade målspråket. Denna operation utnyttjar den anslutna [AI](../)-modellen för innehållsöversättning. |
| static [Type](./type/)() |  |
| [WithApiKey](./withapikey/)(const System::String\&) | Anger en specificerad API-nyckel för modellen. |

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

## Se även

* Namespace [Aspose::Words::AI](../)
* Library [Aspose.Words for C++](../../)
