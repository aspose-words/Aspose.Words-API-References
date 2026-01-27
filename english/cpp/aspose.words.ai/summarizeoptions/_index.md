---
title: Aspose::Words::AI::SummarizeOptions class
linktitle: SummarizeOptions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::AI::SummarizeOptions class. Allows to specify various options for summarizing document content in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words.ai/summarizeoptions/
---
## SummarizeOptions class


Allows to specify various options for summarizing document content.

```cpp
class SummarizeOptions : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_SummaryLength](./get_summarylength/)() const | Allows to specify summary length. Default value is [Medium](../summarylength/). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_SummaryLength](./set_summarylength/)(Aspose::Words::AI::SummaryLength) | Setter for [Aspose::Words::AI::SummarizeOptions::get_SummaryLength](./get_summarylength/). |
| [SummarizeOptions](./summarizeoptions/)() | Initializes a new instances of [SummarizeOptions](./) class. |
| static [Type](./type/)() |  |

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
