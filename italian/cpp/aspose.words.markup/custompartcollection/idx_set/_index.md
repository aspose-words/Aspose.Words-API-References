---
title: "Aspose::Words::Markup::CustomPartCollection::idx_set metodo"
linktitle: "idx_set"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Markup::CustomPartCollection::idx_set metodo. Ottiene o imposta un elemento all'indice specificato in C++."
type: docs
weight: 14000
url: /it/cpp/aspose.words.markup/custompartcollection/idx_set/
---
## CustomPartCollection::idx_set method


Ottiene o imposta un elemento all'indice specificato.

```cpp
void Aspose::Words::Markup::CustomPartCollection::idx_set(int32_t index, const System::SharedPtr<Aspose::Words::Markup::CustomPart> &value)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| index | int32_t | Indice basato su zero dell'elemento. |

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

* Class [CustomPart](../../custompart/)
* Class [CustomPartCollection](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
