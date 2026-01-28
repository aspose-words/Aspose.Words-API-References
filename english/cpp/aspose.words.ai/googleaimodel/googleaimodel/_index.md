---
title: Aspose::Words::AI::GoogleAiModel::GoogleAiModel constructor
linktitle: GoogleAiModel
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::AI::GoogleAiModel::GoogleAiModel constructor. Initializes a new instance of GoogleAiModel class in C++.'
type: docs
weight: 1500
url: /cpp/aspose.words.ai/googleaimodel/googleaimodel/
---
## GoogleAiModel::GoogleAiModel(const System::String\&) constructor


Initializes a new instance of [GoogleAiModel](../) class.

```cpp
Aspose::Words::AI::GoogleAiModel::GoogleAiModel(const System::String &name)
```


| Parameter | Type | Description |
| --- | --- | --- |
| name | const System::String\& | The name of the model. For example, gemini-2.5-flash. |

## Examples



Shows how to use google [AI](../../) model. 
```cpp
System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
auto model = System::MakeObject<Aspose::Words::AI::GoogleAiModel>(u"gemini-flash-latest", apiKey);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");
auto summarizeOptions = System::MakeObject<Aspose::Words::AI::SummarizeOptions>();
summarizeOptions->set_SummaryLength(Aspose::Words::AI::SummaryLength::VeryShort);
System::SharedPtr<Aspose::Words::Document> summary = model->Summarize(doc, summarizeOptions);
```

## See Also

* Class [GoogleAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
## GoogleAiModel::GoogleAiModel(const System::String\&, const System::String\&) constructor


Initializes a new instance of [GoogleAiModel](../) class.

```cpp
Aspose::Words::AI::GoogleAiModel::GoogleAiModel(const System::String &name, const System::String &apiKey)
```


| Parameter | Type | Description |
| --- | --- | --- |
| name | const System::String\& | The name of the model. For example, gemini-2.5-flash. |
| apiKey | const System::String\& | The API key to use the Gemini API. Please refer to [https://ai.google.dev/gemini-api/docs/api-key](https://ai.google.dev/gemini-api/docs/api-key) for details. |

## Examples



Shows how to use google [AI](../../) model. 
```cpp
System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
auto model = System::MakeObject<Aspose::Words::AI::GoogleAiModel>(u"gemini-flash-latest", apiKey);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");
auto summarizeOptions = System::MakeObject<Aspose::Words::AI::SummarizeOptions>();
summarizeOptions->set_SummaryLength(Aspose::Words::AI::SummaryLength::VeryShort);
System::SharedPtr<Aspose::Words::Document> summary = model->Summarize(doc, summarizeOptions);
```

## See Also

* Class [GoogleAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
