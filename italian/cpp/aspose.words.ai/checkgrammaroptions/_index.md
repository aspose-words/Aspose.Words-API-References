---
title: "Aspose::Words::AI::CheckGrammarOptions class"
linktitle: "CheckGrammarOptions"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::AI::CheckGrammarOptions class. Consente di specificare varie opzioni durante il controllo grammaticale di un documento usando l'AI in C++."
type: docs
weight: 1500
url: /it/cpp/aspose.words.ai/checkgrammaroptions/
---
## CheckGrammarOptions class


Consente di specificare varie opzioni durante il controllo grammaticale di un documento usando [AI](../).

```cpp
class CheckGrammarOptions : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [CheckGrammarOptions](./checkgrammaroptions/)() |  |
| [get_ImproveStylistics](./get_improvestylistics/)() const | Consente di specificare se [AI](../) cercherà di migliorare lo stile del testo revisionato. Il valore predefinito è **false**. |
| [get_MakeRevisions](./get_makerevisions/)() const | Consente di specificare se restituire il documento finale o revisionato con il testo corretto. Il valore predefinito è **false**. |
| [get_PreserveFormatting](./get_preserveformatting/)() const | Consente di specificare se [CheckGrammar()](../aimodel/checkgrammar/) cercherà di preservare il layout e la formattazione del documento originale, o meno. Il valore predefinito è **true**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ImproveStylistics](./set_improvestylistics/)(bool) | Consente di specificare se [AI](../) cercherà di migliorare lo stile del testo revisionato. Il valore predefinito è **false**. |
| [set_MakeRevisions](./set_makerevisions/)(bool) | Consente di specificare se restituire il documento finale o revisionato con il testo corretto. Il valore predefinito è **false**. |
| [set_PreserveFormatting](./set_preserveformatting/)(bool) | Consente di specificare se [CheckGrammar()](../aimodel/checkgrammar/) cercherà di preservare il layout e la formattazione del documento originale, o meno. Il valore predefinito è **true**. |
| static [Type](./type/)() |  |

## Esempi



Mostra come controllare la grammatica di un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
// Utilizza i modelli di linguaggio generativi di OpenAI.
System::SharedPtr<Aspose::Words::AI::AiModel> model = Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::Gpt4OMini)->WithApiKey(apiKey);

auto grammarOptions = System::MakeObject<Aspose::Words::AI::CheckGrammarOptions>();
grammarOptions->set_ImproveStylistics(true);

System::SharedPtr<Aspose::Words::Document> proofedDoc = model->CheckGrammar(doc, grammarOptions);
proofedDoc->Save(get_ArtifactsDir() + u"AI.AiGrammar.docx");
```

## Vedi anche

* Namespace [Aspose::Words::AI](../)
* Library [Aspose.Words for C++](../../)
