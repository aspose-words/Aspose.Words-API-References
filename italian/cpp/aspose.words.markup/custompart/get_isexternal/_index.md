---
title: "Metodo Aspose::Words::Markup::CustomPart::get_IsExternal"
linktitle: "get_IsExternal"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Markup::CustomPart::get_IsExternal. False se questa parte personalizzata è memorizzata all'interno del pacchetto OOXML. True se questa parte personalizzata è una destinazione esterna in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words.markup/custompart/get_isexternal/
---
## CustomPart::get_IsExternal method


Falso se questa parte personalizzata è memorizzata all'interno del pacchetto OOXML. Vero se questa parte personalizzata è una destinazione esterna.

```cpp
bool Aspose::Words::Markup::CustomPart::get_IsExternal() const
```

## Note


Il valore predefinito è **false**.

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

* Class [CustomPart](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
