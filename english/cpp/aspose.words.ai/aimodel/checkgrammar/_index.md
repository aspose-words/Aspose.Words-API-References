---
title: Aspose::Words::AI::AiModel::CheckGrammar method
linktitle: CheckGrammar
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::AI::AiModel::CheckGrammar method. Checks grammar of the provided document. This operation leverages the connected AI model for checking grammar of document in C++.'
type: docs
weight: 2500
url: /cpp/aspose.words.ai/aimodel/checkgrammar/
---
## AiModel::CheckGrammar method


Checks grammar of the provided document. This operation leverages the connected [AI](../../) model for checking grammar of document.

```cpp
virtual System::SharedPtr<Aspose::Words::Document> Aspose::Words::AI::AiModel::CheckGrammar(System::SharedPtr<Aspose::Words::Document> sourceDocument, System::SharedPtr<Aspose::Words::AI::CheckGrammarOptions> options=nullptr)
```


| Parameter | Type | Description |
| --- | --- | --- |
| sourceDocument | System::SharedPtr\<Aspose::Words::Document\> | The document being checked for grammar. |
| options | System::SharedPtr\<Aspose::Words::AI::CheckGrammarOptions\> | Optional settings to control how grammar will be checked. |

### ReturnValue

A new [Document](../../../aspose.words/document/) with checked grammar.

## Examples



Shows how to check the grammar of a document. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
// Use OpenAI generative language models.
System::SharedPtr<Aspose::Words::AI::AiModel> model = Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::Gpt4OMini)->WithApiKey(apiKey);

auto grammarOptions = System::MakeObject<Aspose::Words::AI::CheckGrammarOptions>();
grammarOptions->set_ImproveStylistics(true);

System::SharedPtr<Aspose::Words::Document> proofedDoc = model->CheckGrammar(doc, grammarOptions);
proofedDoc->Save(get_ArtifactsDir() + u"AI.AiGrammar.docx");
```

## See Also

* Class [Document](../../../aspose.words/document/)
* Class [CheckGrammarOptions](../../checkgrammaroptions/)
* Class [AiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
