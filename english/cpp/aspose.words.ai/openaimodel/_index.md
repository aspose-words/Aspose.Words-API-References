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
class OpenAiModel : public Aspose::Words::AI::AiModel,
                    public Aspose::Words::AI::IAiModelText
```

## Methods

| Method | Description |
| --- | --- |
| static [Create](../aimodel/create/)(Aspose::Words::AI::AiModelType) | Creates a new instance of [AiModel](../aimodel/) class. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
| [WithApiKey](../aimodel/withapikey/)(const System::String\&) | Sets a specified API key to the model. |
| [WithOrganization](./withorganization/)(const System::String\&) | Sets a specified Organization to the model. |
| [WithProject](./withproject/)(const System::String\&) | Sets a specified Project to the model. |

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

* Class [AiModel](../aimodel/)
* Interface [IAiModelText](../iaimodeltext/)
* Namespace [Aspose::Words::AI](../)
* Library [Aspose.Words for C++](../../)
