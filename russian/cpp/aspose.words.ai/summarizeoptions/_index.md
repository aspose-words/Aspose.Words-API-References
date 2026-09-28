---
title: "Aspose::Words::AI::SummarizeOptions класс"
linktitle: "SummarizeOptions"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::AI::SummarizeOptions класс. Позволяет указывать различные параметры для суммирования содержимого документа в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.ai/summarizeoptions/
---
## SummarizeOptions class


Позволяет задавать различные параметры для суммирования содержимого документа.

```cpp
class SummarizeOptions : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_SummaryLength](./get_summarylength/)() const | Позволяет задавать длину резюме. Значение по умолчанию — [Medium](../summarylength/). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_SummaryLength](./set_summarylength/)(Aspose::Words::AI::SummaryLength) | Сеттер для [Aspose::Words::AI::SummarizeOptions::get_SummaryLength](./get_summarylength/). |
| [SummarizeOptions](./summarizeoptions/)() | Инициализирует новый экземпляр класса [SummarizeOptions](./). |
| static [Type](./type/)() |  |

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
