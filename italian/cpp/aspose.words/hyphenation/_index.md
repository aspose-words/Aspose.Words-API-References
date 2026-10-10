---
title: "Classe Aspose::Words::Hyphenation"
linktitle: "Sillabazione"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::Hyphenation. Fornisce metodi per lavorare con i dizionari di sillabazione. Questi dizionari indicano dove le parole di una lingua specifica possono essere sillabate. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 33000
url: /it/cpp/aspose.words/hyphenation/
---
## Hyphenation class


Fornisce metodi per lavorare con i dizionari di sillabazione. Questi dizionari indicano dove le parole di una lingua specifica possono essere sillabate. Per saperne di più, visita l'articolo di documentazione [Working with Hyphenation](https://docs.aspose.com/words/cpp/working-with-hyphenation/).

```cpp
class Hyphenation
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| static [get_Callback](./get_callback/)() | Ottiene l'interfaccia di callback utilizzata per richiedere i dizionari quando viene costruito il layout di pagina del documento. Questo consente il caricamento ritardato dei dizionari, utile durante l'elaborazione di documenti in molte lingue. |
| static [get_WarningCallback](./get_warningcallback/)() | Chiamata durante il caricamento dei pattern di sillabazione, quando viene rilevato un problema che potrebbe causare perdita di fedeltà nella formattazione. |
| [Hyphenation](./hyphenation/)() |  |
| static [IsDictionaryRegistered](./isdictionaryregistered/)(const System::String\&) | Restituisce **false** se per la lingua specificata non è presente alcun dizionario registrato o se quello registrato è un dizionario Null, **true** altrimenti. |
| static [RegisterDictionary](./registerdictionary/)(const System::String\&, const System::SharedPtr\<System::IO::Stream\>\&) | Registra e carica un dizionario di sillabazione per la lingua specificata da uno stream. Genera un'eccezione se il dizionario non può essere letto o ha un formato non valido. |
| static [RegisterDictionary](./registerdictionary/)(const System::String\&, const System::String\&) | Registra e carica un dizionario di sillabazione per la lingua specificata da un file. Genera un'eccezione se il dizionario non può essere letto o ha un formato non valido. Questo metodo può anche essere usato per registrare un dizionario Null per impedire che [Callback](./get_callback/) venga chiamato ripetutamente per la stessa lingua. |
| static [RegisterDictionary](./registerdictionary/)(System::String, std::basic_istream\<CharType, Traits\>\&) |  |
| static [set_Callback](./set_callback/)(const System::SharedPtr\<Aspose::Words::IHyphenationCallback\>\&) | Imposta l'interfaccia di callback utilizzata per richiedere i dizionari quando viene costruito il layout di pagina del documento. Questo consente il caricamento ritardato dei dizionari, utile durante l'elaborazione di documenti in molte lingue. |
| static [set_WarningCallback](./set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Chiamata durante il caricamento dei pattern di sillabazione, quando viene rilevato un problema che potrebbe causare perdita di fedeltà nella formattazione. |
| static [UnregisterDictionary](./unregisterdictionary/)(const System::String\&) | Annulla la registrazione di un dizionario di sillabazione per la lingua specificata. Questo è diverso dal registrare un dizionario Null. La rimozione della registrazione di un dizionario abilita il callback per la lingua specificata. |
## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
