---
title: Aspose::Words::Properties::DocumentPropertyCollection::get_Count method
linktitle: get_Count
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Properties::DocumentPropertyCollection::get_Count method. Gets number of items in the collection in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words.properties/documentpropertycollection/get_count/
---
## DocumentPropertyCollection::get_Count method


Gets number of items in the collection.

```cpp
int32_t Aspose::Words::Properties::DocumentPropertyCollection::get_Count()
```


## Examples



Shows how to work with custom document properties. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Properties.docx");

// Every document contains a collection of custom properties, which, like the built-in properties, are key-value pairs.
// The document has a fixed list of built-in properties. The user creates all of the custom properties.
ASSERT_EQ(u"Value of custom document property", System::ObjectExt::ToString(doc->get_CustomDocumentProperties()->idx_get(u"CustomProperty")));

doc->get_CustomDocumentProperties()->Add(u"CustomProperty2", String(u"Value of custom document property #2"));

std::cout << "Custom Properties:" << std::endl;
for (const auto& customDocumentProperty : System::IterateOver(doc->get_CustomDocumentProperties()))
{
    std::cout << customDocumentProperty->get_Name() << std::endl;
    std::cout << String::Format(u"\tType:\t{0}", customDocumentProperty->get_Type()) << std::endl;
    std::cout << "\tValue:\t\"" << customDocumentProperty->get_Value() << "\"" << std::endl;
}
```

## See Also

* Class [DocumentPropertyCollection](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
