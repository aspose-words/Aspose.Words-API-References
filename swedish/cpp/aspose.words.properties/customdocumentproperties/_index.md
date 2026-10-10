---
title: "Aspose::Words::Properties::CustomDocumentProperties class"
linktitle: "CustomDocumentProperties"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Properties::CustomDocumentProperties class. En samling av anpassade dokumentegenskaper. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.properties/customdocumentproperties/
---
## CustomDocumentProperties class


En samling av anpassade dokumentegenskaper. För att lära dig mer, besök dokumentationsartikeln [Work with Document Properties](https://docs.aspose.com/words/cpp/work-with-document-properties/).

```cpp
class CustomDocumentProperties : public Aspose::Words::Properties::DocumentPropertyCollection
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [Add](./add/)(const System::String\&, const System::String\&) | Skapar en ny anpassad dokumentegenskap av datatypen [String](../propertytype/). |
| [Add](./add/)(const System::String\&, int32_t) | Skapar en ny anpassad dokumentegenskap av datatypen [Number](../propertytype/). |
| [Add](./add/)(const System::String\&, System::DateTime) | Skapar en ny anpassad dokumentegenskap av datatypen [DateTime](../propertytype/). |
| [Add](./add/)(const System::String\&, bool) | Skapar en ny anpassad dokumentegenskap av datatypen [Boolean](../propertytype/). |
| [Add](./add/)(const System::String\&, double) | Skapar en ny anpassad dokumentegenskap av datatypen [Double](../propertytype/). |
| [AddLinkToContent](./addlinktocontent/)(const System::String\&, const System::String\&) | Skapar en ny anpassad dokumentegenskap som är länkad till innehåll. |
| [Clear](../documentpropertycollection/clear/)() | Tar bort alla egenskaper från samlingen. |
| [Contains](../documentpropertycollection/contains/)(const System::String\&) | Returnerar **true** om en egenskap med det angivna namnet finns i samlingen. |
| [get_Count](../documentpropertycollection/get_count/)() | Hämtar antalet objekt i samlingen. |
| [GetEnumerator](../documentpropertycollection/getenumerator/)() override | Returnerar ett enumerator-objekt som kan användas för att iterera över alla objekt i samlingen. |
| [GetType](./gettype/)() const override |  |
| virtual [idx_get](../documentpropertycollection/idx_get/)(System::String) | Returnerar ett [DocumentProperty](../documentproperty/)-objekt med egenskapens namn. |
| [idx_get](../documentpropertycollection/idx_get/)(int32_t) | Returnerar ett [DocumentProperty](../documentproperty/)-objekt efter index. |
| [IndexOf](../documentpropertycollection/indexof/)(const System::String\&) | Hämtar indexet för en egenskap efter namn. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../documentpropertycollection/remove/)(const System::String\&) | Tar bort en egenskap med det angivna namnet från samlingen. |
| [RemoveAt](../documentpropertycollection/removeat/)(int32_t) | Tar bort en egenskap på det angivna indexet. |
| static [Type](./type/)() |  |
## Anmärkningar


Varje [DocumentProperty](../documentproperty/)-objekt representerar en anpassad egenskap för ett behållardokument.

Namnen på egenskaperna är skiftlägesokänsliga.

Egenskaperna i samlingen sorteras alfabetiskt efter namn.

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

* Class [DocumentPropertyCollection](../documentpropertycollection/)
* Namespace [Aspose::Words::Properties](../)
* Library [Aspose.Words for C++](../../)
