---
title: Aspose::Words::Properties::DocumentProperty::get_Value method
linktitle: get_Value
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Properties::DocumentProperty::get_Value method. Gets or sets the value of the property in C++.'
type: docs
weight: 6000
url: /cpp/aspose.words.properties/documentproperty/get_value/
---
## DocumentProperty::get_Value method


Gets or sets the value of the property.

```cpp
System::SharedPtr<System::Object> Aspose::Words::Properties::DocumentProperty::get_Value()
```

## Remarks


Cannot be **null**.

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

* Class [DocumentProperty](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
