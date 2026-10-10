---
title: "classe Aspose::Words::AI::SummarizeOptions"
linktitle: "SummarizeOptions"
second_title: "Riferimento API Aspose.Words per C++"
description: "classe Aspose::Words::AI::SummarizeOptions. Consente di specificare varie opzioni per riassumere il contenuto del documento in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.ai/summarizeoptions/
---
## SummarizeOptions class


Consente di specificare varie opzioni per riassumere il contenuto del documento.

```cpp
class SummarizeOptions : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_SummaryLength](./get_summarylength/)() const | Consente di specificare la lunghezza del riassunto. Il valore predefinito è [Medium](../summarylength/). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_SummaryLength](./set_summarylength/)(Aspose::Words::AI::SummaryLength) | Metodo setter per [Aspose::Words::AI::SummarizeOptions::get_SummaryLength](./get_summarylength/). |
| [SummarizeOptions](./summarizeoptions/)() | Inizializza una nuova istanza della classe [SummarizeOptions](./). |
| static [Type](./type/)() |  |

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
