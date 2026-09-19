---
title: "Classe Aspose::Words::MailMerging::MappedDataFieldCollection"
linktitle: "MappedDataFieldCollection"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::MailMerging::MappedDataFieldCollection. Consente di mappare automaticamente tra i nomi dei campi nella tua origine dati e i nomi dei campi di stampa unione nel documento. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words.mailmerging/mappeddatafieldcollection/
---
## MappedDataFieldCollection class


Consente di mappare automaticamente i nomi dei campi nella tua fonte dati con i nomi dei campi di unione mail nel documento. Per saperne di più, visita l'articolo di documentazione [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/).

```cpp
class MappedDataFieldCollection : public System::Collections::Generic::IEnumerable<System::Collections::Generic::KeyValuePair<System::String, System::String>>
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Add](./add/)(const System::String\&, const System::String\&) | Aggiunge una nuova mappatura di campo. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | Rimuove tutti gli elementi dalla collezione. |
| [ContainsKey](./containskey/)(const System::String\&) | Determina se una mappatura dal campo specificato nel documento esiste nella collezione. |
| [ContainsValue](./containsvalue/)(const System::String\&) | Determina se una mappatura dal campo specificato nell'origine dati esiste nella collezione. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Ottiene il numero di elementi contenuti nella raccolta. |
| [GetEnumerator](./getenumerator/)() override | Restituisce un oggetto enumeratore di dizionario che può essere usato per iterare su tutti gli elementi della collezione. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(const System::String\&) | Ottiene o imposta il nome del campo nell'origine dati associato al campo di stampa unione specificato. |
| [idx_set](./idx_set/)(const System::String\&, const System::String\&) | Ottiene o imposta il nome del campo nell'origine dati associato al campo di stampa unione specificato. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | Rimuove una mappatura di campo. |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| Typedef | Descrizione |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |
## Note


Questo è implementato come una collezione di chiavi stringa in valori stringa. Le chiavi sono i nomi dei campi di stampa unione nel documento e i valori sono i nomi dei campi nella tua origine dati.

## Vedi anche

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
