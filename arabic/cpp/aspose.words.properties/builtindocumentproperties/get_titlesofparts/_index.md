---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_TitlesOfParts طريقة"
linktitle: "get_TitlesOfParts"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_TitlesOfParts طريقة. كل سلسلة في المصفوفة تحدد اسم جزء في المستند بلغة C++."
type: docs
weight: 30000
url: /ar/cpp/aspose.words.properties/builtindocumentproperties/get_titlesofparts/
---
## BuiltInDocumentProperties::get_TitlesOfParts method


كل سلسلة في المصفوفة تحدد اسم جزء في المستند.

```cpp
System::ArrayPtr<System::String> Aspose::Words::Properties::BuiltInDocumentProperties::get_TitlesOfParts()
```

## ملاحظات


Aspose.Words لا يقوم بتحديث هذه الخاصية.

## أمثلة



يعرض العلاقة بين خاصيتي "HeadingPairs" و "TitlesOfParts".
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Heading pairs and titles of parts.docx");

// يمكننا العثور على القيم المدمجة لهذه المجموعات عبر
// \"File\" -> \"Properties\" -> \"Advanced Properties\" -> \"Contents\" علامة تبويب.
// خاصية HeadingPairs هي مجموعة من أزواج <string, int> التي
// تحدد عدد أجزاء المستند التي يغطيها العنوان.
System::ArrayPtr<System::SharedPtr<System::Object>> headingPairs = doc->get_BuiltInDocumentProperties()->get_HeadingPairs();

// خاصية TitlesOfParts تحتوي على أسماء الأجزاء التي تنتمي إلى العناوين أعلاه.
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

## انظر أيضًا

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
