---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_HeadingPairs metod"
linktitle: "get_HeadingPairs"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_HeadingPairs metod. Anger dokumentrubriker och deras namn i C++."
type: docs
weight: 12000
url: /sv/cpp/aspose.words.properties/builtindocumentproperties/get_headingpairs/
---
## BuiltInDocumentProperties::get_HeadingPairs method


Anger dokumentrubriker och deras namn.

```cpp
System::ArrayPtr<System::SharedPtr<System::Object>> Aspose::Words::Properties::BuiltInDocumentProperties::get_HeadingPairs()
```

## Anmärkningar


Varje rubrikpar upptar två element i denna array.

Det första elementet i paret är en **String** och specificerar rubrikens namn. Det andra elementet i paret är en **Int32** och specificerar antalet dokumentdelar för denna rubrik i egenskapen [TitlesOfParts](../get_titlesofparts/).

Den totala summan av räknare för alla rubrikpar i denna egenskap måste vara lika med antalet element i egenskapen [TitlesOfParts](../get_titlesofparts/).

Aspose.Words uppdaterar inte denna egenskap.

## Exempel



Visar förhållandet mellan egenskaperna "HeadingPairs" och "TitlesOfParts".
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Heading pairs and titles of parts.docx");

// Vi kan hitta de kombinerade värdena för dessa samlingar via
// "File" -> "Properties" -> "Advanced Properties" -> "Contents" flik.
// Egenskapen HeadingPairs är en samling av <string, int>-par som
// bestämmer hur många dokumentdelar en rubrik sträcker sig över.
System::ArrayPtr<System::SharedPtr<System::Object>> headingPairs = doc->get_BuiltInDocumentProperties()->get_HeadingPairs();

// Egenskapen TitlesOfParts innehåller namnen på de delar som tillhör ovanstående rubriker.
System::ArrayPtr<System::String> titlesOfParts = doc->get_BuiltInDocumentProperties()->get_TitlesOfParts();

int32_t headingPairsIndex = 0;
int32_t titlesOfPartsIndex = 0;
while (headingPairsIndex < headingPairs->get_Length())
{
    std::cout << System::String::Format(u"Parts for {0}:", headingPairs[headingPairsIndex++]) << std::endl;
    int32_t partsCount = System::Convert::ToInt32(headingPairs[headingPairsIndex++]);

    for (int32_t i = 0; i < partsCount; i++)
    {
        std::cout << System::String::Format(u"\t\"{0}\"", titlesOfParts[titlesOfPartsIndex++]) << std::endl;
    }
}
```

## Se även

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
