---
title: "Aspose::Words::AI::AiModel::WithApiKey Methode"
linktitle: "WithApiKey"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::AI::AiModel::WithApiKey Methode. Legt einen angegebenen API‑Schlüssel für das Modell in C++ fest."
type: docs
weight: 5000
url: /de/cpp/aspose.words.ai/aimodel/withapikey/
---
## AiModel::WithApiKey method


Setzt einen angegebenen API-Schlüssel für das Modell.

```cpp
System::SharedPtr<Aspose::Words::AI::AiModel> Aspose::Words::AI::AiModel::WithApiKey(const System::String &apiKey)
```


## Beispiele



Zeigt, wie man Text mit OpenAI‑ und Google‑Modellen zusammenfasst.
```cpp
auto firstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");
auto secondDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
// Verwenden Sie generative Sprachmodelle von OpenAI oder Google.
System::SharedPtr<Aspose::Words::AI::AiModel> model = (System::ExplicitCast<Aspose::Words::AI::OpenAiModel>(Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::Gpt4OMini)->WithApiKey(apiKey)))->WithOrganization(u"Organization")->WithProject(u"Project");

auto options = System::MakeObject<Aspose::Words::AI::SummarizeOptions>();

options->set_SummaryLength(Aspose::Words::AI::SummaryLength::Short);
System::SharedPtr<Aspose::Words::Document> oneDocumentSummary = model->Summarize(firstDoc, options);
oneDocumentSummary->Save(get_ArtifactsDir() + u"AI.AiSummarize.One.docx");

options->set_SummaryLength(Aspose::Words::AI::SummaryLength::Long);
System::SharedPtr<Aspose::Words::Document> multiDocumentSummary = model->Summarize(System::MakeArray<System::SharedPtr<Aspose::Words::Document>>({firstDoc, secondDoc}), options);
multiDocumentSummary->Save(get_ArtifactsDir() + u"AI.AiSummarize.Multi.docx");
```

## Siehe auch

* Class [AiModel](../)
* Class [AiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
