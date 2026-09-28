---
title: "Метод Aspose::Words::AI::OpenAiModel::WithProject"
linktitle: "WithProject"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::AI::OpenAiModel::WithProject. Устанавливает указанный проект для модели в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words.ai/openaimodel/withproject/
---
## OpenAiModel::WithProject method


Устанавливает указанный проект для модели.

```cpp
System::SharedPtr<Aspose::Words::AI::OpenAiModel> Aspose::Words::AI::OpenAiModel::WithProject(const System::String &projectId)
```


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

* Class [OpenAiModel](../)
* Class [OpenAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
