---
title: idx_get
second_title: Aspose.Words for C++ API Reference
description: Returns a DocumentProperty object by the name of the property.
type: docs
weight: 417
url: /cpp/aspose.words.properties/builtindocumentproperties/idx_get/
---
## BuiltInDocumentProperties::idx_get method


Returns a [DocumentProperty](../../documentproperty/) object by the name of the property.

```cpp
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> Aspose::Words::Properties::BuiltInDocumentProperties::idx_get(System::String name) override
```


| Parameter | Type | Description |
| --- | --- | --- |
| name | System::String | The case-insensitive name of the property to retrieve. |
## Remarks


The string names of the properties correspond to the names of the typed properties available from [BuiltInDocumentProperties](../).

If you request a property that is not present in the document, but the name of the property is recognized as a valid built-in name, a new [DocumentProperty](../../documentproperty/) is created, added to the collection and returned. The newly created property is assigned a default value (empty string, zero, false or DateTime.MinValue depending on the type of the built-in property).

If you request a property that is not present in the document and the name is not recognized as a built-in name, a null is returned.

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

* Class [DocumentProperty](../../documentproperty/)
* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words](../../../)
