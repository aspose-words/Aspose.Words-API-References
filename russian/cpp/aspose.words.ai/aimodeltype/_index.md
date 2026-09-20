---
title: "Aspose::Words::AI::AiModelType перечисление"
linktitle: "AiModelType"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::AI::AiModelType перечисление. Представляет типы AiModel, которые могут быть интегрированы в рабочий процесс обработки документов в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words.ai/aimodeltype/
---
## AiModelType enum


Представляет типы [AiModel](../aimodel/), которые могут быть интегрированы в рабочий процесс обработки документов.

```cpp
enum class AiModelType
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Gpt4O | 0 | Тип генеративной модели GPT-4o. |
| Gpt4OMini | 1 | Тип генеративной модели GPT-4o mini. |
| Gpt4Turbo | 2 | Тип генеративной модели GPT-4 Turbo. |
| Gpt35Turbo | 3 | Тип генеративной модели GPT-3.5 Turbo. |
| GeminiFlashLatest | 4 | Тип генеративной модели Gemini Flash последнего выпуска. |
| GeminiProLatest | 6 | Тип генеративной модели Gemini Pro последнего выпуска. |
| Claude35Sonnet | 7 | Claude 3.5 Sonnet тип генеративной модели. |
| Claude35Haiku | 8 | Claude 3.5 Haiku тип генеративной модели. |
| Claude3Opus | 9 | Claude 3 Opus тип генеративной модели. |
| Claude3Sonnet | 10 | Claude 3 Sonnet тип генеративной модели. |
| Claude3Haiku | 11 | Claude 3 Haiku тип генеративной модели. |


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
