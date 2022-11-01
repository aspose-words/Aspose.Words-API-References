---
title: idx_get
second_title: Aspose.Words for C++ API Reference
description: Returns a DocumentProperty object by index.
type: docs
weight: 53
url: /cpp/aspose.words.properties/documentpropertycollection/idx_get/
---
## DocumentPropertyCollection.idx_get(int32_t) method


Returns a [DocumentProperty](../../documentproperty/) object by index.

```cpp
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> Aspose::Words::Properties::DocumentPropertyCollection::idx_get(int32_t index)
```


| Parameter | Type | Description |
| --- | --- | --- |
| index | int32_t | Zero-based index of the [DocumentProperty](../../documentproperty/) to retrieve. |

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

## DocumentPropertyCollection.idx_get(System::String) method


Returns a [DocumentProperty](../../documentproperty/) object by the name of the property.

```cpp
virtual System::SharedPtr<Aspose::Words::Properties::DocumentProperty> Aspose::Words::Properties::DocumentPropertyCollection::idx_get(System::String name)
```


| Parameter | Type | Description |
| --- | --- | --- |
| name | System::String | The case-insensitive name of the property to retrieve. |

Returns null if a property with the specified name is not found.

## Examples




Shows how to create a custom document property which contains a date and time. 
```cpp
auto doc = MakeObject<Document>();

doc->get_CustomDocumentProperties()->Add(u"AuthorizationDate", System::DateTime::get_Now());

std::cout << "Document authorized on " << doc->get_CustomDocumentProperties()->idx_get(u"AuthorizationDate")->ToDateTime() << std::endl;
```

