---
title: "Aspose::Words::AI::AnthropicAiModel класс"
linktitle: "AnthropicAiModel"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::AI::AnthropicAiModel класс. Абстрактный класс, представляющий интеграцию с AI-моделями Anthropic в Aspose.Words на C++."
type: docs
weight: 1250
url: /ru/cpp/aspose.words.ai/anthropicaimodel/
---
## AnthropicAiModel class


Абстрактный класс, представляющий интеграцию с [AI](../) моделями Anthropic внутри [Aspose.Words](../../aspose.words/).

```cpp
class AnthropicAiModel : public Aspose::Words::AI::AiModel
```

## Методы

| Метод | Описание |
| --- | --- |
| [AnthropicAiModel](./anthropicaimodel/)() |  |
| virtual [CheckGrammar](../aimodel/checkgrammar/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::CheckGrammarOptions\>) | Проверяет грамматику предоставленного документа. Эта операция использует подключённую модель [AI](../) для проверки грамматики документа. |
| static [Create](../aimodel/create/)(Aspose::Words::AI::AiModelType) | Создаёт новый экземпляр класса [AiModel](../aimodel/). |
| [get_Timeout](../aimodel/get_timeout/)() const | Получает или задает количество миллисекунд ожидания до истечения тайм‑аута запроса к модели [AI](../). Значение по умолчанию — 100 000 миллисекунд (100 секунд). |
| [get_Url](./get_url/)() override | Получает URL модели. Значение по умолчанию — "https://api.anthropic.com/". |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Timeout](../aimodel/set_timeout/)(int32_t) | Сеттер для [Aspose::Words::AI::AiModel::get_Timeout](../aimodel/get_timeout/). |
| [set_Url](./set_url/)(System::String) override | Задает URL модели. Значение по умолчанию — "https://api.anthropic.com/". |
| [Summarize](./summarize/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) override | Создаёт резюме указанного документа с возможностью настройки длины резюме. Эта операция использует подключённую модель [AI](../) для обработки содержимого. |
| [Summarize](./summarize/)(System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) override | Создаёт резюме для массива документов с возможностью управления длиной резюме и другими параметрами. Этот метод использует подключённую модель [AI](../) для обработки каждого документа в массиве. |
| [Translate](./translate/)(System::SharedPtr\<Aspose::Words::Document\>, Aspose::Words::AI::Language) override | Переводит предоставленный документ на указанный целевой язык. Эта операция использует подключённую модель [AI](../) для перевода содержимого. |
| static [Type](./type/)() |  |
| [WithApiKey](../aimodel/withapikey/)(const System::String\&) | Задаёт указанный API‑ключ для модели. |
## См. также

* Class [AiModel](../aimodel/)
* Namespace [Aspose::Words::AI](../)
* Library [Aspose.Words for C++](../../)
