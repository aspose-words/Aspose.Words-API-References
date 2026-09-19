---
title: "Enum Aspose::Words::AI::SummaryLength"
linktitle: "SummaryLength"
second_title: "Riferimento API Aspose.Words per C++"
description: "Enum Aspose::Words::AI::SummaryLength. Elenca le possibili lunghezze del riepilogo in C++."
type: docs
weight: 7000
url: /it/cpp/aspose.words.ai/summarylength/
---
## SummaryLength enum


Enumera le possibili lunghezze del riassunto.

```cpp
enum class SummaryLength
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| VeryShort | 0 | Prova a generare 1-2 frasi. |
| Short | 1 | Prova a generare 3-4 frasi. |
| Medium | 2 | Prova a generare 5-6 frasi. |
| Long | 3 | Prova a generare 7-10 frasi. |
| VeryLong | 4 | Prova a generare 11-20 frasi. |


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

* Namespace [Aspose::Words::AI](../)
* Library [Aspose.Words for C++](../../)
