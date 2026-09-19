---
title: "Metodo Aspose::Words::AI::OpenAiModel::WithOrganization"
linktitle: "WithOrganization"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::AI::OpenAiModel::WithOrganization. Imposta un'Organizzazione specificata per il modello in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.ai/openaimodel/withorganization/
---
## OpenAiModel::WithOrganization method


Imposta un'Organizzazione specificata al modello.

```cpp
System::SharedPtr<Aspose::Words::AI::OpenAiModel> Aspose::Words::AI::OpenAiModel::WithOrganization(const System::String &organizationId)
```


## Esempi



Mostra come riassumere il testo utilizzando i modelli OpenAI e Google.
```cpp
auto firstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");
auto secondDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
// Utilizza i modelli di linguaggio generativo OpenAI o Google.
System::SharedPtr<Aspose::Words::AI::AiModel> model = (System::ExplicitCast<Aspose::Words::AI::OpenAiModel>(Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::Gpt4OMini)->WithApiKey(apiKey)))->WithOrganization(u"Organization")->WithProject(u"Project");

auto options = System::MakeObject<Aspose::Words::AI::SummarizeOptions>();

options->set_SummaryLength(Aspose::Words::AI::SummaryLength::Short);
System::SharedPtr<Aspose::Words::Document> oneDocumentSummary = model->Summarize(firstDoc, options);
oneDocumentSummary->Save(get_ArtifactsDir() + u"AI.AiSummarize.One.docx");

options->set_SummaryLength(Aspose::Words::AI::SummaryLength::Long);
System::SharedPtr<Aspose::Words::Document> multiDocumentSummary = model->Summarize(System::MakeArray<System::SharedPtr<Aspose::Words::Document>>({firstDoc, secondDoc}), options);
multiDocumentSummary->Save(get_ArtifactsDir() + u"AI.AiSummarize.Multi.docx");
```

## Vedi anche

* Class [OpenAiModel](../)
* Class [OpenAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
