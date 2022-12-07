---
title: get_HeadingPairs
second_title: Aspose.Words for C++ API Reference
description: Specifies document headings and their names.
type: docs
weight: 144
url: /cpp/aspose.words.properties/builtindocumentproperties/get_headingpairs/
---
## BuiltInDocumentProperties::get_HeadingPairs method


Specifies document headings and their names.

```cpp
System::ArrayPtr<System::SharedPtr<System::Object>> Aspose::Words::Properties::BuiltInDocumentProperties::get_HeadingPairs()
```

## Remarks


Every heading pair occupies two elements in this array.

The first element of the pair is a **String** and specifies the heading name. The second element of the pair is an **Int32** and specifies the count of document parts for this heading in the [TitlesOfParts](../get_titlesofparts/) property.

The total sum of counts for all heading pairs in this property must be equal to the number of elements in the [TitlesOfParts](../get_titlesofparts/) property.

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
