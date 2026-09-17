---
title: "Aspose::Words::AI::GoogleAiModel::GoogleAiModel constructeur"
linktitle: "GoogleAiModel"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::AI::GoogleAiModel::GoogleAiModel constructeur. Initialise une nouvelle instance de la classe GoogleAiModel en C++."
type: docs
weight: 1500
url: /fr/cpp/aspose.words.ai/googleaimodel/googleaimodel/
---
## GoogleAiModel::GoogleAiModel(const System::String\&) constructor


Initialise une nouvelle instance de la classe [GoogleAiModel](../).

```cpp
Aspose::Words::AI::GoogleAiModel::GoogleAiModel(const System::String &name)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| name | const System::String\& | Le nom du modèle. Par exemple, gemini-2.5-flash. |

## Exemples



Montre comment utiliser le modèle [AI](../../) de Google.
```cpp
System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
auto model = System::MakeObject<Aspose::Words::AI::GoogleAiModel>(u"gemini-flash-latest", apiKey);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");
auto summarizeOptions = System::MakeObject<Aspose::Words::AI::SummarizeOptions>();
summarizeOptions->set_SummaryLength(Aspose::Words::AI::SummaryLength::VeryShort);
System::SharedPtr<Aspose::Words::Document> summary = model->Summarize(doc, summarizeOptions);
```

## Voir aussi

* Class [GoogleAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
## GoogleAiModel::GoogleAiModel(const System::String\&, const System::String\&) constructor


Initialise une nouvelle instance de la classe [GoogleAiModel](../).

```cpp
Aspose::Words::AI::GoogleAiModel::GoogleAiModel(const System::String &name, const System::String &apiKey)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| name | const System::String\& | Le nom du modèle. Par exemple, gemini-2.5-flash. |
| apiKey | const System::String\& | La clé API pour utiliser l'API Gemini. Veuillez vous référer à [https://ai.google.dev/gemini-api/docs/api-key](https://ai.google.dev/gemini-api/docs/api-key) pour plus de détails. |

## Exemples



Montre comment utiliser le modèle [AI](../../) de Google.
```cpp
System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
auto model = System::MakeObject<Aspose::Words::AI::GoogleAiModel>(u"gemini-flash-latest", apiKey);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");
auto summarizeOptions = System::MakeObject<Aspose::Words::AI::SummarizeOptions>();
summarizeOptions->set_SummaryLength(Aspose::Words::AI::SummaryLength::VeryShort);
System::SharedPtr<Aspose::Words::Document> summary = model->Summarize(doc, summarizeOptions);
```

## Voir aussi

* Class [GoogleAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
