---
title: Aspose::Words::AI::AiModel::Translate method
linktitle: Translate
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::AI::AiModel::Translate method. Translates the provided document into the specified target language. This operation leverages the connected AI model for content translating in C++.'
type: docs
weight: 4667
url: /cpp/aspose.words.ai/aimodel/translate/
---
## AiModel::Translate method


Translates the provided document into the specified target language. This operation leverages the connected [AI](../../) model for content translating.

```cpp
virtual System::SharedPtr<Aspose::Words::Document> Aspose::Words::AI::AiModel::Translate(System::SharedPtr<Aspose::Words::Document> sourceDocument, Aspose::Words::AI::Language targetLanguage)=0
```


| Parameter | Type | Description |
| --- | --- | --- |
| sourceDocument | System::SharedPtr\<Aspose::Words::Document\> | The document to be translated. |
| targetLanguage | Aspose::Words::AI::Language | The language into which the document will be translated. |

### ReturnValue

A new [Document](../../../aspose.words/document/) object containing the translated document.

## Examples



Shows how to translate text using Google models. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
// Use Google generative language models.
System::SharedPtr<Aspose::Words::AI::AiModel> model = Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::GeminiFlashLatest)->WithApiKey(apiKey);

System::SharedPtr<Aspose::Words::Document> translatedDoc = model->Translate(doc, Aspose::Words::AI::Language::Arabic);
translatedDoc->Save(get_ArtifactsDir() + u"AI.AiTranslate.docx");
```

## See Also

* Class [Document](../../../aspose.words/document/)
* Enum [Language](../../language/)
* Class [AiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
