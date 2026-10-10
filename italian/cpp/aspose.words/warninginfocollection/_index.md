---
title: "Classe Aspose::Words::WarningInfoCollection"
linktitle: "WarningInfoCollection"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::WarningInfoCollection. Rappresenta una collezione tipizzata di oggetti WarningInfo. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 75000
url: /it/cpp/aspose.words/warninginfocollection/
---
## WarningInfoCollection class


Rappresenta una collezione tipizzata di oggetti [WarningInfo](../warninginfo/). Per saperne di più, visita l'articolo di documentazione [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
class WarningInfoCollection : public Aspose::Words::IWarningCallback,
                              public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::WarningInfo>>
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | Rimuove tutti gli elementi dalla collezione. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Ottiene il numero di elementi contenuti nella raccolta. |
| [GetEnumerator](./getenumerator/)() override | Restituisce un oggetto enumeratore che può essere usato per iterare su tutti gli elementi della raccolta. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Ottiene un elemento all'indice specificato. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
| [Warning](./warning/)(System::SharedPtr\<Aspose::Words::WarningInfo\>) override | Implementa l'interfaccia [IWarningCallback](../iwarningcallback/). Aggiunge un avviso a questa collezione. |
| [WarningInfoCollection](./warninginfocollection/)() |  |
## Typedefs

| Typedef | Descrizione |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |
## Note


Puoi utilizzare questo oggetto collezione come la forma più semplice di implementazione di [IWarningCallback](../iwarningcallback/) per raccogliere tutti gli avvisi generati da Aspose.Words durante un'operazione di caricamento o salvataggio. Crea un'istanza di questa classe e assegnala alla proprietà [WarningCallback](../../aspose.words.loading/loadoptions/get_warningcallback/) o [WarningCallback](../documentbase/get_warningcallback/).

## Esempi



Mostra come impostare la proprietà per trovare la corrispondenza più vicina per un carattere mancante tra le sorgenti di caratteri disponibili.
```cpp
// Apri un documento che contiene testo formattato con un carattere che non esiste in nessuna delle nostre sorgenti di caratteri.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Missing font.docx");

// Assegna una callback per gestire gli avvisi di sostituzione dei caratteri.
auto warningCollector = System::MakeObject<Aspose::Words::WarningInfoCollection>();
doc->set_WarningCallback(warningCollector);

// Imposta un nome di carattere predefinito e abilita la sostituzione dei caratteri.
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_DefaultFontName(u"Arial");
fontSettings->get_SubstitutionSettings()->get_FontInfoSubstitution()->set_Enabled(true);

// Le metriche originali del carattere dovrebbero essere usate dopo la sostituzione del carattere.
doc->get_LayoutOptions()->set_KeepOriginalFontMetrics(true);

// Riceveremo un avviso di sostituzione del carattere se salviamo un documento con un carattere mancante.
doc->set_FontSettings(fontSettings);
doc->Save(get_ArtifactsDir() + u"FontSettings.EnableFontSubstitution.pdf");

for (auto&& info : warningCollector)
{
    if (info->get_WarningType() == Aspose::Words::WarningType::FontSubstitution)
    {
        std::cout << info->get_Description() << std::endl;
    }
}
```

## Vedi anche

* Interface [IWarningCallback](../iwarningcallback/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
