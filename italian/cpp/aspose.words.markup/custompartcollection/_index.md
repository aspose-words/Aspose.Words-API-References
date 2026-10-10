---
title: "Aspose::Words::Markup::CustomPartCollection class"
linktitle: "CustomPartCollection"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Markup::CustomPartCollection class. Rappresenta una raccolta di oggetti CustomPart. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.markup/custompartcollection/
---
## CustomPartCollection class


Rappresenta una raccolta di oggetti [CustomPart](../custompart/). Per saperne di più, visita l'articolo di documentazione [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class CustomPartCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Markup::CustomPart>>
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Markup::CustomPart\>\&) | Aggiunge un elemento alla raccolta. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | Rimuove tutti gli elementi dalla collezione. |
| [Clone](./clone/)() | Crea una copia profonda di questa collezione e dei suoi elementi. |
| [CustomPartCollection](./custompartcollection/)() |  |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Ottiene il numero di elementi contenuti nella raccolta. |
| [GetEnumerator](./getenumerator/)() override | Restituisce un oggetto enumeratore che può essere usato per iterare su tutti gli elementi della raccolta. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Ottiene o imposta un elemento all'indice specificato. |
| [idx_set](./idx_set/)(int32_t, const System::SharedPtr\<Aspose::Words::Markup::CustomPart\>\&) | Ottiene o imposta un elemento all'indice specificato. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [RemoveAt](./removeat/)(int32_t) | Rimuove un elemento all'indice specificato. |
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


Normalmente non è necessario creare istanze di questa classe. È possibile accedere alle parti personalizzate relative al pacchetto OOXML tramite la proprietà [PackageCustomParts](../../aspose.words/document/get_packagecustomparts/).

## Esempi



Mostra come accedere alla raccolta di parti personalizzate arbitrarie di un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Custom parts OOXML package.docx");

ASSERT_EQ(2, doc->get_PackageCustomParts()->get_Count());

// Clona la seconda parte, quindi aggiungi la copia alla raccolta.
System::SharedPtr<Aspose::Words::Markup::CustomPart> clonedPart = doc->get_PackageCustomParts()->idx_get(1)->Clone();
doc->get_PackageCustomParts()->Add(clonedPart);

ASSERT_EQ(3, doc->get_PackageCustomParts()->get_Count());

// Enumera la raccolta e stampa ogni parte.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Markup::CustomPart>>> enumerator = doc->get_PackageCustomParts()->GetEnumerator();
    int32_t index = 0;
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"Part index {0}:", index) << std::endl;
        std::cout << System::String::Format(u"\tName:\t\t\t\t{0}", enumerator->get_Current()->get_Name()) << std::endl;
        std::cout << System::String::Format(u"\tContent type:\t\t{0}", enumerator->get_Current()->get_ContentType()) << std::endl;
        std::cout << System::String::Format(u"\tRelationship type:\t{0}", enumerator->get_Current()->get_RelationshipType()) << std::endl;
        std::cout << (enumerator->get_Current()->get_IsExternal() ? u"\tSourced from outside the document" : System::String::Format(u"\tStored within the document, length: {0} bytes", enumerator->get_Current()->get_Data()->get_Length())) << std::endl;
        index++;
    }
}

// Possiamo rimuovere gli elementi da questa raccolta individualmente o tutti insieme.
doc->get_PackageCustomParts()->RemoveAt(2);

ASSERT_EQ(2, doc->get_PackageCustomParts()->get_Count());

doc->get_PackageCustomParts()->Clear();

ASSERT_EQ(0, doc->get_PackageCustomParts()->get_Count());
```

## Vedi anche

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
