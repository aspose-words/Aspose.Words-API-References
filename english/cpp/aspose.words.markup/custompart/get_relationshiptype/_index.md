---
title: Aspose::Words::Markup::CustomPart::get_RelationshipType method
linktitle: get_RelationshipType
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Markup::CustomPart::get_RelationshipType method. Gets or sets the relationship type from the parent part to this custom part in C++.'
type: docs
weight: 8000
url: /cpp/aspose.words.markup/custompart/get_relationshiptype/
---
## CustomPart::get_RelationshipType method


Gets or sets the relationship type from the parent part to this custom part.

```cpp
System::String Aspose::Words::Markup::CustomPart::get_RelationshipType() const
```

## Remarks


The relationship type for a custom part must be "unknown" e.g. a custom relationship type, not one of the relationship types defined within ISO/IEC 29500.

The default value is an empty string. A valid value must be a non-empty string.

## Examples



Shows how to access a document's arbitrary custom parts collection. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Custom parts OOXML package.docx");

ASSERT_EQ(2, doc->get_PackageCustomParts()->get_Count());

// Clone the second part, then add the clone to the collection.
System::SharedPtr<Aspose::Words::Markup::CustomPart> clonedPart = doc->get_PackageCustomParts()->idx_get(1)->Clone();
doc->get_PackageCustomParts()->Add(clonedPart);

ASSERT_EQ(3, doc->get_PackageCustomParts()->get_Count());

// Enumerate over the collection and print every part.
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

// We can remove elements from this collection individually, or all at once.
doc->get_PackageCustomParts()->RemoveAt(2);

ASSERT_EQ(2, doc->get_PackageCustomParts()->get_Count());

doc->get_PackageCustomParts()->Clear();

ASSERT_EQ(0, doc->get_PackageCustomParts()->get_Count());
```

## See Also

* Class [CustomPart](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
