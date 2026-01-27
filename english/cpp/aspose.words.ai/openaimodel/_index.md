---
title: Aspose::Words::AI::OpenAiModel class
linktitle: OpenAiModel
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::AI::OpenAiModel class. An abstract class representing the integration with OpenAI''s large language models within the Aspose.Words in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.ai/openaimodel/
---
## OpenAiModel class


An abstract class representing the integration with OpenAI's large language models within the [Aspose.Words](../../aspose.words/).

```cpp
class OpenAiModel : public Aspose::Words::AI::AiModel
```

## Methods

| Method | Description |
| --- | --- |
| virtual [CheckGrammar](../aimodel/checkgrammar/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::CheckGrammarOptions\>) | Checks grammar of the provided document. This operation leverages the connected [AI](../) model for checking grammar of document. |
| static [Create](../aimodel/create/)(Aspose::Words::AI::AiModelType) | Creates a new instance of [AiModel](../aimodel/) class. |
| [get_Timeout](../aimodel/get_timeout/)() const | Gets or sets the number of milliseconds to wait before the request to [AI](../) model times out. The default value is 100,000 milliseconds (100 seconds). |
| [get_Url](./get_url/)() override | Gets a URL of the model. The default value is "https://api.openai.com/". |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Timeout](../aimodel/set_timeout/)(int32_t) | Setter for [Aspose::Words::AI::AiModel::get_Timeout](../aimodel/get_timeout/). |
| [set_Url](./set_url/)(System::String) override | Sets a URL of the model. The default value is "https://api.openai.com/". |
| [Summarize](./summarize/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) override | Generates a summary of the specified document, with options to adjust the length of the summary. This operation leverages the connected [AI](../) model for content processing. |
| [Summarize](./summarize/)(System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) override | Generates summaries for an array of documents, with options to control the summary length and other settings. This method utilizes the connected [AI](../) model for processing each document in the array. |
| [Translate](./translate/)(System::SharedPtr\<Aspose::Words::Document\>, Aspose::Words::AI::Language) override | Translates the provided document into the specified target language. This operation leverages the connected [AI](../) model for content translating. |
| static [Type](./type/)() |  |
| [WithApiKey](../aimodel/withapikey/)(const System::String\&) | Sets a specified API key to the model. |
| [WithOrganization](./withorganization/)(const System::String\&) | Sets a specified Organization to the model. |
| [WithProject](./withproject/)(const System::String\&) | Sets a specified Project to the model. |

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

* Class [AiModel](../aimodel/)
* Namespace [Aspose::Words::AI](../)
* Library [Aspose.Words for C++](../../)
