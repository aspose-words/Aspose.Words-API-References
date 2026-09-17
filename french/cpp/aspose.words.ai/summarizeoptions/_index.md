---
title: "Aspose::Words::AI::SummarizeOptions classe"
linktitle: "SummarizeOptions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::AI::SummarizeOptions classe. Permet de spécifier diverses options pour résumer le contenu du document en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.ai/summarizeoptions/
---
## SummarizeOptions class


Permet de spécifier diverses options pour résumer le contenu du document.

```cpp
class SummarizeOptions : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_SummaryLength](./get_summarylength/)() const | Permet de spécifier la longueur du résumé. La valeur par défaut est [Medium](../summarylength/). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_SummaryLength](./set_summarylength/)(Aspose::Words::AI::SummaryLength) | Mutateur pour [Aspose::Words::AI::SummarizeOptions::get_SummaryLength](./get_summarylength/). |
| [SummarizeOptions](./summarizeoptions/)() | Initialise une nouvelle instance de la classe [SummarizeOptions](./). |
| static [Type](./type/)() |  |

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
