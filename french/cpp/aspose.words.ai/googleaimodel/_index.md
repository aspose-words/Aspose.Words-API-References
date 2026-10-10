---
title: "Aspose::Words::AI::GoogleAiModel classe"
linktitle: "GoogleAiModel"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::AI::GoogleAiModel classe. Classe représentant l'intégration des modèles Google AI (Gemini) au sein d'Aspose.Words en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.ai/googleaimodel/
---
## GoogleAiModel class


Classe représentant l'intégration des modèles Google [AI](../) (Gemini) au sein de [Aspose.Words](../../aspose.words/).

```cpp
class GoogleAiModel : public Aspose::Words::AI::AiModel
```

## Méthodes

| Méthode | Description |
| --- | --- |
| virtual [CheckGrammar](../aimodel/checkgrammar/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::CheckGrammarOptions\>) | Vérifie la grammaire du document fourni. Cette opération exploite le modèle [AI](../) connecté pour vérifier la grammaire du document. |
| static [Create](../aimodel/create/)(Aspose::Words::AI::AiModelType) | Crée une nouvelle instance de la classe [AiModel](../aimodel/). |
| [get_Timeout](../aimodel/get_timeout/)() const | Obtient ou définit le nombre de millisecondes à attendre avant que la requête au modèle [AI](../) n'expire. La valeur par défaut est de 100 000 millisecondes (100 secondes). |
| [get_Url](./get_url/)() override | Obtient une URL du modèle. La valeur par défaut est "https://generativelanguage.googleapis.com/v1beta/models/". |
| [GetType](./gettype/)() const override |  |
| [GoogleAiModel](./googleaimodel/)(const System::String\&) | Initialise une nouvelle instance de la classe [GoogleAiModel](./). |
| [GoogleAiModel](./googleaimodel/)(const System::String\&, const System::String\&) | Initialise une nouvelle instance de la classe [GoogleAiModel](./). |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Timeout](../aimodel/set_timeout/)(int32_t) | Définisseur pour [Aspose::Words::AI::AiModel::get_Timeout](../aimodel/get_timeout/). |
| [set_Url](./set_url/)(System::String) override | Définit une URL du modèle. La valeur par défaut est "https://generativelanguage.googleapis.com/v1beta/models/". |
| [Summarize](./summarize/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) override | Résume l'objet [Document](../../aspose.words/document/) spécifié. |
| [Summarize](./summarize/)(System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) override | Résume les objets [Document](../../aspose.words/document/) spécifiés. |
| [Translate](./translate/)(System::SharedPtr\<Aspose::Words::Document\>, Aspose::Words::AI::Language) override | Traduit un document spécifié. |
| static [Type](./type/)() |  |
| [WithApiKey](../aimodel/withapikey/)(const System::String\&) | Définit une clé API spécifiée pour le modèle. |

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


Montre comment utiliser le modèle [AI](../) de Google.
```cpp
System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
auto model = System::MakeObject<Aspose::Words::AI::GoogleAiModel>(u"gemini-flash-latest", apiKey);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");
auto summarizeOptions = System::MakeObject<Aspose::Words::AI::SummarizeOptions>();
summarizeOptions->set_SummaryLength(Aspose::Words::AI::SummaryLength::VeryShort);
System::SharedPtr<Aspose::Words::Document> summary = model->Summarize(doc, summarizeOptions);
```

## Voir aussi

* Class [AiModel](../aimodel/)
* Namespace [Aspose::Words::AI](../)
* Library [Aspose.Words for C++](../../)
