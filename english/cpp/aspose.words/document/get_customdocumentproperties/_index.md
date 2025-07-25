---
title: Aspose::Words::Document::get_CustomDocumentProperties method
linktitle: get_CustomDocumentProperties
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Document::get_CustomDocumentProperties method. Returns a collection that represents all the custom document properties of the document in C++.'
type: docs
weight: 18000
url: /cpp/aspose.words/document/get_customdocumentproperties/
---
## Document::get_CustomDocumentProperties method


Returns a collection that represents all the custom document properties of the document.

```cpp
System::SharedPtr<Aspose::Words::Properties::CustomDocumentProperties> Aspose::Words::Document::get_CustomDocumentProperties()
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

* Class [CustomDocumentProperties](../../../aspose.words.properties/customdocumentproperties/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
