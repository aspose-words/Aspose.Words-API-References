---
title: Aspose::Words::AI::CheckGrammarOptions class
linktitle: CheckGrammarOptions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::AI::CheckGrammarOptions class. Allows to specify various options while checking grammar of a document using AI in C++.'
type: docs
weight: 1500
url: /cpp/aspose.words.ai/checkgrammaroptions/
---
## CheckGrammarOptions class


Allows to specify various options while checking grammar of a document using [AI](../).

```cpp
class CheckGrammarOptions : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [CheckGrammarOptions](./checkgrammaroptions/)() |  |
| [get_ImproveStylistics](./get_improvestylistics/)() const | Allows to specify either [AI](../) will try to improve stylistics of the text being proofed. Default value is **false**. |
| [get_MakeRevisions](./get_makerevisions/)() const | Allows to specify either final or revised document to be returned with proofed text. Default value is **false**. |
| [get_PreserveFormatting](./get_preserveformatting/)() const | Allows to specify either [CheckGrammar()](../iaimodeltext/checkgrammar/) will try to preserve layout and formatting of the original document, or not. Default value is **true**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ImproveStylistics](./set_improvestylistics/)(bool) | Allows to specify either [AI](../) will try to improve stylistics of the text being proofed. Default value is **false**. |
| [set_MakeRevisions](./set_makerevisions/)(bool) | Allows to specify either final or revised document to be returned with proofed text. Default value is **false**. |
| [set_PreserveFormatting](./set_preserveformatting/)(bool) | Allows to specify either [CheckGrammar()](../iaimodeltext/checkgrammar/) will try to preserve layout and formatting of the original document, or not. Default value is **true**. |
| static [Type](./type/)() |  |

## Examples



Shows how to check the grammar of a document. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
// Use OpenAI generative language models.
System::SharedPtr<Aspose::Words::AI::IAiModelText> model = System::ExplicitCast<Aspose::Words::AI::OpenAiModel>(Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::Gpt4OMini)->WithApiKey(apiKey));

auto grammarOptions = System::MakeObject<Aspose::Words::AI::CheckGrammarOptions>();
grammarOptions->set_ImproveStylistics(true);

System::SharedPtr<Aspose::Words::Document> proofedDoc = model->CheckGrammar(doc, grammarOptions);
proofedDoc->Save(get_ArtifactsDir() + u"AI.AiGrammar.docx");
```

## See Also

* Namespace [Aspose::Words::AI](../)
* Library [Aspose.Words for C++](../../)
