---
title: Aspose::Words::AI::AiModelType enum
linktitle: AiModelType
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::AI::AiModelType enum. Represents the types of AiModel that can be integrated into the document processing workflow in C++.'
type: docs
weight: 6000
url: /cpp/aspose.words.ai/aimodeltype/
---
## AiModelType enum


Represents the types of [AiModel](../aimodel/) that can be integrated into the document processing workflow.

```cpp
enum class AiModelType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Gpt4O | 0 | GPT-4o generative model type. |
| Gpt4OMini | 1 | GPT-4o mini generative model type. |
| Gpt4Turbo | 2 | GPT-4 Turbo generative model type. |
| Gpt35Turbo | 3 | GPT-3.5 Turbo generative model type. |
| GeminiFlashLatest | 4 | Gemini Flash latest release generative model type. |
| GeminiProLatest | 6 | Gemini Pro latest release generative model type. |
| Claude35Sonnet | 7 | Claude 3.5 Sonnet generative model type. |
| Claude35Haiku | 8 | Claude 3.5 Haiku generative model type. |
| Claude3Opus | 9 | Claude 3 Opus generative model type. |
| Claude3Sonnet | 10 | Claude 3 Sonnet generative model type. |
| Claude3Haiku | 11 | Claude 3 Haiku generative model type. |


## Examples



Shows how to summarize text using OpenAI and Google models. 
```cpp
auto firstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");
auto secondDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
// Use OpenAI or Google generative language models.
System::SharedPtr<Aspose::Words::AI::AiModel> model = (System::ExplicitCast<Aspose::Words::AI::OpenAiModel>(Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::Gpt4OMini)->WithApiKey(apiKey)))->WithOrganization(u"Organization")->WithProject(u"Project");

auto options = System::MakeObject<Aspose::Words::AI::SummarizeOptions>();

options->set_SummaryLength(Aspose::Words::AI::SummaryLength::Short);
System::SharedPtr<Aspose::Words::Document> oneDocumentSummary = model->Summarize(firstDoc, options);
oneDocumentSummary->Save(get_ArtifactsDir() + u"AI.AiSummarize.One.docx");

options->set_SummaryLength(Aspose::Words::AI::SummaryLength::Long);
System::SharedPtr<Aspose::Words::Document> multiDocumentSummary = model->Summarize(System::MakeArray<System::SharedPtr<Aspose::Words::Document>>({firstDoc, secondDoc}), options);
multiDocumentSummary->Save(get_ArtifactsDir() + u"AI.AiSummarize.Multi.docx");
```

## See Also

* Namespace [Aspose::Words::AI](../)
* Library [Aspose.Words for C++](../../)
