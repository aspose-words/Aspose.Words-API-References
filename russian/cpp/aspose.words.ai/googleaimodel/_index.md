---
title: "Aspose::Words::AI::GoogleAiModel класс"
linktitle: "GoogleAiModel"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::AI::GoogleAiModel класс. Класс, представляющий интеграцию моделей Google AI (Gemini) в Aspose.Words на C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.ai/googleaimodel/
---
## GoogleAiModel class


Класс, представляющий интеграцию моделей Google [AI](../) (Gemini) в [Aspose.Words](../../aspose.words/).

```cpp
class GoogleAiModel : public Aspose::Words::AI::AiModel
```

## Методы

| Метод | Описание |
| --- | --- |
| virtual [CheckGrammar](../aimodel/checkgrammar/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::CheckGrammarOptions\>) | Проверяет грамматику предоставленного документа. Эта операция использует подключённую модель [AI](../) для проверки грамматики документа. |
| static [Create](../aimodel/create/)(Aspose::Words::AI::AiModelType) | Создаёт новый экземпляр класса [AiModel](../aimodel/). |
| [get_Timeout](../aimodel/get_timeout/)() const | Получает или задает количество миллисекунд ожидания до истечения тайм‑аута запроса к модели [AI](../). Значение по умолчанию — 100 000 миллисекунд (100 секунд). |
| [get_Url](./get_url/)() override | Получает URL модели. Значение по умолчанию — "https://generativelanguage.googleapis.com/v1beta/models/". |
| [GetType](./gettype/)() const override |  |
| [GoogleAiModel](./googleaimodel/)(const System::String\&) | Инициализирует новый экземпляр класса [GoogleAiModel](./). |
| [GoogleAiModel](./googleaimodel/)(const System::String\&, const System::String\&) | Инициализирует новый экземпляр класса [GoogleAiModel](./). |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Timeout](../aimodel/set_timeout/)(int32_t) | Сеттер для [Aspose::Words::AI::AiModel::get_Timeout](../aimodel/get_timeout/). |
| [set_Url](./set_url/)(System::String) override | Устанавливает URL модели. Значение по умолчанию — "https://generativelanguage.googleapis.com/v1beta/models/". |
| [Summarize](./summarize/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) override | Создаёт резюме указанного объекта [Document](../../aspose.words/document/). |
| [Summarize](./summarize/)(System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) override | Создаёт резюме указанных объектов [Document](../../aspose.words/document/). |
| [Translate](./translate/)(System::SharedPtr\<Aspose::Words::Document\>, Aspose::Words::AI::Language) override | Переводит указанный документ. |
| static [Type](./type/)() |  |
| [WithApiKey](../aimodel/withapikey/)(const System::String\&) | Задаёт указанный API‑ключ для модели. |

## Примеры



Показывает, как суммировать текст с использованием моделей OpenAI и Google.
```cpp
auto firstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");
auto secondDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
// Используйте генеративные языковые модели OpenAI или Google.
System::SharedPtr<Aspose::Words::AI::AiModel> model = (System::ExplicitCast<Aspose::Words::AI::OpenAiModel>(Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::Gpt4OMini)->WithApiKey(apiKey)))->WithOrganization(u"Organization")->WithProject(u"Project");

auto options = System::MakeObject<Aspose::Words::AI::SummarizeOptions>();

options->set_SummaryLength(Aspose::Words::AI::SummaryLength::Short);
System::SharedPtr<Aspose::Words::Document> oneDocumentSummary = model->Summarize(firstDoc, options);
oneDocumentSummary->Save(get_ArtifactsDir() + u"AI.AiSummarize.One.docx");

options->set_SummaryLength(Aspose::Words::AI::SummaryLength::Long);
System::SharedPtr<Aspose::Words::Document> multiDocumentSummary = model->Summarize(System::MakeArray<System::SharedPtr<Aspose::Words::Document>>({firstDoc, secondDoc}), options);
multiDocumentSummary->Save(get_ArtifactsDir() + u"AI.AiSummarize.Multi.docx");
```


Показывает, как использовать модель google [AI](../).
```cpp
System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
auto model = System::MakeObject<Aspose::Words::AI::GoogleAiModel>(u"gemini-flash-latest", apiKey);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");
auto summarizeOptions = System::MakeObject<Aspose::Words::AI::SummarizeOptions>();
summarizeOptions->set_SummaryLength(Aspose::Words::AI::SummaryLength::VeryShort);
System::SharedPtr<Aspose::Words::Document> summary = model->Summarize(doc, summarizeOptions);
```

## См. также

* Class [AiModel](../aimodel/)
* Namespace [Aspose::Words::AI](../)
* Library [Aspose.Words for C++](../../)
