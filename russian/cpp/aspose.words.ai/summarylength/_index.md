---
title: "Перечисление Aspose::Words::AI::SummaryLength"
linktitle: "SummaryLength"
second_title: "Справочник API Aspose.Words для C++"
description: "Перечисление Aspose::Words::AI::SummaryLength. Перечисляет возможные длины резюме в C++."
type: docs
weight: 7000
url: /ru/cpp/aspose.words.ai/summarylength/
---
## SummaryLength enum


Перечисляет возможные длины резюме.

```cpp
enum class SummaryLength
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| VeryShort | 0 | Попробуйте сгенерировать 1‑2 предложения. |
| Short | 1 | Попробуйте сгенерировать 3‑4 предложения. |
| Medium | 2 | Попробуйте сгенерировать 5‑6 предложений. |
| Длинный | 3 | Попробуйте сгенерировать 7-10 предложений. |
| ОченьДлинный | 4 | Попробуйте сгенерировать 11-20 предложений. |


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
