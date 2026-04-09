---
title: Aspose::Words::AI::OpenAiModel::OpenAiModel constructor
linktitle: OpenAiModel
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::AI::OpenAiModel::OpenAiModel constructor. Initializes a new instance of OpenAiModel class in C++.'
type: docs
weight: 1334
url: /cpp/aspose.words.ai/openaimodel/openaimodel/
---
## OpenAiModel::OpenAiModel(const System::String\&) constructor


Initializes a new instance of [OpenAiModel](../) class.

```cpp
Aspose::Words::AI::OpenAiModel::OpenAiModel(const System::String &name)
```


| Parameter | Type | Description |
| --- | --- | --- |
| name | const System::String\& | The name of the model. For example, gpt-5.2-chat-latest. |

## See Also

* Class [OpenAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
## OpenAiModel::OpenAiModel(const System::String\&, const System::String\&) constructor


Initializes a new instance of [OpenAiModel](../) class.

```cpp
Aspose::Words::AI::OpenAiModel::OpenAiModel(const System::String &name, const System::String &apiKey)
```


| Parameter | Type | Description |
| --- | --- | --- |
| name | const System::String\& | The name of the model. For example, gpt-5.2-chat-latest. |
| apiKey | const System::String\& | The API key to use the OpenAi API. |

## Examples



Shows how to create an OpenAI model instance directly using an API key and model name. 
```cpp
System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
// Create an OpenAI model instance using the constructor with model name and API key.
auto model = System::MakeObject<Aspose::Words::AI::OpenAiModel>(u"gpt-4o-mini", apiKey);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");
// Summarize the document using the OpenAI model with short summary length.
auto summarizeOptions = System::MakeObject<Aspose::Words::AI::SummarizeOptions>();
summarizeOptions->set_SummaryLength(Aspose::Words::AI::SummaryLength::VeryShort);
System::SharedPtr<Aspose::Words::Document> summary = model->Summarize(doc, summarizeOptions);

summary->Save(get_ArtifactsDir() + u"OpenAiModel.OpenAiModelConstructor.docx");
```

## See Also

* Class [OpenAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
