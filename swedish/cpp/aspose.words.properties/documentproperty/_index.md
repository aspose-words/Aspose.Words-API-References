---
title: "Aspose::Words::Properties::DocumentProperty klass"
linktitle: "DocumentProperty"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Properties::DocumentProperty klass. Representerar en anpassad eller inbyggd dokumentegenskap. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.properties/documentproperty/
---
## DocumentProperty class


Representerar en anpassad eller inbyggd dokumentegenskap. För att lära dig mer, besök dokumentationsartikeln [Work with Document Properties](https://docs.aspose.com/words/cpp/work-with-document-properties/).

```cpp
class DocumentProperty : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_IsLinkToContent](./get_islinktocontent/)() | Visar om den här egenskapen är länkad till innehåll eller inte. |
| [get_LinkSource](./get_linksource/)() const | Hämtar källan för en länkad anpassad dokumentegenskap. |
| [get_Name](./get_name/)() const | Returnerar namnet på egenskapen. |
| [get_Type](./get_type/)() const | Hämtar datatypen för egenskapen. |
| [get_Value](./get_value/)() | Hämtar eller anger värdet på egenskapen. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Value](./set_value/)(const System::SharedPtr\<System::Object\>\&) | Sättare för [Aspose::Words::Properties::DocumentProperty::get_Value](./get_value/). |
| [ToBool](./tobool/)() | Returnerar egenskapsvärdet som bool. |
| [ToByteArray](./tobytearray/)() | Returnerar egenskapsvärdet som byte-array. |
| [ToDateTime](./todatetime/)() | Returnerar egenskapsvärdet som **DateTime** i UTC. |
| [ToDouble](./todouble/)() | Returnerar egenskapsvärdet som double. |
| [ToInt](./toint/)() | Returnerar egenskapsvärdet som heltal. |
| [ToString](./tostring/)() const override | Returnerar egenskapsvärdet som en sträng formaterad enligt aktuell lokala inställning. |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Properties](../)
* Library [Aspose.Words for C++](../../)
