---
title: "Aspose::Words::Document::get_BuiltInDocumentProperties method"
linktitle: "get_BuiltInDocumentProperties"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Document::get_BuiltInDocumentProperties method. Returnerar en samling som representerar alla inbyggda dokumentegenskaper i dokumentet i C++."
type: docs
weight: 15000
url: /sv/cpp/aspose.words/document/get_builtindocumentproperties/
---
## Document::get_BuiltInDocumentProperties method


Returnerar en samling som representerar alla inbyggda dokumentegenskaper för dokumentet.

```cpp
System::SharedPtr<Aspose::Words::Properties::BuiltInDocumentProperties> Aspose::Words::Document::get_BuiltInDocumentProperties() const
```


## Exempel



Visar hur man arbetar med inbyggda dokumentegenskaper.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Properties.docx");

// Objektet "Document" innehåller en del av dess metadata i sina medlemmar.
std::cout << System::String::Format(u"Document filename:\n\t \"{0}\"", doc->get_OriginalFileName()) << std::endl;

// Dokumentet lagrar också metadata i sina inbyggda egenskaper.
// Varje inbyggd egenskap är en medlem i dokumentets "BuiltInDocumentProperties"‑objekt.
std::cout << "Built-in Properties:" << std::endl;
for (auto&& docProperty : System::IterateOver(doc->get_BuiltInDocumentProperties()))
{
    std::cout << docProperty->get_Name() << std::endl;
    std::cout << System::String::Format(u"\tType:\t{0}", docProperty->get_Type()) << std::endl;

    // Vissa egenskaper kan lagra flera värden.
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

## Se även

* Class [BuiltInDocumentProperties](../../../aspose.words.properties/builtindocumentproperties/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
