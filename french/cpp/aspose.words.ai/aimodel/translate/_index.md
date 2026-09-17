---
title: "Méthode Aspose::Words::AI::AiModel::Translate"
linktitle: "Traduire"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::AI::AiModel::Translate. Traduit le document fourni dans la langue cible spécifiée. Cette opération exploite le modèle d'IA connecté pour la traduction de contenu en C++."
type: docs
weight: 4667
url: /fr/cpp/aspose.words.ai/aimodel/translate/
---
## AiModel::Translate method


Traduit le document fourni dans la langue cible spécifiée. Cette opération utilise le modèle [AI](../../) connecté pour la traduction de contenu.

```cpp
virtual System::SharedPtr<Aspose::Words::Document> Aspose::Words::AI::AiModel::Translate(System::SharedPtr<Aspose::Words::Document> sourceDocument, Aspose::Words::AI::Language targetLanguage)=0
```


| Paramètre | Type | Description |
| --- | --- | --- |
| sourceDocument | System::SharedPtr\<Aspose::Words::Document\> | Le document à traduire. |
| targetLanguage | Aspose::Words::AI::Language | La langue dans laquelle le document sera traduit. |

### ReturnValue

Un nouvel objet [Document](../../../aspose.words/document/) contenant le document traduit.

## Exemples



Montre comment traduire du texte en utilisant les modèles Google.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
// Utilisez les modèles de langage génératif de Google.
System::SharedPtr<Aspose::Words::AI::AiModel> model = Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::GeminiFlashLatest)->WithApiKey(apiKey);

System::SharedPtr<Aspose::Words::Document> translatedDoc = model->Translate(doc, Aspose::Words::AI::Language::Arabic);
translatedDoc->Save(get_ArtifactsDir() + u"AI.AiTranslate.docx");
```

## Voir aussi

* Class [Document](../../../aspose.words/document/)
* Enum [Language](../../language/)
* Class [AiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
