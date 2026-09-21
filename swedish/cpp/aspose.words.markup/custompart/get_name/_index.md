---
title: "Aspose::Words::Markup::CustomPart::get_Name metod"
linktitle: "get_Name"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Markup::CustomPart::get_Name metod. Hämtar eller anger detta parts absoluta namn inom OOXML‑paketet eller mål‑URL:en i C++."
type: docs
weight: 7000
url: /sv/cpp/aspose.words.markup/custompart/get_name/
---
## CustomPart::get_Name method


Hämtar eller anger delens absoluta namn inom OOXML-paketet eller mål‑URL:en.

```cpp
System::String Aspose::Words::Markup::CustomPart::get_Name() const
```

## Anmärkningar


Om relationsmålet är internt är denna egenskap det absoluta delnamnet inom paketet. Om relationsmålet är externt är denna egenskap mål‑URL:en.

Standardvärdet är en tom sträng. Ett giltigt värde måste vara en icke‑tom sträng.

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

* Class [CustomPart](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
