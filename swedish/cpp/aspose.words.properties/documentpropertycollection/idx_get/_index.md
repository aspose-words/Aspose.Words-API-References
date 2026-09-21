---
title: "Aspose::Words::Properties::DocumentPropertyCollection::idx_get metod"
linktitle: "idx_get"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Properties::DocumentPropertyCollection::idx_get metod. Returnerar ett DocumentProperty‑objekt efter index i C++."
type: docs
weight: 7000
url: /sv/cpp/aspose.words.properties/documentpropertycollection/idx_get/
---
## DocumentPropertyCollection::idx_get(int32_t) method


Returnerar ett [DocumentProperty](../../documentproperty/)‑objekt efter index.

```cpp
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> Aspose::Words::Properties::DocumentPropertyCollection::idx_get(int32_t index)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| index | int32_t | Nollbaserat index för det [DocumentProperty](../../documentproperty/) som ska hämtas. |

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
* Class [DocumentPropertyCollection](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentPropertyCollection::idx_get(System::String) method


Returnerar ett [DocumentProperty](../../documentproperty/)‑objekt baserat på egenskapens namn.

```cpp
virtual System::SharedPtr<Aspose::Words::Properties::DocumentProperty> Aspose::Words::Properties::DocumentPropertyCollection::idx_get(System::String name)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| namn | System::String | Det skiftlägesokänsliga namnet på egenskapen som ska hämtas. |
## Anmärkningar


Returnerar **null** om en egenskap med det angivna namnet inte hittas.

## Exempel



Visar hur man skapar en anpassad dokumentegenskap som innehåller ett datum och en tid.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

doc->get_CustomDocumentProperties()->Add(u"AuthorizationDate", System::DateTime::get_Now());
System::DateTime authorizationDate = doc->get_CustomDocumentProperties()->idx_get(u"AuthorizationDate")->ToDateTime();
std::cout << System::String::Format(u"Document authorized on {0}", authorizationDate) << std::endl;
```

## Se även

* Class [DocumentProperty](../../documentproperty/)
* Class [DocumentPropertyCollection](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
