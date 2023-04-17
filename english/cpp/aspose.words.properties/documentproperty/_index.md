---
title: Aspose::Words::Properties::DocumentProperty class
linktitle: DocumentProperty
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Properties::DocumentProperty class. Represents a custom or built-in document property. To learn more, visit the  documentation article in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.properties/documentproperty/
---
## DocumentProperty class


Represents a custom or built-in document property. To learn more, visit the [Work with Document Properties](https://docs.aspose.com/words/cpp/work-with-document-properties/) documentation article.

```cpp
class DocumentProperty : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_IsLinkToContent](./get_islinktocontent/)() | Shows whether this property is linked to content or not. |
| [get_LinkSource](./get_linksource/)() const | Gets the source of a linked custom document property. |
| [get_Name](./get_name/)() const | Returns the name of the property. |
| [get_Type](./get_type/)() const | Gets the data type of the property. |
| [get_Value](./get_value/)() | Gets or sets the value of the property. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Value](./set_value/)(const System::SharedPtr\<System::Object\>\&) | Setter for [Aspose::Words::Properties::DocumentProperty::get_Value](./get_value/). |
| [ToBool](./tobool/)() | Returns the property value as bool. |
| [ToByteArray](./tobytearray/)() | Returns the property value as byte array. |
| [ToDateTime](./todatetime/)() | Returns the property value as **DateTime** in UTC. |
| [ToDouble](./todouble/)() | Returns the property value as double. |
| [ToInt](./toint/)() | Returns the property value as integer. |
| [ToString](./tostring/)() const override | Returns the property value as a string formatted according to the current locale. |
| static [Type](./type/)() |  |

## Examples



Shows how to work with built-in document properties. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Properties.docx");

// The "Document" object contains some of its metadata in its members.
std::cout << "Document filename:\n\t \"" << doc->get_OriginalFileName() << "\"" << std::endl;

// The document also stores metadata in its built-in properties.
// Each built-in property is a member of the document's "BuiltInDocumentProperties" object.
std::cout << "Built-in Properties:" << std::endl;
for (const auto& docProperty : System::IterateOver(doc->get_BuiltInDocumentProperties()))
{
    std::cout << docProperty->get_Name() << std::endl;
    std::cout << String::Format(u"\tType:\t{0}", docProperty->get_Type()) << std::endl;

    // Some properties may store multiple values.
    if (System::ObjectExt::Is<System::Collections::Generic::ICollection<SharedPtr<System::Object>>>(docProperty->get_Value()))
    {
        for (const auto& value : System::IterateOver(
                 System::DynamicCast_noexcept<System::Collections::Generic::ICollection<SharedPtr<System::Object>>>(docProperty->get_Value())))
        {
            std::cout << "\tValue:\t\"" << value << "\"" << std::endl;
        }
    }
    else
    {
        std::cout << "\tValue:\t\"" << docProperty->get_Value() << "\"" << std::endl;
    }
}
```

## See Also

* Namespace [Aspose::Words::Properties](../)
* Library [Aspose.Words for C++](../../)
