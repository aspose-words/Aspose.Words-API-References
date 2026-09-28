---
title: "Конструктор Aspose::Words::AI::OpenAiModel::OpenAiModel"
linktitle: "OpenAiModel"
second_title: "Справочник API Aspose.Words для C++"
description: "Конструктор Aspose::Words::AI::OpenAiModel::OpenAiModel. Инициализирует новый экземпляр класса OpenAiModel на C++."
type: docs
weight: 1334
url: /ru/cpp/aspose.words.ai/openaimodel/openaimodel/
---
## OpenAiModel::OpenAiModel(const System::String\&) constructor


Инициализирует новый экземпляр класса [OpenAiModel](../).

```cpp
Aspose::Words::AI::OpenAiModel::OpenAiModel(const System::String &name)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| name | const System::String\& | Имя модели. Например, gpt-5.2-chat-latest. |

## См. также

* Class [OpenAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
## OpenAiModel::OpenAiModel(const System::String\&, const System::String\&) constructor


Инициализирует новый экземпляр класса [OpenAiModel](../).

```cpp
Aspose::Words::AI::OpenAiModel::OpenAiModel(const System::String &name, const System::String &apiKey)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| name | const System::String\& | Имя модели. Например, gpt-5.2-chat-latest. |
| apiKey | const System::String\& | API‑ключ для использования OpenAi API. |

## Примеры



Показывает, как создать экземпляр модели OpenAI напрямую, используя API‑ключ и имя модели.
```cpp
System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
// Создайте экземпляр модели OpenAI, используя конструктор с именем модели и API‑ключом.
auto model = System::MakeObject<Aspose::Words::AI::OpenAiModel>(u"gpt-4o-mini", apiKey);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");
// Сделайте резюме документа с помощью модели OpenAI, используя короткую длину резюме.
auto summarizeOptions = System::MakeObject<Aspose::Words::AI::SummarizeOptions>();
summarizeOptions->set_SummaryLength(Aspose::Words::AI::SummaryLength::VeryShort);
System::SharedPtr<Aspose::Words::Document> summary = model->Summarize(doc, summarizeOptions);

summary->Save(get_ArtifactsDir() + u"OpenAiModel.OpenAiModelConstructor.docx");
```

## См. также

* Class [OpenAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
