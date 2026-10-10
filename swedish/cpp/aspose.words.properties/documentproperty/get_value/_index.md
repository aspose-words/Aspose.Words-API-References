---
title: "Aspose::Words::Properties::DocumentProperty::get_Value metod"
linktitle: "get_Value"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Properties::DocumentProperty::get_Value metod. Hämtar eller anger värdet på egenskapen i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words.properties/documentproperty/get_value/
---
## DocumentProperty::get_Value method


Hämtar eller anger värdet på egenskapen.

```cpp
System::SharedPtr<System::Object> Aspose::Words::Properties::DocumentProperty::get_Value()
```

## Anmärkningar


Kan inte vara **null**.

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
