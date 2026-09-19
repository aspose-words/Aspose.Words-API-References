---
title: "Aspose::Words::AI::AnthropicAiModel class"
linktitle: "AnthropicAiModel"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::AI::AnthropicAiModel class. Una classe astratta che rappresenta l'integrazione con i modelli AI di Anthropic all'interno di Aspose.Words in C++."
type: docs
weight: 1250
url: /it/cpp/aspose.words.ai/anthropicaimodel/
---
## AnthropicAiModel class


Una classe astratta che rappresenta l'integrazione con i modelli [AI](../) di Anthropic all'interno di [Aspose.Words](../../aspose.words/).

```cpp
class AnthropicAiModel : public Aspose::Words::AI::AiModel
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [AnthropicAiModel](./anthropicaimodel/)() |  |
| virtual [CheckGrammar](../aimodel/checkgrammar/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::CheckGrammarOptions\>) | Controlla la grammatica del documento fornito. Questa operazione utilizza il modello [AI](../) connesso per il controllo grammaticale del documento. |
| static [Create](../aimodel/create/)(Aspose::Words::AI::AiModelType) | Crea una nuova istanza della classe [AiModel](../aimodel/). |
| [get_Timeout](../aimodel/get_timeout/)() const | Ottiene o imposta il numero di millisecondi da attendere prima che la richiesta al modello [AI](../) scada. Il valore predefinito è 100.000 millisecondi (100 secondi). |
| [get_Url](./get_url/)() override | Ottiene un URL del modello. Il valore predefinito è "https://api.anthropic.com/". |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Timeout](../aimodel/set_timeout/)(int32_t) | Impostatore per [Aspose::Words::AI::AiModel::get_Timeout](../aimodel/get_timeout/). |
| [set_Url](./set_url/)(System::String) override | Imposta un URL del modello. Il valore predefinito è "https://api.anthropic.com/". |
| [Summarize](./summarize/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) override | Genera un riepilogo del documento specificato, con opzioni per regolare la lunghezza del riepilogo. Questa operazione utilizza il modello [AI](../) connesso per l'elaborazione del contenuto. |
| [Summarize](./summarize/)(System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) override | Genera riepiloghi per un array di documenti, con opzioni per controllare la lunghezza del riepilogo e altre impostazioni. Questo metodo utilizza il modello [AI](../) connesso per elaborare ciascun documento nell'array. |
| [Translate](./translate/)(System::SharedPtr\<Aspose::Words::Document\>, Aspose::Words::AI::Language) override | Traduce il documento fornito nella lingua di destinazione specificata. Questa operazione utilizza il modello [AI](../) connesso per la traduzione del contenuto. |
| static [Type](./type/)() |  |
| [WithApiKey](../aimodel/withapikey/)(const System::String\&) | Imposta una chiave API specificata sul modello. |
## Vedi anche

* Class [AiModel](../aimodel/)
* Namespace [Aspose::Words::AI](../)
* Library [Aspose.Words for C++](../../)
