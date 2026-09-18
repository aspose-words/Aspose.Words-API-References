---
title: "Aspose::Words::AI::CheckGrammarOptions Klasse"
linktitle: "CheckGrammarOptions"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::AI::CheckGrammarOptions Klasse. Ermöglicht das Angeben verschiedener Optionen beim Überprüfen der Grammatik eines Dokuments mit AI in C++."
type: docs
weight: 1500
url: /de/cpp/aspose.words.ai/checkgrammaroptions/
---
## CheckGrammarOptions class


Ermöglicht das Angeben verschiedener Optionen beim Überprüfen der Grammatik eines Dokuments mit [AI](../).

```cpp
class CheckGrammarOptions : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [CheckGrammarOptions](./checkgrammaroptions/)() |  |
| [get_ImproveStylistics](./get_improvestylistics/)() const | Ermöglicht die Angabe, dass [AI](../) versuchen wird, die Stilistik des zu prüfenden Textes zu verbessern. Standardwert ist **false**. |
| [get_MakeRevisions](./get_makerevisions/)() const | Ermöglicht die Angabe, ob das endgültige oder überarbeitete Dokument mit korrigiertem Text zurückgegeben werden soll. Standardwert ist **false**. |
| [get_PreserveFormatting](./get_preserveformatting/)() const | Ermöglicht die Angabe, ob [CheckGrammar()](../aimodel/checkgrammar/) versucht, das Layout und die Formatierung des Originaldokuments beizubehalten, oder nicht. Der Standardwert ist **true**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ImproveStylistics](./set_improvestylistics/)(bool) | Ermöglicht die Angabe, dass [AI](../) versuchen wird, die Stilistik des zu prüfenden Textes zu verbessern. Standardwert ist **false**. |
| [set_MakeRevisions](./set_makerevisions/)(bool) | Ermöglicht die Angabe, ob das endgültige oder überarbeitete Dokument mit korrigiertem Text zurückgegeben werden soll. Standardwert ist **false**. |
| [set_PreserveFormatting](./set_preserveformatting/)(bool) | Ermöglicht die Angabe, ob [CheckGrammar()](../aimodel/checkgrammar/) versucht, das Layout und die Formatierung des Originaldokuments beizubehalten, oder nicht. Der Standardwert ist **true**. |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::AI](../)
* Library [Aspose.Words for C++](../../)
