---
title: Aspose::Words::AI::IAiModelText interface
linktitle: IAiModelText
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::AI::IAiModelText interface. The common interface for AI models designed to generate a variety of text-based content in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words.ai/iaimodeltext/
---
## IAiModelText interface


The common interface for [AI](../) models designed to generate a variety of text-based content.

```cpp
class IAiModelText : public virtual System::Object
```

## Methods

| Method | Description |
| --- | --- |
| virtual [CheckGrammar](./checkgrammar/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::CheckGrammarOptions\>) | Checks grammar of the provided document. This operation leverages the connected [AI](../) model for checking grammar of document. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Summarize](./summarize/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) | Generates a summary of the specified document, with options to adjust the length of the summary. This operation leverages the connected [AI](../) model for content processing. |
| virtual [Summarize](./summarize/)(System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) | Generates summaries for an array of documents, with options to control the summary length and other settings. This method utilizes the connected [AI](../) model for processing each document in the array. |
| virtual [Translate](./translate/)(System::SharedPtr\<Aspose::Words::Document\>, Aspose::Words::AI::Language) | Translates the provided document into the specified target language. This operation leverages the connected [AI](../) model for content translating. |
| static [Type](./type/)() |  |

## Examples



Shows how to summarize text using OpenAI and [Google](../../aspose.words.ai.google/) models. 
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

* Namespace [Aspose::Words::AI](../)
* Library [Aspose.Words for C++](../../)
