---
title: "Aspose::Words::Markup::CustomPartCollection::Add-metoden"
linktitle: "Add"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Markup::CustomPartCollection::Add-metoden. Lägger till ett objekt i samlingen i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.markup/custompartcollection/add/
---
## CustomPartCollection::Add method


Lägger till ett objekt i samlingen.

```cpp
void Aspose::Words::Markup::CustomPartCollection::Add(const System::SharedPtr<Aspose::Words::Markup::CustomPart> &part)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| del | const System::SharedPtr\<Aspose::Words::Markup::CustomPart\>\& | Objektet att lägga till. |

## Exempel



Visar hur man får åtkomst till ett dokuments godtyckliga samling av anpassade delar.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Custom parts OOXML package.docx");

ASSERT_EQ(2, doc->get_PackageCustomParts()->get_Count());

// Klona den andra delen och lägg sedan till klonen i samlingen.
System::SharedPtr<Aspose::Words::Markup::CustomPart> clonedPart = doc->get_PackageCustomParts()->idx_get(1)->Clone();
doc->get_PackageCustomParts()->Add(clonedPart);

ASSERT_EQ(3, doc->get_PackageCustomParts()->get_Count());

// Iterera över samlingen och skriv ut varje del.
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

// Vi kan ta bort element från den här samlingen individuellt eller alla på en gång.
doc->get_PackageCustomParts()->RemoveAt(2);

ASSERT_EQ(2, doc->get_PackageCustomParts()->get_Count());

doc->get_PackageCustomParts()->Clear();

ASSERT_EQ(0, doc->get_PackageCustomParts()->get_Count());
```

## Se även

* Class [CustomPart](../../custompart/)
* Class [CustomPartCollection](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
