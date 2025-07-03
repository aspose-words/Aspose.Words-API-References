---
title: Aspose::Words::Document::get_BuiltInDocumentProperties method
linktitle: get_BuiltInDocumentProperties
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Document::get_BuiltInDocumentProperties method. Returns a collection that represents all the built-in document properties of the document in C++.'
type: docs
weight: 15000
url: /cpp/aspose.words/document/get_builtindocumentproperties/
---
## Document::get_BuiltInDocumentProperties method


Returns a collection that represents all the built-in document properties of the document.

```cpp
System::SharedPtr<Aspose::Words::Properties::BuiltInDocumentProperties> Aspose::Words::Document::get_BuiltInDocumentProperties() const
```


## Examples



Shows how to work with built-in document properties. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Properties.docx");

// The "Document" object contains some of its metadata in its members.
std::cout << System::String::Format(u"Document filename:\n\t \"{0}\"", doc->get_OriginalFileName()) << std::endl;

// The document also stores metadata in its built-in properties.
// Each built-in property is a member of the document's "BuiltInDocumentProperties" object.
std::cout << "Built-in Properties:" << std::endl;
for (auto&& docProperty : System::IterateOver(doc->get_BuiltInDocumentProperties()))
{
    std::cout << docProperty->get_Name() << std::endl;
    std::cout << System::String::Format(u"\tType:\t{0}", docProperty->get_Type()) << std::endl;

    // Some properties may store multiple values.
    if (System::ObjectExt::Is<System::Collections::Generic::ICollection<System::SharedPtr<System::Object>>>(docProperty->get_Value()))
    {
        for (auto&& value : System::IterateOver(System::AsCast<System::Collections::Generic::ICollection<System::SharedPtr<System::Object>>>(docProperty->get_Value())))
        {
            std::cout << System::String::Format(u"\tValue:\t\"{0}\"", value) << std::endl;
        }
    }
    else
    {
        std::cout << System::String::Format(u"\tValue:\t\"{0}\"", docProperty->get_Value()) << std::endl;
    }
}
```

## See Also

* Class [BuiltInDocumentProperties](../../../aspose.words.properties/builtindocumentproperties/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
