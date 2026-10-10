---
title: "Aspose::Words::AI::AiModel::CheckGrammar metod"
linktitle: "CheckGrammar"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::AI::AiModel::CheckGrammar metod. Kontrollerar grammatiken i det angivna dokumentet. Denna operation utnyttjar den anslutna AI‑modellen för att kontrollera dokumentets grammatik i C++."
type: docs
weight: 2500
url: /sv/cpp/aspose.words.ai/aimodel/checkgrammar/
---
## AiModel::CheckGrammar method


Kontrollerar grammatiken i det angivna dokumentet. Denna operation utnyttjar den anslutna [AI](../../)‑modellen för att kontrollera dokumentets grammatik.

```cpp
virtual System::SharedPtr<Aspose::Words::Document> Aspose::Words::AI::AiModel::CheckGrammar(System::SharedPtr<Aspose::Words::Document> sourceDocument, System::SharedPtr<Aspose::Words::AI::CheckGrammarOptions> options=nullptr)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| sourceDocument | System::SharedPtr\<Aspose::Words::Document\> | Dokumentet som kontrolleras för grammatik. |
| options | System::SharedPtr\<Aspose::Words::AI::CheckGrammarOptions\> | Valfria inställningar för att styra hur grammatiken ska kontrolleras. |

### ReturnValue

Ett nytt [Document](../../../aspose.words/document/) med kontrollerad grammatik.

## Exempel



Visar hur man kontrollerar grammatiken i ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
// Använd OpenAI:s generativa språkmodeller.
System::SharedPtr<Aspose::Words::AI::AiModel> model = Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::Gpt4OMini)->WithApiKey(apiKey);

auto grammarOptions = System::MakeObject<Aspose::Words::AI::CheckGrammarOptions>();
grammarOptions->set_ImproveStylistics(true);

System::SharedPtr<Aspose::Words::Document> proofedDoc = model->CheckGrammar(doc, grammarOptions);
proofedDoc->Save(get_ArtifactsDir() + u"AI.AiGrammar.docx");
```

## Se även

* Class [Document](../../../aspose.words/document/)
* Class [CheckGrammarOptions](../../checkgrammaroptions/)
* Class [AiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
