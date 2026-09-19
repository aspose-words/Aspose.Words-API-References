---
title: "Aspose::Words::RevisionGroupCollection classe"
linktitle: "RevisionGroupCollection"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::RevisionGroupCollection classe. Una raccolta di oggetti RevisionGroup che rappresentano gruppi di revisioni nel documento. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 55000
url: /it/cpp/aspose.words/revisiongroupcollection/
---
## RevisionGroupCollection class


Una raccolta di oggetti [RevisionGroup](../revisiongroup/) che rappresentano gruppi di revisioni nel documento. Per saperne di più, visita l'articolo di documentazione [Traccia le modifiche in un documento](https://docs.aspose.com/words/cpp/track-changes-in-a-document/).

```cpp
class RevisionGroupCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::RevisionGroup>>
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Restituisce il numero di gruppi di revisione nella raccolta. |
| [GetEnumerator](./getenumerator/)() override | Restituisce un oggetto enumeratore. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Restituisce un gruppo di revisione all'indice specificato. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
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


Non crei istanze di questa classe direttamente. Usa la proprietà [Groups](../revisioncollection/get_groups/) per ottenere i gruppi di revisione presenti in un documento.

## Esempi



Mostra come stampare le informazioni su un gruppo di revisioni in un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");

ASSERT_EQ(7, doc->get_Revisions()->get_Groups()->get_Count());

for (auto&& group : doc->get_Revisions()->get_Groups())
{
    std::cout << System::String::Format(u"Revision author: {0}; Revision type: {1} \n\tRevision text: {2}", group->get_Author(), group->get_RevisionType(), group->get_Text()) << std::endl;
}
```


Mostra come ottenere un gruppo di revisioni in un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");

System::SharedPtr<Aspose::Words::RevisionGroup> revisionGroup = doc->get_Revisions()->get_Groups()->idx_get(0);
```

## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
