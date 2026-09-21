---
title: "Aspose::Words::Properties::DocumentProperty::get_Name‑metod"
linktitle: "get_Name"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Properties::DocumentProperty::get_Name‑metod. Returnerar egenskapens namn i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words.properties/documentproperty/get_name/
---
## DocumentProperty::get_Name method


Returnerar namnet på egenskapen.

```cpp
System::String Aspose::Words::Properties::DocumentProperty::get_Name() const
```

## Anmärkningar


Får inte vara **null** och får inte vara en tom sträng.

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

* Class [DocumentProperty](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
