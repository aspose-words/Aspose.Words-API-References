---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_HeadingPairs yöntemi"
linktitle: "get_HeadingPairs"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_HeadingPairs yöntemi. Belge başlıklarını ve bunların adlarını belirtir C++'da."
type: docs
weight: 12000
url: /tr/cpp/aspose.words.properties/builtindocumentproperties/get_headingpairs/
---
## BuiltInDocumentProperties::get_HeadingPairs method


Belge başlıklarını ve bunların adlarını belirtir.

```cpp
System::ArrayPtr<System::SharedPtr<System::Object>> Aspose::Words::Properties::BuiltInDocumentProperties::get_HeadingPairs()
```

## Açıklamalar


Bu dizide her başlık çifti iki öğe kaplar.

Çiftin ilk öğesi bir **String** olup başlık adını belirtir. Çiftin ikinci öğesi bir **Int32** olup bu başlık için belge parçalarının sayısını [TitlesOfParts](../get_titlesofparts/) özelliğinde belirtir.

Bu özellikteki tüm başlık çiftlerinin toplam sayısı, [TitlesOfParts](../get_titlesofparts/) özelliğindeki öğe sayısına eşit olmalıdır.

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
