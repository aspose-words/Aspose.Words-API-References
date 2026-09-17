---
title: "Aspose::Words::AI::AiModelType énum"
linktitle: "AiModelType"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::AI::AiModelType énum. Représente les types d'AiModel qui peuvent être intégrés au flux de traitement de documents en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words.ai/aimodeltype/
---
## AiModelType enum


Représente les types de [AiModel](../aimodel/) qui peuvent être intégrés au flux de traitement de documents.

```cpp
enum class AiModelType
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Gpt4O | 0 | Type de modèle génératif GPT-4o. |
| Gpt4OMini | 1 | Type de modèle génératif mini GPT-4o. |
| Gpt4Turbo | 2 | Type de modèle génératif GPT-4 Turbo. |
| Gpt35Turbo | 3 | Type de modèle génératif GPT-3.5 Turbo. |
| GeminiFlashLatest | 4 | Type de modèle génératif Gemini Flash de la dernière version. |
| GeminiProLatest | 6 | Type de modèle génératif Gemini Pro de la dernière version. |
| Claude35Sonnet | 7 | Claude 3.5 Sonnet type de modèle génératif. |
| Claude35Haiku | 8 | Claude 3.5 Haiku type de modèle génératif. |
| Claude3Opus | 9 | Claude 3 Opus type de modèle génératif. |
| Claude3Sonnet | 10 | Claude 3 Sonnet type de modèle génératif. |
| Claude3Haiku | 11 | Claude 3 Haiku type de modèle génératif. |


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
