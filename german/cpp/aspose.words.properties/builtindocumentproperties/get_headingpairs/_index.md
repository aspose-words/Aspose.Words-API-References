---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_HeadingPairs Methode"
linktitle: "get_HeadingPairs"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_HeadingPairs Methode. Gibt Dokumentüberschriften und deren Namen in C++ an."
type: docs
weight: 12000
url: /de/cpp/aspose.words.properties/builtindocumentproperties/get_headingpairs/
---
## BuiltInDocumentProperties::get_HeadingPairs method


Gibt Dokumentüberschriften und deren Namen an.

```cpp
System::ArrayPtr<System::SharedPtr<System::Object>> Aspose::Words::Properties::BuiltInDocumentProperties::get_HeadingPairs()
```

## Hinweise


Jedes Überschriftenpaar belegt zwei Elemente in diesem Array.

Das erste Element des Paares ist ein **String** und gibt den Überschriftennamen an. Das zweite Element des Paares ist ein **Int32** und gibt die Anzahl der Dokumentteile für diese Überschrift in der [TitlesOfParts](../get_titlesofparts/) Eigenschaft an.

Die Gesamtsumme der Zählungen aller Überschriftenpaare in dieser Eigenschaft muss gleich der Anzahl der Elemente in der [TitlesOfParts](../get_titlesofparts/) Eigenschaft sein.

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
