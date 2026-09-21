---
title: "Aspose::Words::AI::AiModelType enum"
linktitle: "AiModelType"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::AI::AiModelType enum. Representerar typerna av AiModel som kan integreras i dokumentbehandlingsarbetsflödet i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words.ai/aimodeltype/
---
## AiModelType enum


Representerar typerna av [AiModel](../aimodel/) som kan integreras i dokumentbehandlingsarbetsflödet.

```cpp
enum class AiModelType
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| Gpt4O | 0 | GPT-4o generativ modelltyp. |
| Gpt4OMini | 1 | GPT-4o mini generativ modelltyp. |
| Gpt4Turbo | 2 | GPT-4 Turbo generativ modelltyp. |
| Gpt35Turbo | 3 | GPT-3.5 Turbo generativ modelltyp. |
| GeminiFlashLatest | 4 | Gemini Flash senaste utgåva generativ modelltyp. |
| GeminiProLatest | 6 | Gemini Pro senaste utgåva generativ modelltyp. |
| Claude35Sonnet | 7 | Claude 3.5 Sonnet generativ modelltyp. |
| Claude35Haiku | 8 | Claude 3.5 Haiku generativ modelltyp. |
| Claude3Opus | 9 | Claude 3 Opus generativ modelltyp. |
| Claude3Sonnet | 10 | Claude 3 Sonnet generativ modelltyp. |
| Claude3Haiku | 11 | Claude 3 Haiku generativ modelltyp. |


## Exempel



Visar hur man sammanfattar text med hjälp av OpenAI- och Google-modeller.
```cpp
auto firstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");
auto secondDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
// Använd generativa språkmodeller från OpenAI eller Google.
System::SharedPtr<Aspose::Words::AI::AiModel> model = (System::ExplicitCast<Aspose::Words::AI::OpenAiModel>(Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::Gpt4OMini)->WithApiKey(apiKey)))->WithOrganization(u"Organization")->WithProject(u"Project");

auto options = System::MakeObject<Aspose::Words::AI::SummarizeOptions>();

options->set_SummaryLength(Aspose::Words::AI::SummaryLength::Short);
System::SharedPtr<Aspose::Words::Document> oneDocumentSummary = model->Summarize(firstDoc, options);
oneDocumentSummary->Save(get_ArtifactsDir() + u"AI.AiSummarize.One.docx");

options->set_SummaryLength(Aspose::Words::AI::SummaryLength::Long);
System::SharedPtr<Aspose::Words::Document> multiDocumentSummary = model->Summarize(System::MakeArray<System::SharedPtr<Aspose::Words::Document>>({firstDoc, secondDoc}), options);
multiDocumentSummary->Save(get_ArtifactsDir() + u"AI.AiSummarize.Multi.docx");
```

## Se även

* Namespace [Aspose::Words::AI](../)
* Library [Aspose.Words for C++](../../)
