---
title: Aspose::Words::Properties::DocumentProperty::get_Name method
linktitle: get_Name
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Properties::DocumentProperty::get_Name method. Returns the name of the property in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words.properties/documentproperty/get_name/
---
## DocumentProperty::get_Name method


Returns the name of the property.

```cpp
System::String Aspose::Words::Properties::DocumentProperty::get_Name() const
```

## Remarks


Cannot be **null** and cannot be an empty string.

## Examples



Shows how to work with built-in document properties. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Properties.docx"));

// The "Document" object contains some of its metadata in its members.
System::Console::WriteLine(System::String::Format(u"Document filename:\n\t \"{0}\"", doc->get_OriginalFileName()));

// The document also stores metadata in its built-in properties.
// Each built-in property is a member of the document's "BuiltInDocumentProperties" object.
System::Console::WriteLine(u"Built-in Properties:");
for (auto&& docProperty : System::IterateOver(doc->get_BuiltInDocumentProperties()))
{
    System::Console::WriteLine(docProperty->get_Name());
    System::Console::WriteLine(System::String::Format(u"\tType:\t{0}", docProperty->get_Type()));

    // Some properties may store multiple values.
    if (System::ObjectExt::Is<System::Collections::Generic::ICollection<System::SharedPtr<System::Object>>>(docProperty->get_Value()))
    {
        for (auto&& value : System::IterateOver(System::AsCast<System::Collections::Generic::ICollection<System::SharedPtr<System::Object>>>(docProperty->get_Value())))
        {
            System::Console::WriteLine(System::String::Format(u"\tValue:\t\"{0}\"", value));
        }
    }
    else
    {
        System::Console::WriteLine(System::String::Format(u"\tValue:\t\"{0}\"", docProperty->get_Value()));
    }
}
```

## See Also

* Class [DocumentProperty](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
