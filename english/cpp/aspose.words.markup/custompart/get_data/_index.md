---
title: get_Data
second_title: Aspose.Words for C++ API Reference
description: Contains the data of this custom part.
type: docs
weight: 40
url: /cpp/aspose.words.markup/custompart/get_data/
---
## CustomPart.get_Data method


Contains the data of this custom part.

```cpp
System::ArrayPtr<uint8_t> Aspose::Words::Markup::CustomPart::get_Data() const
```


This property is applicable only when [IsExternal](../get_isexternal/) is **false**.

The default value is an empty byte array. The value cannot be **null**.

## Examples




Shows how to access a document's arbitrary custom parts collection. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Custom parts OOXML package.docx");

ASSERT_EQ(2, doc->get_PackageCustomParts()->get_Count());

// Clone the second part, then add the clone to the collection.
SharedPtr<CustomPart> clonedPart = doc->get_PackageCustomParts()->idx_get(1)->Clone();
doc->get_PackageCustomParts()->Add(clonedPart);

ASSERT_EQ(3, doc->get_PackageCustomParts()->get_Count());

// Enumerate over the collection and print every part.
{
    SharedPtr<System::Collections::Generic::IEnumerator<SharedPtr<CustomPart>>> enumerator = doc->get_PackageCustomParts()->GetEnumerator();
    int index = 0;
    while (enumerator->MoveNext())
    {
        std::cout << "Part index " << index << ":" << std::endl;
        std::cout << "\tName:\t\t\t\t" << enumerator->get_Current()->get_Name() << std::endl;
        std::cout << "\tContent type:\t\t" << enumerator->get_Current()->get_ContentType() << std::endl;
        std::cout << "\tRelationship type:\t" << enumerator->get_Current()->get_RelationshipType() << std::endl;
        std::cout << (enumerator->get_Current()->get_IsExternal()
                          ? u"\tSourced from outside the document"
                          : String::Format(u"\tStored within the document, length: {0} bytes", enumerator->get_Current()->get_Data()->get_Length()))
                  << std::endl;
        index++;
    }
}

// We can remove elements from this collection individually, or all at once.
doc->get_PackageCustomParts()->RemoveAt(2);

ASSERT_EQ(2, doc->get_PackageCustomParts()->get_Count());

doc->get_PackageCustomParts()->Clear();

ASSERT_EQ(0, doc->get_PackageCustomParts()->get_Count());
```
