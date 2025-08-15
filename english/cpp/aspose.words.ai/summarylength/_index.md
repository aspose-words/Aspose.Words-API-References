---
title: Aspose::Words::AI::SummaryLength enum
linktitle: SummaryLength
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::AI::SummaryLength enum. Enumerates possible lengths of summary in C++.'
type: docs
weight: 7000
url: /cpp/aspose.words.ai/summarylength/
---
## SummaryLength enum


Enumerates possible lengths of summary.

```cpp
enum class SummaryLength
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| VeryShort | 0 | Try to generate 1-2 sentences. |
| Short | 1 | Try to generate 3-4 sentences. |
| Medium | 2 | Try to generate 5-6 sentences. |
| Long | 3 | Try to generate 7-10 sentences. |
| VeryLong | 4 | Try to generate 11-20 sentences. |


## Examples



Shows how to summarize text using OpenAI and [Google](../../aspose.words.ai.google/) models. 
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
