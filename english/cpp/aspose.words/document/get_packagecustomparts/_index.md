---
title: Aspose::Words::Document::get_PackageCustomParts method
linktitle: get_PackageCustomParts
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Document::get_PackageCustomParts method. Gets or sets the collection of custom parts (arbitrary content) that are linked to the OOXML package using "unknown relationships" in C++.'
type: docs
weight: 42000
url: /cpp/aspose.words/document/get_packagecustomparts/
---
## Document::get_PackageCustomParts method


Gets or sets the collection of custom parts (arbitrary content) that are linked to the OOXML package using "unknown relationships".

```cpp
System::SharedPtr<Aspose::Words::Markup::CustomPartCollection> Aspose::Words::Document::get_PackageCustomParts() const
```

## Remarks


Do not confuse these custom parts with Custom XML Data. If you need to access Custom XML parts, use the [CustomXmlParts](../get_customxmlparts/) property.

This collection contains OOXML parts whose parent is the OOXML package and they targets are of an "unknown relationship". For more information see [CustomPart](../../../aspose.words.markup/custompart/).

Aspose.Words loads and saves custom parts into OOXML documents only.

This property cannot be **null**.

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

* Class [CustomPartCollection](../../../aspose.words.markup/custompartcollection/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
