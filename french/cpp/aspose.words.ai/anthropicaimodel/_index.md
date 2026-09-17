---
title: "classe Aspose::Words::AI::AnthropicAiModel"
linktitle: "AnthropicAiModel"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "classe Aspose::Words::AI::AnthropicAiModel. Une classe abstraite représentant l'intégration avec les modèles d'AI d'Anthropic au sein d'Aspose.Words en C++."
type: docs
weight: 1250
url: /fr/cpp/aspose.words.ai/anthropicaimodel/
---
## AnthropicAiModel class


Une classe abstraite représentant l'intégration avec les modèles d'[AI](../) d'Anthropic au sein de [Aspose.Words](../../aspose.words/).

```cpp
class AnthropicAiModel : public Aspose::Words::AI::AiModel
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [AnthropicAiModel](./anthropicaimodel/)() |  |
| virtual [CheckGrammar](../aimodel/checkgrammar/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::CheckGrammarOptions\>) | Vérifie la grammaire du document fourni. Cette opération exploite le modèle [AI](../) connecté pour vérifier la grammaire du document. |
| static [Create](../aimodel/create/)(Aspose::Words::AI::AiModelType) | Crée une nouvelle instance de la classe [AiModel](../aimodel/). |
| [get_Timeout](../aimodel/get_timeout/)() const | Obtient ou définit le nombre de millisecondes à attendre avant que la requête au modèle [AI](../) n'expire. La valeur par défaut est de 100 000 millisecondes (100 secondes). |
| [get_Url](./get_url/)() override | Obtient l'URL du modèle. La valeur par défaut est "https://api.anthropic.com/". |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Timeout](../aimodel/set_timeout/)(int32_t) | Définisseur pour [Aspose::Words::AI::AiModel::get_Timeout](../aimodel/get_timeout/). |
| [set_Url](./set_url/)(System::String) override | Définit l'URL du modèle. La valeur par défaut est "https://api.anthropic.com/". |
| [Summarize](./summarize/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) override | Génère un résumé du document spécifié, avec des options pour ajuster la longueur du résumé. Cette opération exploite le modèle [AI](../) connecté pour le traitement du contenu. |
| [Summarize](./summarize/)(System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) override | Génère des résumés pour un tableau de documents, avec des options pour contrôler la longueur du résumé et d'autres paramètres. Cette méthode utilise le modèle [AI](../) connecté pour traiter chaque document du tableau. |
| [Translate](./translate/)(System::SharedPtr\<Aspose::Words::Document\>, Aspose::Words::AI::Language) override | Traduit le document fourni dans la langue cible spécifiée. Cette opération exploite le modèle [AI](../) connecté pour la traduction du contenu. |
| static [Type](./type/)() |  |
| [WithApiKey](../aimodel/withapikey/)(const System::String\&) | Définit une clé API spécifiée pour le modèle. |
## Voir aussi

* Class [AiModel](../aimodel/)
* Namespace [Aspose::Words::AI](../)
* Library [Aspose.Words for C++](../../)
