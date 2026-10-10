---
title: "Aspose::Words::AI::OpenAiModel classe"
linktitle: "OpenAiModel"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::AI::OpenAiModel classe. Classe che rappresenta l'integrazione dei modelli OpenAi all'interno di Aspose.Words in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.ai/openaimodel/
---
## OpenAiModel class


Classe che rappresenta l'integrazione dei modelli OpenAi all'interno di [Aspose.Words](../../aspose.words/).

```cpp
class OpenAiModel : public Aspose::Words::AI::AiModel
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| virtual [CheckGrammar](../aimodel/checkgrammar/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::CheckGrammarOptions\>) | Controlla la grammatica del documento fornito. Questa operazione utilizza il modello [AI](../) connesso per il controllo grammaticale del documento. |
| static [Create](../aimodel/create/)(Aspose::Words::AI::AiModelType) | Crea una nuova istanza della classe [AiModel](../aimodel/). |
| [get_Timeout](../aimodel/get_timeout/)() const | Ottiene o imposta il numero di millisecondi da attendere prima che la richiesta al modello [AI](../) scada. Il valore predefinito è 100.000 millisecondi (100 secondi). |
| [get_Url](./get_url/)() override | Ottiene un URL del modello. Il valore predefinito è "https://api.openai.com/". |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [OpenAiModel](./openaimodel/)(const System::String\&, const System::String\&) | Inizializza una nuova istanza della classe [OpenAiModel](./). |
| [OpenAiModel](./openaimodel/)(const System::String\&) | Inizializza una nuova istanza della classe [OpenAiModel](./). |
| [set_Timeout](../aimodel/set_timeout/)(int32_t) | Impostatore per [Aspose::Words::AI::AiModel::get_Timeout](../aimodel/get_timeout/). |
| [set_Url](./set_url/)(System::String) override | Imposta un URL del modello. Il valore predefinito è "https://api.openai.com/". |
| [Summarize](./summarize/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) override | Genera un riepilogo del documento specificato, con opzioni per regolare la lunghezza del riepilogo. Questa operazione utilizza il modello [AI](../) connesso per l'elaborazione del contenuto. |
| [Summarize](./summarize/)(System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) override | Genera riepiloghi per un array di documenti, con opzioni per controllare la lunghezza del riepilogo e altre impostazioni. Questo metodo utilizza il modello [AI](../) connesso per elaborare ciascun documento nell'array. |
| [Translate](./translate/)(System::SharedPtr\<Aspose::Words::Document\>, Aspose::Words::AI::Language) override | Traduce il documento fornito nella lingua di destinazione specificata. Questa operazione utilizza il modello [AI](../) connesso per la traduzione del contenuto. |
| static [Type](./type/)() |  |
| [WithApiKey](../aimodel/withapikey/)(const System::String\&) | Imposta una chiave API specificata sul modello. |
| [WithOrganization](./withorganization/)(const System::String\&) | Imposta un'Organizzazione specificata al modello. |
| [WithProject](./withproject/)(const System::String\&) | Imposta un Progetto specificato al modello. |

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

* Class [AiModel](../aimodel/)
* Namespace [Aspose::Words::AI](../)
* Library [Aspose.Words for C++](../../)
