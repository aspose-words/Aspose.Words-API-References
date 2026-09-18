---
title: "Aspose::Words::AI::AiModelType Enum"
linktitle: "AiModelType"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::AI::AiModelType Enum. Stellt die Typen von AiModel dar, die in den Dokumentverarbeitungs‑Workflow in C++ integriert werden können."
type: docs
weight: 6000
url: /de/cpp/aspose.words.ai/aimodeltype/
---
## AiModelType enum


Stellt die Typen von [AiModel](../aimodel/) dar, die in den Dokumentverarbeitungs‑Workflow integriert werden können.

```cpp
enum class AiModelType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Gpt4O | 0 | GPT-4o generativer Modelltyp. |
| Gpt4OMini | 1 | GPT-4o mini generativer Modellentyp. |
| Gpt4Turbo | 2 | GPT-4 Turbo generativer Modellentyp. |
| Gpt35Turbo | 3 | GPT-3.5 Turbo generativer Modellentyp. |
| GeminiFlashLatest | 4 | Gemini Flash neueste Veröffentlichung generativer Modellentyp. |
| GeminiProLatest | 6 | Gemini Pro neueste Veröffentlichung generativer Modellentyp. |
| Claude35Sonnet | 7 | Claude 3.5 Sonnet generativer Modellentyp. |
| Claude35Haiku | 8 | Claude 3.5 Haiku generativer Modellentyp. |
| Claude3Opus | 9 | Claude 3 Opus generativer Modellentyp. |
| Claude3Sonnet | 10 | Claude 3 Sonnet generativer Modellentyp. |
| Claude3Haiku | 11 | Claude 3 Haiku generativer Modellentyp. |


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

* Namespace [Aspose::Words::AI](../)
* Library [Aspose.Words for C++](../../)
