---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::idx_get metod"
linktitle: "idx_get"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::idx_get‑metod. Returnerar ett DocumentProperty‑objekt baserat på egenskapens namn i C++."
type: docs
weight: 35000
url: /sv/cpp/aspose.words.properties/builtindocumentproperties/idx_get/
---
## BuiltInDocumentProperties::idx_get method


Returnerar ett [DocumentProperty](../../documentproperty/)‑objekt baserat på egenskapens namn.

```cpp
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> Aspose::Words::Properties::BuiltInDocumentProperties::idx_get(System::String name) override
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| namn | System::String | Det skiftlägesokänsliga namnet på egenskapen som ska hämtas. |
## Anmärkningar


Strängnamnen på egenskaperna motsvarar namnen på de typade egenskaper som finns tillgängliga från [BuiltInDocumentProperties](../).

Om du begär en egenskap som inte finns i dokumentet, men egenskapens namn känns igen som ett giltigt inbyggt namn, skapas en ny [DocumentProperty](../../documentproperty/), läggs till i samlingen och returneras. Den nyss skapade egenskapen tilldelas ett standardvärde (tom sträng, noll, **false** eller DateTime.MinValue beroende på typen av den inbyggda egenskapen).

Om du begär en egenskap som inte finns i dokumentet och namnet inte känns igen som ett inbyggt namn, returneras **null**.

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

## Se även

* Class [DocumentProperty](../../documentproperty/)
* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
