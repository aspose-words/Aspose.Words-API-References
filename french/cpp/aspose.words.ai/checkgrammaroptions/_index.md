---
title: "classe Aspose::Words::AI::CheckGrammarOptions"
linktitle: "CheckGrammarOptions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "classe Aspose::Words::AI::CheckGrammarOptions. Permet de spécifier diverses options lors de la vérification grammaticale d'un document à l'aide de l'AI en C++."
type: docs
weight: 1500
url: /fr/cpp/aspose.words.ai/checkgrammaroptions/
---
## CheckGrammarOptions class


Permet de spécifier diverses options lors de la vérification grammaticale d'un document à l'aide de [AI](../).

```cpp
class CheckGrammarOptions : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [CheckGrammarOptions](./checkgrammaroptions/)() |  |
| [get_ImproveStylistics](./get_improvestylistics/)() const | Permet de spécifier que [AI](../) tentera d'améliorer le style du texte corrigé. La valeur par défaut est **false**. |
| [get_MakeRevisions](./get_makerevisions/)() const | Permet de spécifier que le document final ou révisé soit renvoyé avec le texte corrigé. La valeur par défaut est **false**. |
| [get_PreserveFormatting](./get_preserveformatting/)() const | Permet de spécifier que [CheckGrammar()](../aimodel/checkgrammar/) tentera de préserver la mise en page et le formatage du document original, ou non. La valeur par défaut est **true**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ImproveStylistics](./set_improvestylistics/)(bool) | Permet de spécifier que [AI](../) tentera d'améliorer le style du texte corrigé. La valeur par défaut est **false**. |
| [set_MakeRevisions](./set_makerevisions/)(bool) | Permet de spécifier que le document final ou révisé soit renvoyé avec le texte corrigé. La valeur par défaut est **false**. |
| [set_PreserveFormatting](./set_preserveformatting/)(bool) | Permet de spécifier que [CheckGrammar()](../aimodel/checkgrammar/) tentera de préserver la mise en page et le formatage du document original, ou non. La valeur par défaut est **true**. |
| static [Type](./type/)() |  |

## Exemples



Montre comment vérifier la grammaire d'un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
// Utilisez les modèles de langage génératif OpenAI.
System::SharedPtr<Aspose::Words::AI::AiModel> model = Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::Gpt4OMini)->WithApiKey(apiKey);

auto grammarOptions = System::MakeObject<Aspose::Words::AI::CheckGrammarOptions>();
grammarOptions->set_ImproveStylistics(true);

System::SharedPtr<Aspose::Words::Document> proofedDoc = model->CheckGrammar(doc, grammarOptions);
proofedDoc->Save(get_ArtifactsDir() + u"AI.AiGrammar.docx");
```

## Voir aussi

* Namespace [Aspose::Words::AI](../)
* Library [Aspose.Words for C++](../../)
