---
title: "Aspose::Words::AI::GoogleAiModel::GoogleAiModel конструктор"
linktitle: "GoogleAiModel"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::AI::GoogleAiModel::GoogleAiModel конструктор. Инициализирует новый экземпляр класса GoogleAiModel в C++."
type: docs
weight: 1500
url: /ru/cpp/aspose.words.ai/googleaimodel/googleaimodel/
---
## GoogleAiModel::GoogleAiModel(const System::String\&) constructor


Инициализирует новый экземпляр класса [GoogleAiModel](../).

```cpp
Aspose::Words::AI::GoogleAiModel::GoogleAiModel(const System::String &name)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| name | const System::String\& | Имя модели. Например, gemini-2.5-flash. |

## Примеры



Показывает, как использовать модель google [AI](../../).
```cpp
System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
auto model = System::MakeObject<Aspose::Words::AI::GoogleAiModel>(u"gemini-flash-latest", apiKey);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");
auto summarizeOptions = System::MakeObject<Aspose::Words::AI::SummarizeOptions>();
summarizeOptions->set_SummaryLength(Aspose::Words::AI::SummaryLength::VeryShort);
System::SharedPtr<Aspose::Words::Document> summary = model->Summarize(doc, summarizeOptions);
```

## См. также

* Class [GoogleAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
## GoogleAiModel::GoogleAiModel(const System::String\&, const System::String\&) constructor


Инициализирует новый экземпляр класса [GoogleAiModel](../).

```cpp
Aspose::Words::AI::GoogleAiModel::GoogleAiModel(const System::String &name, const System::String &apiKey)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| name | const System::String\& | Имя модели. Например, gemini-2.5-flash. |
| apiKey | const System::String\& | API‑ключ для использования Gemini API. Пожалуйста, обратитесь к [https://ai.google.dev/gemini-api/docs/api-key](https://ai.google.dev/gemini-api/docs/api-key) для получения подробностей. |

## Примеры



Показывает, как использовать модель google [AI](../../).
```cpp
System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
auto model = System::MakeObject<Aspose::Words::AI::GoogleAiModel>(u"gemini-flash-latest", apiKey);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");
auto summarizeOptions = System::MakeObject<Aspose::Words::AI::SummarizeOptions>();
summarizeOptions->set_SummaryLength(Aspose::Words::AI::SummaryLength::VeryShort);
System::SharedPtr<Aspose::Words::Document> summary = model->Summarize(doc, summarizeOptions);
```

## См. также

* Class [GoogleAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
