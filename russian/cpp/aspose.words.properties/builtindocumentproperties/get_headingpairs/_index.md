---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_HeadingPairs метод"
linktitle: "get_HeadingPairs"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_HeadingPairs метод. Указывает заголовки документа и их имена в C++."
type: docs
weight: 12000
url: /ru/cpp/aspose.words.properties/builtindocumentproperties/get_headingpairs/
---
## BuiltInDocumentProperties::get_HeadingPairs method


Указывает заголовки документа и их названия.

```cpp
System::ArrayPtr<System::SharedPtr<System::Object>> Aspose::Words::Properties::BuiltInDocumentProperties::get_HeadingPairs()
```

## Примечания


Каждая пара заголовков занимает два элемента в этом массиве.

Первый элемент пары — это **String** и указывает имя заголовка. Второй элемент пары — это **Int32** и указывает количество частей документа для этого заголовка в свойстве [TitlesOfParts](../get_titlesofparts/).

Общая сумма количеств для всех пар заголовков в этом свойстве должна быть равна количеству элементов в свойстве [TitlesOfParts](../get_titlesofparts/).

Aspose.Words не обновляет это свойство.

## Примеры



Показывает взаимосвязь между свойствами \"HeadingPairs\" и \"TitlesOfParts\".
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Heading pairs and titles of parts.docx");

// Мы можем найти объединённые значения этих коллекций через
// \"File\" -> \"Properties\" -> \"Advanced Properties\" -> \"Contents\" вкладка.
// Свойство HeadingPairs представляет собой коллекцию пар <string, int>, которые
// определяет, сколько частей документа охватывает заголовок.
System::ArrayPtr<System::SharedPtr<System::Object>> headingPairs = doc->get_BuiltInDocumentProperties()->get_HeadingPairs();

// Свойство TitlesOfParts содержит имена частей, которые относятся к вышеуказанным заголовкам.
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

## См. также

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
