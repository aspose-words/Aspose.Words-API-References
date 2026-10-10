---
title: "Aspose::Words::AI::AiModelType enum"
linktitle: "AiModelType"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::AI::AiModelType enum. C++'ta belge işleme iş akışına entegre edilebilen AiModel türlerini temsil eder."
type: docs
weight: 6000
url: /tr/cpp/aspose.words.ai/aimodeltype/
---
## AiModelType enum


Belge işleme iş akışına entegre edilebilen [AiModel](../aimodel/) türlerini temsil eder.

```cpp
enum class AiModelType
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Gpt4O | 0 | GPT-4o üretken model türü. |
| Gpt4OMini | 1 | GPT-4o mini üretken model türü. |
| Gpt4Turbo | 2 | GPT-4 Turbo üretken model türü. |
| Gpt35Turbo | 3 | GPT-3.5 Turbo üretken model türü. |
| GeminiFlashLatest | 4 | Gemini Flash en son sürüm üretken model türü. |
| GeminiProLatest | 6 | Gemini Pro en son sürüm üretken model türü. |
| Claude35Sonnet | 7 | Claude 3.5 Sonnet üretken model türü. |
| Claude35Haiku | 8 | Claude 3.5 Haiku üretken model türü. |
| Claude3Opus | 9 | Claude 3 Opus üretken model türü. |
| Claude3Sonnet | 10 | Claude 3 Sonnet üretken model türü. |
| Claude3Haiku | 11 | Claude 3 Haiku üretken model türü. |


## Örnekler



OpenAI ve Google modellerini kullanarak metni nasıl özetleyeceğinizi gösterir.
```cpp
auto firstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");
auto secondDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
// OpenAI veya Google üretken dil modellerini kullanın.
System::SharedPtr<Aspose::Words::AI::AiModel> model = (System::ExplicitCast<Aspose::Words::AI::OpenAiModel>(Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::Gpt4OMini)->WithApiKey(apiKey)))->WithOrganization(u"Organization")->WithProject(u"Project");

auto options = System::MakeObject<Aspose::Words::AI::SummarizeOptions>();

options->set_SummaryLength(Aspose::Words::AI::SummaryLength::Short);
System::SharedPtr<Aspose::Words::Document> oneDocumentSummary = model->Summarize(firstDoc, options);
oneDocumentSummary->Save(get_ArtifactsDir() + u"AI.AiSummarize.One.docx");

options->set_SummaryLength(Aspose::Words::AI::SummaryLength::Long);
System::SharedPtr<Aspose::Words::Document> multiDocumentSummary = model->Summarize(System::MakeArray<System::SharedPtr<Aspose::Words::Document>>({firstDoc, secondDoc}), options);
multiDocumentSummary->Save(get_ArtifactsDir() + u"AI.AiSummarize.Multi.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::AI](../)
* Library [Aspose.Words for C++](../../)
