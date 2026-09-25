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
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Properties.docx"));

// Every document contains a collection of custom properties, which, like the built-in properties, are key-value pairs.
// The document has a fixed list of built-in properties. The user creates all of the custom properties.
ASSERT_EQ(u"Value of custom document property", System::ObjectExt::ToString(doc->get_CustomDocumentProperties()->idx_get(u"CustomProperty")));

doc->get_CustomDocumentProperties()->Add(u"CustomProperty2", System::String(u"Value of custom document property #2"));

System::Console::WriteLine(u"Custom Properties:");
for (auto&& customDocumentProperty : System::IterateOver(doc->get_CustomDocumentProperties()))
{
    System::Console::WriteLine(customDocumentProperty->get_Name());
    System::Console::WriteLine(System::String::Format(u"\tType:\t{0}", customDocumentProperty->get_Type()));
    System::Console::WriteLine(System::String::Format(u"\tValue:\t\"{0}\"", customDocumentProperty->get_Value()));
}
```

## See Also

* Class [DocumentPropertyCollection](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
