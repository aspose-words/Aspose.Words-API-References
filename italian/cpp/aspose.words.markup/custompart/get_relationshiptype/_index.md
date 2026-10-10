---
title: "Metodo Aspose::Words::Markup::CustomPart::get_RelationshipType"
linktitle: "get_RelationshipType"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Markup::CustomPart::get_RelationshipType. Ottiene o imposta il tipo di relazione dalla parte padre a questa parte personalizzata in C++."
type: docs
weight: 8000
url: /it/cpp/aspose.words.markup/custompart/get_relationshiptype/
---
## CustomPart::get_RelationshipType method


Ottiene o imposta il tipo di relazione dalla parte padre a questa parte personalizzata.

```cpp
System::String Aspose::Words::Markup::CustomPart::get_RelationshipType() const
```

## Note


Il tipo di relazione per una parte personalizzata deve essere "unknown", ad esempio un tipo di relazione personalizzato, non uno dei tipi di relazione definiti all'interno di ISO/IEC 29500.

Il valore predefinito è una stringa vuota. Un valore valido deve essere una stringa non vuota.

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
