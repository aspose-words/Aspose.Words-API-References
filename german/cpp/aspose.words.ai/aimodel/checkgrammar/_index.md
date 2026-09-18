---
title: "Aspose::Words::AI::AiModel::CheckGrammar-Methode"
linktitle: "CheckGrammar"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::AI::AiModel::CheckGrammar-Methode. Prüft die Grammatik des bereitgestellten Dokuments. Dieser Vorgang nutzt das verbundene KI-Modell zum Prüfen der Grammatik des Dokuments in C++."
type: docs
weight: 2500
url: /de/cpp/aspose.words.ai/aimodel/checkgrammar/
---
## AiModel::CheckGrammar method


Prüft die Grammatik des bereitgestellten Dokuments. Dieser Vorgang nutzt das verbundene [AI](../../)-Modell zum Prüfen der Grammatik des Dokuments.

```cpp
virtual System::SharedPtr<Aspose::Words::Document> Aspose::Words::AI::AiModel::CheckGrammar(System::SharedPtr<Aspose::Words::Document> sourceDocument, System::SharedPtr<Aspose::Words::AI::CheckGrammarOptions> options=nullptr)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| sourceDocument | System::SharedPtr\<Aspose::Words::Document\> | Das Dokument, dessen Grammatik geprüft wird. |
| options | System::SharedPtr\<Aspose::Words::AI::CheckGrammarOptions\> | Optionale Einstellungen zur Steuerung, wie die Grammatik geprüft wird. |

### ReturnValue

Ein neues [Document](../../../aspose.words/document/) mit geprüfter Grammatik.

## Beispiele



Zeigt, wie die Grammatik eines Dokuments überprüft wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
// Verwenden Sie generative Sprachmodelle von OpenAI.
System::SharedPtr<Aspose::Words::AI::AiModel> model = Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::Gpt4OMini)->WithApiKey(apiKey);

auto grammarOptions = System::MakeObject<Aspose::Words::AI::CheckGrammarOptions>();
grammarOptions->set_ImproveStylistics(true);

System::SharedPtr<Aspose::Words::Document> proofedDoc = model->CheckGrammar(doc, grammarOptions);
proofedDoc->Save(get_ArtifactsDir() + u"AI.AiGrammar.docx");
```

## Siehe auch

* Class [Document](../../../aspose.words/document/)
* Class [CheckGrammarOptions](../../checkgrammaroptions/)
* Class [AiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
