---
title: "Aspose::Words::AI::AiModelType enum"
linktitle: "AiModelType"
second_title: "Riferimento API Aspose.Words per C++"
description: "enum Aspose::Words::AI::AiModelType. Rappresenta i tipi di AiModel che possono essere integrati nel flusso di lavoro di elaborazione dei documenti in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words.ai/aimodeltype/
---
## AiModelType enum


Rappresenta i tipi di [AiModel](../aimodel/) che possono essere integrati nel flusso di lavoro di elaborazione dei documenti.

```cpp
enum class AiModelType
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Gpt4O | 0 | Tipo di modello generativo GPT-4o. |
| Gpt4OMini | 1 | Tipo di modello generativo GPT-4o mini. |
| Gpt4Turbo | 2 | Tipo di modello generativo GPT-4 Turbo. |
| Gpt35Turbo | 3 | Tipo di modello generativo GPT-3.5 Turbo. |
| GeminiFlashLatest | 4 | Tipo di modello generativo Gemini Flash ultima versione. |
| GeminiProLatest | 6 | Tipo di modello generativo Gemini Pro ultima versione. |
| Claude35Sonnet | 7 | Claude 3.5 Sonnet è un tipo di modello generativo. |
| Claude35Haiku | 8 | Claude 3.5 Haiku è un tipo di modello generativo. |
| Claude3Opus | 9 | Claude 3 Opus è un tipo di modello generativo. |
| Claude3Sonnet | 10 | Claude 3 Sonnet è un tipo di modello generativo. |
| Claude3Haiku | 11 | Claude 3 Haiku è un tipo di modello generativo. |


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
