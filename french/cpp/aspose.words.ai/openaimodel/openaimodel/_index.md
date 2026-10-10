---
title: "Constructeur Aspose::Words::AI::OpenAiModel::OpenAiModel"
linktitle: "OpenAiModel"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Constructeur Aspose::Words::AI::OpenAiModel::OpenAiModel. Initialise une nouvelle instance de la classe OpenAiModel en C++."
type: docs
weight: 1334
url: /fr/cpp/aspose.words.ai/openaimodel/openaimodel/
---
## OpenAiModel::OpenAiModel(const System::String\&) constructor


Initialise une nouvelle instance de la classe [OpenAiModel](../).

```cpp
Aspose::Words::AI::OpenAiModel::OpenAiModel(const System::String &name)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| name | const System::String\& | Le nom du modèle. Par exemple, gpt-5.2-chat-latest. |

## Voir aussi

* Class [OpenAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
## OpenAiModel::OpenAiModel(const System::String\&, const System::String\&) constructor


Initialise une nouvelle instance de la classe [OpenAiModel](../).

```cpp
Aspose::Words::AI::OpenAiModel::OpenAiModel(const System::String &name, const System::String &apiKey)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| name | const System::String\& | Le nom du modèle. Par exemple, gpt-5.2-chat-latest. |
| apiKey | const System::String\& | La clé API pour utiliser l'API OpenAi. |

## Exemples



Montre comment créer une instance de modèle OpenAI directement en utilisant une clé API et le nom du modèle.
```cpp
System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
// Créez une instance de modèle OpenAI en utilisant le constructeur avec le nom du modèle et la clé API.
auto model = System::MakeObject<Aspose::Words::AI::OpenAiModel>(u"gpt-4o-mini", apiKey);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");
// Résumez le document en utilisant le modèle OpenAI avec une longueur de résumé courte.
auto summarizeOptions = System::MakeObject<Aspose::Words::AI::SummarizeOptions>();
summarizeOptions->set_SummaryLength(Aspose::Words::AI::SummaryLength::VeryShort);
System::SharedPtr<Aspose::Words::Document> summary = model->Summarize(doc, summarizeOptions);

summary->Save(get_ArtifactsDir() + u"OpenAiModel.OpenAiModelConstructor.docx");
```

## Voir aussi

* Class [OpenAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
