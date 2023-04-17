---
title: Aspose::Words::Markup::CustomPart::get_Name method
linktitle: get_Name
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Markup::CustomPart::get_Name method. Gets or sets this part''s absolute name within the OOXML package or the target URL in C++.'
type: docs
weight: 7000
url: /cpp/aspose.words.markup/custompart/get_name/
---
## CustomPart::get_Name method


Gets or sets this part's absolute name within the OOXML package or the target URL.

```cpp
System::String Aspose::Words::Markup::CustomPart::get_Name() const
```

## Remarks


If the relationship target is internal, then this property is the absolute part name within the package. If the relationship target is external, then this property is the target URL.

The default value is an empty string. A valid value must be a non-empty string.

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

## See Also

* Class [CustomPart](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
