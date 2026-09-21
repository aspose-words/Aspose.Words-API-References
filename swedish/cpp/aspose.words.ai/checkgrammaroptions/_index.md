---
title: "Aspose::Words::AI::CheckGrammarOptions klass"
linktitle: "CheckGrammarOptions"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::AI::CheckGrammarOptions klass. Tillåter att ange olika alternativ när grammatikkontrollen av ett dokument utförs med AI i C++."
type: docs
weight: 1500
url: /sv/cpp/aspose.words.ai/checkgrammaroptions/
---
## CheckGrammarOptions class


Tillåter att ange olika alternativ när grammatikkontrollen av ett dokument utförs med [AI](../).

```cpp
class CheckGrammarOptions : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [CheckGrammarOptions](./checkgrammaroptions/)() |  |
| [get_ImproveStylistics](./get_improvestylistics/)() const | Tillåter att ange antingen [AI](../) kommer att försöka förbättra stilistiken i den text som korrekturläses. Standardvärdet är **false**. |
| [get_MakeRevisions](./get_makerevisions/)() const | Tillåter att specificera antingen slutgiltigt eller reviderat dokument som ska returneras med korrekturläst text. Standardvärdet är **false**. |
| [get_PreserveFormatting](./get_preserveformatting/)() const | Tillåter att specificera antingen [CheckGrammar()](../aimodel/checkgrammar/) kommer att försöka bevara layout och formatering av originaldokumentet, eller inte. Standardvärdet är **true**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ImproveStylistics](./set_improvestylistics/)(bool) | Tillåter att ange antingen [AI](../) kommer att försöka förbättra stilistiken i den text som korrekturläses. Standardvärdet är **false**. |
| [set_MakeRevisions](./set_makerevisions/)(bool) | Tillåter att specificera antingen slutgiltigt eller reviderat dokument som ska returneras med korrekturläst text. Standardvärdet är **false**. |
| [set_PreserveFormatting](./set_preserveformatting/)(bool) | Tillåter att specificera antingen [CheckGrammar()](../aimodel/checkgrammar/) kommer att försöka bevara layout och formatering av originaldokumentet, eller inte. Standardvärdet är **true**. |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::AI](../)
* Library [Aspose.Words for C++](../../)
