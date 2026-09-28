---
title: "Класс Aspose::Words::AI::AiModel"
linktitle: "AiModel"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::AI::AiModel. Абстрактный класс, представляющий интеграцию с различными AI‑моделями в Aspose.Words на C++."
type: docs
weight: 1000
url: /ru/cpp/aspose.words.ai/aimodel/
---
## AiModel class


Абстрактный класс, представляющий интеграцию с различными моделями [AI](../) в рамках [Aspose.Words](../../aspose.words/).

```cpp
class AiModel : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| virtual [CheckGrammar](./checkgrammar/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::CheckGrammarOptions\>) | Проверяет грамматику предоставленного документа. Эта операция использует подключённую модель [AI](../) для проверки грамматики документа. |
| static [Create](./create/)(Aspose::Words::AI::AiModelType) | Создаёт новый экземпляр класса [AiModel](./). |
| [get_Timeout](./get_timeout/)() const | Получает или задает количество миллисекунд ожидания до истечения тайм‑аута запроса к модели [AI](../). Значение по умолчанию — 100 000 миллисекунд (100 секунд). |
| virtual [get_Url](./get_url/)() | Получает или задает URL модели. Значение по умолчанию специфично для модели. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Timeout](./set_timeout/)(int32_t) | Сеттер для [Aspose::Words::AI::AiModel::get_Timeout](./get_timeout/). |
| virtual [set_Url](./set_url/)(System::String) | Сеттер для [Aspose::Words::AI::AiModel::get_Url](./get_url/). |
| virtual [Summarize](./summarize/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) | Создаёт резюме указанного документа с возможностью настройки длины резюме. Эта операция использует подключённую модель [AI](../) для обработки содержимого. |
| virtual [Summarize](./summarize/)(System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) | Создаёт резюме для массива документов с возможностью управления длиной резюме и другими параметрами. Этот метод использует подключённую модель [AI](../) для обработки каждого документа в массиве. |
| virtual [Translate](./translate/)(System::SharedPtr\<Aspose::Words::Document\>, Aspose::Words::AI::Language) | Переводит предоставленный документ на указанный целевой язык. Эта операция использует подключённую модель [AI](../) для перевода содержимого. |
| static [Type](./type/)() |  |
| [WithApiKey](./withapikey/)(const System::String\&) | Задаёт указанный API‑ключ для модели. |

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

* Namespace [Aspose::Words::AI](../)
* Library [Aspose.Words for C++](../../)
