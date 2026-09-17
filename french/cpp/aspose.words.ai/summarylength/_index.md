---
title: "Énumération Aspose::Words::AI::SummaryLength"
linktitle: "SummaryLength"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Énumération Aspose::Words::AI::SummaryLength. Énumère les longueurs possibles du résumé en C++."
type: docs
weight: 7000
url: /fr/cpp/aspose.words.ai/summarylength/
---
## SummaryLength enum


Énumère les longueurs possibles du résumé.

```cpp
enum class SummaryLength
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| VeryShort | 0 | Essayez de générer 1 à 2 phrases. |
| Short | 1 | Essayez de générer 3 à 4 phrases. |
| Medium | 2 | Essayez de générer 5 à 6 phrases. |
| Long | 3 | Essayez de générer 7-10 phrases. |
| VeryLong | 4 | Essayez de générer 11-20 phrases. |


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
