---
title: get_TitlesOfParts
second_title: Aspose.Words for C++ API Reference
description: Each string in the array specifies the name of a part in the document.
type: docs
weight: 378
url: /cpp/aspose.words.properties/builtindocumentproperties/get_titlesofparts/
---
## BuiltInDocumentProperties::get_TitlesOfParts method


Each string in the array specifies the name of a part in the document.

```cpp
System::ArrayPtr<System::String> Aspose::Words::Properties::BuiltInDocumentProperties::get_TitlesOfParts()
```

## Remarks


Aspose.Words does not update this property.

## Examples



Shows the relationship between "HeadingPairs" and "TitlesOfParts" properties. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Heading pairs and titles of parts.docx");

// We can find the combined values of these collections via
// "File" -> "Properties" -> "Advanced Properties" -> "Contents" tab.
// The HeadingPairs property is a collection of <string, int> pairs that
// determines how many document parts a heading spans across.
ArrayPtr<SharedPtr<System::Object>> headingPairs = doc->get_BuiltInDocumentProperties()->get_HeadingPairs();

// The TitlesOfParts property contains the names of parts that belong to the above headings.
ArrayPtr<String> titlesOfParts = doc->get_BuiltInDocumentProperties()->get_TitlesOfParts();

int headingPairsIndex = 0;
int titlesOfPartsIndex = 0;
while (headingPairsIndex < headingPairs->get_Length())
{
    std::cout << "Parts for " << headingPairs[headingPairsIndex++] << ":" << std::endl;
    int partsCount = System::Convert::ToInt32(headingPairs[headingPairsIndex++]);

    for (int i = 0; i < partsCount; i++)
    {
        std::cout << "\t\"" << titlesOfParts[titlesOfPartsIndex++] << "\"" << std::endl;
    }
}
```

## See Also

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words](../../../)
