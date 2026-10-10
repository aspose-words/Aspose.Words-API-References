---
title: "Méthode Aspose::Words::AI::AiModel::CheckGrammar"
linktitle: "CheckGrammar"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::AI::AiModel::CheckGrammar. Vérifie la grammaire du document fourni. Cette opération utilise le modèle AI connecté pour vérifier la grammaire du document en C++."
type: docs
weight: 2500
url: /fr/cpp/aspose.words.ai/aimodel/checkgrammar/
---
## AiModel::CheckGrammar method


Vérifie la grammaire du document fourni. Cette opération utilise le modèle [AI](../../) connecté pour vérifier la grammaire du document.

```cpp
virtual System::SharedPtr<Aspose::Words::Document> Aspose::Words::AI::AiModel::CheckGrammar(System::SharedPtr<Aspose::Words::Document> sourceDocument, System::SharedPtr<Aspose::Words::AI::CheckGrammarOptions> options=nullptr)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| sourceDocument | System::SharedPtr\<Aspose::Words::Document\> | Le document dont la grammaire est vérifiée. |
| options | System::SharedPtr\<Aspose::Words::AI::CheckGrammarOptions\> | Paramètres optionnels pour contrôler la façon dont la grammaire sera vérifiée. |

### ReturnValue

Un nouveau [Document](../../../aspose.words/document/) avec la grammaire vérifiée.

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

* Class [Document](../../../aspose.words/document/)
* Class [CheckGrammarOptions](../../checkgrammaroptions/)
* Class [AiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
