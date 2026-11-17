---
title: Aspose::Words::Properties::DocumentProperty::ToString method
linktitle: ToString
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Properties::DocumentProperty::ToString method. Returns the property value as a string formatted according to the current locale in C++.'
type: docs
weight: 15000
url: /cpp/aspose.words.properties/documentproperty/tostring/
---
## DocumentProperty::ToString method


Returns the property value as a string formatted according to the current locale.

```cpp
System::String Aspose::Words::Properties::DocumentProperty::ToString() const override
```

## Remarks


Converts a boolean property into "Y" or "N". Converts a date property into a short date string. For all other types converts a property using Object.ToString().
## Examples


Shows how to work with custom document properties.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Properties.docx"));

// Every document contains a collection of custom properties, which, like the built-in properties, are key-value pairs.
// The document has a fixed list of built-in properties. The user creates all of the custom properties.
ASSERT_EQ(System::ObjectExt::ToString(doc->get_CustomDocumentProperties()->idx_get(u"CustomProperty")), u"Value of custom document property");

doc->get_CustomDocumentProperties()->Add(u"CustomProperty2", System::String(u"Value of custom document property #2"));

std::cout << "Custom Properties:" << std::endl;
for (auto&& customDocumentProperty : System::IterateOver(doc->get_CustomDocumentProperties()))
{
    std::cout << customDocumentProperty->get_Name() << std::endl;
    std::cout << System::String::Format(u"\tType:\t{0}", customDocumentProperty->get_Type()) << std::endl;
    std::cout << System::String::Format(u"\tValue:\t\"{0}\"", customDocumentProperty->get_Value()) << std::endl;
}
```

Shows various type conversion methods of custom document properties.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Properties::CustomDocumentProperties> properties = doc->get_CustomDocumentProperties();

System::DateTime authDate = System::DateTime::get_Today();
properties->Add(u"Authorized", true);
properties->Add(u"Authorized By", System::String(u"John Doe"));
properties->Add(u"Authorized Date", authDate);
properties->Add(u"Authorized Revision", doc->get_BuiltInDocumentProperties()->get_RevisionNumber());
properties->Add(u"Authorized Amount", 123.45);

ASPOSE_ASSERT_EQ(properties->idx_get(u"Authorized")->ToBool(), true);
ASSERT_EQ(System::ObjectExt::ToString(properties->idx_get(u"Authorized By")), u"John Doe");
ASSERT_EQ(properties->idx_get(u"Authorized Date")->ToDateTime(), authDate);
ASSERT_EQ(properties->idx_get(u"Authorized Revision")->ToInt(), 1);
ASPOSE_ASSERT_EQ(properties->idx_get(u"Authorized Amount")->ToDouble(), 123.45);
```
## See Also

* Class [DocumentProperty](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
