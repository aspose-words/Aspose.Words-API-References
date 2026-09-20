---
title: "Aspose::Words::AI::OpenAiModel класс"
linktitle: "OpenAiModel"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::AI::OpenAiModel класс. Класс, представляющий интеграцию моделей OpenAi в Aspose.Words на C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.ai/openaimodel/
---
## OpenAiModel class


Класс, представляющий интеграцию моделей OpenAi в [Aspose.Words](../../aspose.words/).

```cpp
class OpenAiModel : public Aspose::Words::AI::AiModel
```

## Методы

| Метод | Описание |
| --- | --- |
| virtual [CheckGrammar](../aimodel/checkgrammar/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::CheckGrammarOptions\>) | Проверяет грамматику предоставленного документа. Эта операция использует подключённую модель [AI](../) для проверки грамматики документа. |
| static [Create](../aimodel/create/)(Aspose::Words::AI::AiModelType) | Создаёт новый экземпляр класса [AiModel](../aimodel/). |
| [get_Timeout](../aimodel/get_timeout/)() const | Получает или задает количество миллисекунд ожидания до истечения тайм‑аута запроса к модели [AI](../). Значение по умолчанию — 100 000 миллисекунд (100 секунд). |
| [get_Url](./get_url/)() override | Получает URL модели. Значение по умолчанию — "https://api.openai.com/". |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [OpenAiModel](./openaimodel/)(const System::String\&, const System::String\&) | Инициализирует новый экземпляр класса [OpenAiModel](./). |
| [OpenAiModel](./openaimodel/)(const System::String\&) | Инициализирует новый экземпляр класса [OpenAiModel](./). |
| [set_Timeout](../aimodel/set_timeout/)(int32_t) | Сеттер для [Aspose::Words::AI::AiModel::get_Timeout](../aimodel/get_timeout/). |
| [set_Url](./set_url/)(System::String) override | Устанавливает URL модели. Значение по умолчанию — "https://api.openai.com/". |
| [Summarize](./summarize/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) override | Создаёт резюме указанного документа с возможностью настройки длины резюме. Эта операция использует подключённую модель [AI](../) для обработки содержимого. |
| [Summarize](./summarize/)(System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) override | Создаёт резюме для массива документов с возможностью управления длиной резюме и другими параметрами. Этот метод использует подключённую модель [AI](../) для обработки каждого документа в массиве. |
| [Translate](./translate/)(System::SharedPtr\<Aspose::Words::Document\>, Aspose::Words::AI::Language) override | Переводит предоставленный документ на указанный целевой язык. Эта операция использует подключённую модель [AI](../) для перевода содержимого. |
| static [Type](./type/)() |  |
| [WithApiKey](../aimodel/withapikey/)(const System::String\&) | Задаёт указанный API‑ключ для модели. |
| [WithOrganization](./withorganization/)(const System::String\&) | Устанавливает указанную организацию для модели. |
| [WithProject](./withproject/)(const System::String\&) | Устанавливает указанный проект для модели. |

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

## См. также

* Class [AiModel](../aimodel/)
* Namespace [Aspose::Words::AI](../)
* Library [Aspose.Words for C++](../../)
