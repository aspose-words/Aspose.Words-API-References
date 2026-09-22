---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_TitlesOfParts metodu"
linktitle: "get_TitlesOfParts"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_TitlesOfParts metodu. Dizideki her dize, belgede bir parçanın adını C++'ta belirtir."
type: docs
weight: 30000
url: /tr/cpp/aspose.words.properties/builtindocumentproperties/get_titlesofparts/
---
## BuiltInDocumentProperties::get_TitlesOfParts method


Dizideki her dize, belgedeki bir parçanın adını belirtir.

```cpp
System::ArrayPtr<System::String> Aspose::Words::Properties::BuiltInDocumentProperties::get_TitlesOfParts()
```

## Açıklamalar


Aspose.Words bu özelliği güncellemez.

## Örnekler



Shows the relationship between "HeadingPairs" and "TitlesOfParts" properties.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Heading pairs and titles of parts.docx");

// Bu koleksiyonların birleşik değerlerini şu şekilde bulabiliriz:
// "File" -> "Properties" -> "Advanced Properties" -> "Contents" sekmesi.
// HeadingPairs özelliği, <string, int> çiftlerinden oluşan bir koleksiyondur ve
// bir başlığın kaç belge parçası boyunca uzandığını belirler.
System::ArrayPtr<System::SharedPtr<System::Object>> headingPairs = doc->get_BuiltInDocumentProperties()->get_HeadingPairs();

// TitlesOfParts özelliği, yukarıdaki başlıklara ait parçaların adlarını içerir.
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

## Ayrıca Bakınız

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
