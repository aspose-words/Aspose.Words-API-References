---
title: "Aspose::Words::AI::GoogleAiModel classe"
linktitle: "GoogleAiModel"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::AI::GoogleAiModel classe. Classe che rappresenta l'integrazione dei Google AI Models (Gemini) all'interno di Aspose.Words in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.ai/googleaimodel/
---
## GoogleAiModel class


Classe che rappresenta l'integrazione dei Google [AI](../) Models (Gemini) all'interno di [Aspose.Words](../../aspose.words/).

```cpp
class GoogleAiModel : public Aspose::Words::AI::AiModel
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| virtual [CheckGrammar](../aimodel/checkgrammar/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::CheckGrammarOptions\>) | Controlla la grammatica del documento fornito. Questa operazione utilizza il modello [AI](../) connesso per il controllo grammaticale del documento. |
| static [Create](../aimodel/create/)(Aspose::Words::AI::AiModelType) | Crea una nuova istanza della classe [AiModel](../aimodel/). |
| [get_Timeout](../aimodel/get_timeout/)() const | Ottiene o imposta il numero di millisecondi da attendere prima che la richiesta al modello [AI](../) scada. Il valore predefinito è 100.000 millisecondi (100 secondi). |
| [get_Url](./get_url/)() override | Ottiene un URL del modello. Il valore predefinito è "https://generativelanguage.googleapis.com/v1beta/models/". |
| [GetType](./gettype/)() const override |  |
| [GoogleAiModel](./googleaimodel/)(const System::String\&) | Inizializza una nuova istanza della classe [GoogleAiModel](./). |
| [GoogleAiModel](./googleaimodel/)(const System::String\&, const System::String\&) | Inizializza una nuova istanza della classe [GoogleAiModel](./). |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Timeout](../aimodel/set_timeout/)(int32_t) | Impostatore per [Aspose::Words::AI::AiModel::get_Timeout](../aimodel/get_timeout/). |
| [set_Url](./set_url/)(System::String) override | Imposta un URL del modello. Il valore predefinito è "https://generativelanguage.googleapis.com/v1beta/models/". |
| [Summarize](./summarize/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) override | Riassume l'oggetto [Document](../../aspose.words/document/) specificato. |
| [Summarize](./summarize/)(System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) override | Riassume gli oggetti [Document](../../aspose.words/document/) specificati. |
| [Translate](./translate/)(System::SharedPtr\<Aspose::Words::Document\>, Aspose::Words::AI::Language) override | Traduce un documento specificato. |
| static [Type](./type/)() |  |
| [WithApiKey](../aimodel/withapikey/)(const System::String\&) | Imposta una chiave API specificata sul modello. |

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


Mostra come utilizzare il modello google [AI](../).
```cpp
System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
auto model = System::MakeObject<Aspose::Words::AI::GoogleAiModel>(u"gemini-flash-latest", apiKey);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");
auto summarizeOptions = System::MakeObject<Aspose::Words::AI::SummarizeOptions>();
summarizeOptions->set_SummaryLength(Aspose::Words::AI::SummaryLength::VeryShort);
System::SharedPtr<Aspose::Words::Document> summary = model->Summarize(doc, summarizeOptions);
```

## Vedi anche

* Class [AiModel](../aimodel/)
* Namespace [Aspose::Words::AI](../)
* Library [Aspose.Words for C++](../../)
