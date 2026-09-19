---
title: "Classe Aspose::Words::Markup::CustomXmlSchemaCollection"
linktitle: "CustomXmlSchemaCollection"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::Markup::CustomXmlSchemaCollection. Una raccolta di stringhe che rappresentano schemi XML associati a una parte XML personalizzata. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 7000
url: /it/cpp/aspose.words.markup/customxmlschemacollection/
---
## CustomXmlSchemaCollection class


Una raccolta di stringhe che rappresentano gli schemi XML associati a una parte XML personalizzata. Per saperne di più, visita l'articolo di documentazione [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class CustomXmlSchemaCollection : public System::Collections::Generic::IEnumerable<System::String>
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Add](./add/)(const System::String\&) | Aggiunge un elemento alla raccolta. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | Rimuove tutti gli elementi dalla collezione. |
| [Clone](./clone/)() | Crea una copia profonda di questo oggetto. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Ottiene il numero di elementi contenuti nella raccolta. |
| [GetEnumerator](./getenumerator/)() override | Restituisce un oggetto enumeratore che può essere usato per iterare su tutti gli elementi della raccolta. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Ottiene o imposta l'elemento all'indice specificato. |
| [idx_set](./idx_set/)(int32_t, const System::String\&) | Ottiene o imposta l'elemento all'indice specificato. |
| [IndexOf](./indexof/)(const System::String\&) | Restituisce l'indice basato su zero del valore specificato nella raccolta. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | Rimuove il valore specificato dalla raccolta. |
| [RemoveAt](./removeat/)(int32_t) | Rimuove un valore all'indice specificato. |
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


Non si creano istanze di questa classe. Si accede alla raccolta di schemi XML di una parte XML personalizzata tramite la proprietà [Schemas](../customxmlpart/get_schemas/).

## Esempi



Mostra come lavorare con una raccolta di schemi XML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::String xmlPartId = System::Guid::NewGuid().ToString(u"B");
System::String xmlPartContent = u"<root><text>Hello, World!</text></root>";
System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPart = doc->get_CustomXmlParts()->Add(xmlPartId, xmlPartContent);

// Aggiungi un'associazione di schema XML.
xmlPart->get_Schemas()->Add(u"http://www.w3.org/2001/XMLSchema");

// Clona la raccolta di associazione di schemi XML della parte XML personalizzata,
// e poi aggiungi un paio di nuovi schemi alla copia.
System::SharedPtr<Aspose::Words::Markup::CustomXmlSchemaCollection> schemas = xmlPart->get_Schemas()->Clone();
schemas->Add(u"http://www.w3.org/2001/XMLSchema-instance");
schemas->Add(u"http://schemas.microsoft.com/office/2006/metadata/contentType");

ASSERT_EQ(3, schemas->get_Count());
ASSERT_EQ(2, schemas->IndexOf(u"http://schemas.microsoft.com/office/2006/metadata/contentType"));

// Enumera gli schemi e stampa ogni elemento.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::String>> enumerator = schemas->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << enumerator->get_Current() << std::endl;
    }
}

// Di seguito sono riportati tre modi per rimuovere gli schemi dalla raccolta.
// 1 -  Rimuovi uno schema per indice:
schemas->RemoveAt(2);

// 2 -  Rimuovi uno schema per valore:
schemas->Remove(u"http://www.w3.org/2001/XMLSchema");

// 3 -  Usa il metodo "Clear" per svuotare la collezione in una volta.
schemas->Clear();

ASSERT_EQ(0, schemas->get_Count());
```

## Vedi anche

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
