---
title: "Aspose::Words::Properties::DocumentProperty::ToString‑metod"
linktitle: "ToString"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Properties::DocumentProperty::ToString‑metod. Returnerar egenskapsvärdet som en sträng formaterad enligt aktuell kultur i C++."
type: docs
weight: 15000
url: /sv/cpp/aspose.words.properties/documentproperty/tostring/
---
## DocumentProperty::ToString method


Returnerar egenskapsvärdet som en sträng formaterad enligt aktuell lokala inställning.

```cpp
System::String Aspose::Words::Properties::DocumentProperty::ToString() const override
```

## Anmärkningar


Konverterar en boolesk egenskap till "Y" eller "N". Konverterar en datumegenskap till en kort datumsträng. För alla andra typer konverteras en egenskap med Object.ToString().

## Exempel



Visar hur man arbetar med anpassade dokumentegenskaper.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Properties.docx");

// Varje dokument innehåller en samling av anpassade egenskaper, som, precis som de inbyggda egenskaperna, är nyckel‑värde‑par.
// Dokumentet har en fast lista med inbyggda egenskaper. Användaren skapar alla anpassade egenskaper.
ASSERT_EQ(u"Value of custom document property", System::ObjectExt::ToString(doc->get_CustomDocumentProperties()->idx_get(u"CustomProperty")));

doc->get_CustomDocumentProperties()->Add(u"CustomProperty2", System::String(u"Value of custom document property #2"));

std::cout << "Custom Properties:" << std::endl;
for (auto&& customDocumentProperty : System::IterateOver(doc->get_CustomDocumentProperties()))
{
    std::cout << customDocumentProperty->get_Name() << std::endl;
    std::cout << System::String::Format(u"\tType:\t{0}", customDocumentProperty->get_Type()) << std::endl;
    std::cout << System::String::Format(u"\tValue:\t\"{0}\"", customDocumentProperty->get_Value()) << std::endl;
}
```


Visar olika typkonverteringsmetoder för anpassade dokumentegenskaper.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Properties::CustomDocumentProperties> properties = doc->get_CustomDocumentProperties();

System::DateTime authDate = System::DateTime::get_Today();
properties->Add(u"Authorized", true);
properties->Add(u"Authorized By", System::String(u"John Doe"));
properties->Add(u"Authorized Date", authDate);
properties->Add(u"Authorized Revision", doc->get_BuiltInDocumentProperties()->get_RevisionNumber());
properties->Add(u"Authorized Amount", 123.45);

ASPOSE_ASSERT_EQ(true, properties->idx_get(u"Authorized")->ToBool());
ASSERT_EQ(u"John Doe", System::ObjectExt::ToString(properties->idx_get(u"Authorized By")));
ASSERT_EQ(authDate, properties->idx_get(u"Authorized Date")->ToDateTime());
ASSERT_EQ(1, properties->idx_get(u"Authorized Revision")->ToInt());
ASPOSE_ASSERT_EQ(123.45, properties->idx_get(u"Authorized Amount")->ToDouble());
```

## Se även

* Class [DocumentProperty](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
