---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_TitlesOfParts-Methode"
linktitle: "get_TitlesOfParts"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_TitlesOfParts-Methode. Jeder String im Array gibt den Namen eines Teils im Dokument in C++ an."
type: docs
weight: 30000
url: /de/cpp/aspose.words.properties/builtindocumentproperties/get_titlesofparts/
---
## BuiltInDocumentProperties::get_TitlesOfParts method


Jeder String im Array gibt den Namen eines Teils im Dokument an.

```cpp
System::ArrayPtr<System::String> Aspose::Words::Properties::BuiltInDocumentProperties::get_TitlesOfParts()
```

## Hinweise


Aspose.Words aktualisiert diese Eigenschaft nicht.

## Beispiele



Zeigt die Beziehung zwischen den Eigenschaften \"HeadingPairs\" und \"TitlesOfParts\".
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Heading pairs and titles of parts.docx");

// Wir können die kombinierten Werte dieser Sammlungen finden über
// \"Datei\" -> \"Eigenschaften\" -> \"Erweiterte Eigenschaften\" -> \"Inhalte\" Registerkarte.
// Die HeadingPairs-Eigenschaft ist eine Sammlung von <string, int>-Paaren, die
// bestimmt, über wie viele Dokumentteile sich eine Überschrift erstreckt.
System::ArrayPtr<System::SharedPtr<System::Object>> headingPairs = doc->get_BuiltInDocumentProperties()->get_HeadingPairs();

// Die TitlesOfParts-Eigenschaft enthält die Namen der Teile, die zu den oben genannten Überschriften gehören.
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

## Siehe auch

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
