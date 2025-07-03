---
title: Aspose::Words::AI::SummarizeOptions::get_SummaryLength method
linktitle: get_SummaryLength
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::AI::SummarizeOptions::get_SummaryLength method. Allows to specify summary length. Default value is Medium in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.ai/summarizeoptions/get_summarylength/
---
## SummarizeOptions::get_SummaryLength method


Allows to specify summary length. Default value is [Medium](../../summarylength/).

```cpp
Aspose::Words::AI::SummaryLength Aspose::Words::AI::SummarizeOptions::get_SummaryLength() const
```


## Examples



Shows how to summarize text using OpenAI and [Google](../../../aspose.words.ai.google/) models. 
```cpp
auto firstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");
auto secondDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
// Use OpenAI or Google generative language models.
System::SharedPtr<Aspose::Words::AI::IAiModelText> model = (System::ExplicitCast<Aspose::Words::AI::OpenAiModel>(Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::Gpt4OMini)->WithApiKey(apiKey)))->WithOrganization(u"Organization")->WithProject(u"Project");

auto options = System::MakeObject<Aspose::Words::AI::SummarizeOptions>();

options->set_SummaryLength(Aspose::Words::AI::SummaryLength::Short);
System::SharedPtr<Aspose::Words::Document> oneDocumentSummary = model->Summarize(firstDoc, options);
oneDocumentSummary->Save(get_ArtifactsDir() + u"AI.AiSummarize.One.docx");

options->set_SummaryLength(Aspose::Words::AI::SummaryLength::Long);
System::SharedPtr<Aspose::Words::Document> multiDocumentSummary = model->Summarize(System::MakeArray<System::SharedPtr<Aspose::Words::Document>>({firstDoc, secondDoc}), options);
multiDocumentSummary->Save(get_ArtifactsDir() + u"AI.AiSummarize.Multi.docx");
```

## See Also

* Enum [SummaryLength](../../summarylength/)
* Class [SummarizeOptions](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
