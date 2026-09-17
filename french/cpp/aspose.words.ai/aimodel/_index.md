---
title: "Classe Aspose::Words::AI::AiModel"
linktitle: "AiModel"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Classe Aspose::Words::AI::AiModel. Une classe abstraite représentant l'intégration avec divers modèles d'IA au sein d'Aspose.Words en C++."
type: docs
weight: 1000
url: /fr/cpp/aspose.words.ai/aimodel/
---
## AiModel class


Une classe abstraite représentant l'intégration avec divers modèles [AI](../) au sein de [Aspose.Words](../../aspose.words/).

```cpp
class AiModel : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| virtual [CheckGrammar](./checkgrammar/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::CheckGrammarOptions\>) | Vérifie la grammaire du document fourni. Cette opération exploite le modèle [AI](../) connecté pour vérifier la grammaire du document. |
| static [Create](./create/)(Aspose::Words::AI::AiModelType) | Crée une nouvelle instance de la classe [AiModel](./). |
| [get_Timeout](./get_timeout/)() const | Obtient ou définit le nombre de millisecondes à attendre avant que la requête au modèle [AI](../) n'expire. La valeur par défaut est de 100 000 millisecondes (100 secondes). |
| virtual [get_Url](./get_url/)() | Obtient ou définit l'URL du modèle. La valeur par défaut est spécifique au modèle. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Timeout](./set_timeout/)(int32_t) | Définisseur pour [Aspose::Words::AI::AiModel::get_Timeout](./get_timeout/). |
| virtual [set_Url](./set_url/)(System::String) | Définisseur pour [Aspose::Words::AI::AiModel::get_Url](./get_url/). |
| virtual [Summarize](./summarize/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) | Génère un résumé du document spécifié, avec des options pour ajuster la longueur du résumé. Cette opération exploite le modèle [AI](../) connecté pour le traitement du contenu. |
| virtual [Summarize](./summarize/)(System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) | Génère des résumés pour un tableau de documents, avec des options pour contrôler la longueur du résumé et d'autres paramètres. Cette méthode utilise le modèle [AI](../) connecté pour traiter chaque document du tableau. |
| virtual [Translate](./translate/)(System::SharedPtr\<Aspose::Words::Document\>, Aspose::Words::AI::Language) | Traduit le document fourni dans la langue cible spécifiée. Cette opération exploite le modèle [AI](../) connecté pour la traduction du contenu. |
| static [Type](./type/)() |  |
| [WithApiKey](./withapikey/)(const System::String\&) | Définit une clé API spécifiée pour le modèle. |

## Exemples



Montre comment résumer du texte en utilisant les modèles OpenAI et Google.
```cpp
auto firstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");
auto secondDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
// Utilisez les modèles de langage génératif OpenAI ou Google.
System::SharedPtr<Aspose::Words::AI::AiModel> model = (System::ExplicitCast<Aspose::Words::AI::OpenAiModel>(Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::Gpt4OMini)->WithApiKey(apiKey)))->WithOrganization(u"Organization")->WithProject(u"Project");

auto options = System::MakeObject<Aspose::Words::AI::SummarizeOptions>();

options->set_SummaryLength(Aspose::Words::AI::SummaryLength::Short);
System::SharedPtr<Aspose::Words::Document> oneDocumentSummary = model->Summarize(firstDoc, options);
oneDocumentSummary->Save(get_ArtifactsDir() + u"AI.AiSummarize.One.docx");

options->set_SummaryLength(Aspose::Words::AI::SummaryLength::Long);
System::SharedPtr<Aspose::Words::Document> multiDocumentSummary = model->Summarize(System::MakeArray<System::SharedPtr<Aspose::Words::Document>>({firstDoc, secondDoc}), options);
multiDocumentSummary->Save(get_ArtifactsDir() + u"AI.AiSummarize.Multi.docx");
```

## Voir aussi

* Namespace [Aspose::Words::AI](../)
* Library [Aspose.Words for C++](../../)
