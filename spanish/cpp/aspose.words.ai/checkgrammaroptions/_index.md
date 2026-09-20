---
title: "Clase Aspose::Words::AI::CheckGrammarOptions"
linktitle: "CheckGrammarOptions"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::AI::CheckGrammarOptions. Permite especificar varias opciones al comprobar la gramática de un documento usando AI en C++."
type: docs
weight: 1500
url: /es/cpp/aspose.words.ai/checkgrammaroptions/
---
## CheckGrammarOptions class


Permite especificar varias opciones al comprobar la gramática de un documento usando [AI](../).

```cpp
class CheckGrammarOptions : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [CheckGrammarOptions](./checkgrammaroptions/)() |  |
| [get_ImproveStylistics](./get_improvestylistics/)() const | Permite especificar que [AI](../) intentará mejorar la estilística del texto revisado. El valor predeterminado es **false**. |
| [get_MakeRevisions](./get_makerevisions/)() const | Permite especificar si se devuelve el documento final o revisado con el texto corregido. El valor predeterminado es **false**. |
| [get_PreserveFormatting](./get_preserveformatting/)() const | Permite especificar si [CheckGrammar()](../aimodel/checkgrammar/) intentará preservar el diseño y formato del documento original, o no. El valor predeterminado es **true**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ImproveStylistics](./set_improvestylistics/)(bool) | Permite especificar que [AI](../) intentará mejorar la estilística del texto revisado. El valor predeterminado es **false**. |
| [set_MakeRevisions](./set_makerevisions/)(bool) | Permite especificar si se devuelve el documento final o revisado con el texto corregido. El valor predeterminado es **false**. |
| [set_PreserveFormatting](./set_preserveformatting/)(bool) | Permite especificar si [CheckGrammar()](../aimodel/checkgrammar/) intentará preservar el diseño y formato del documento original, o no. El valor predeterminado es **true**. |
| static [Type](./type/)() |  |

## Ejemplos



Muestra cómo comprobar la gramática de un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
// Utiliza modelos de lenguaje generativo de OpenAI.
System::SharedPtr<Aspose::Words::AI::AiModel> model = Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::Gpt4OMini)->WithApiKey(apiKey);

auto grammarOptions = System::MakeObject<Aspose::Words::AI::CheckGrammarOptions>();
grammarOptions->set_ImproveStylistics(true);

System::SharedPtr<Aspose::Words::Document> proofedDoc = model->CheckGrammar(doc, grammarOptions);
proofedDoc->Save(get_ArtifactsDir() + u"AI.AiGrammar.docx");
```

## Ver también

* Namespace [Aspose::Words::AI](../)
* Library [Aspose.Words for C++](../../)
