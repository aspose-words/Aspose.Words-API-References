---
title: Aspose::Words::Properties::BuiltInDocumentProperties::set_HeadingPairs method
linktitle: set_HeadingPairs
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Properties::BuiltInDocumentProperties::set_HeadingPairs method. Specifies document headings and their names in C++.'
type: docs
weight: 47000
url: /cpp/aspose.words.properties/builtindocumentproperties/set_headingpairs/
---
## BuiltInDocumentProperties::set_HeadingPairs method


Specifies document headings and their names.

```cpp
void Aspose::Words::Properties::BuiltInDocumentProperties::set_HeadingPairs(const System::ArrayPtr<System::SharedPtr<System::Object>> & value)
```

## Remarks


Every heading pair occupies two elements in this array.

The first element of the pair is a **String** and specifies the heading name. The second element of the pair is an **Int32** and specifies the count of document parts for this heading in the [TitlesOfParts](../get_titlesofparts/) property.

The total sum of counts for all heading pairs in this property must be equal to the number of elements in the [TitlesOfParts](../get_titlesofparts/) property.

Aspose.Words does not update this property.
## Examples


Shows the relationship between "HeadingPairs" and "TitlesOfParts" properties.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Heading pairs and titles of parts.docx"));

// We can find the combined values of these collections via
// "File" -> "Properties" -> "Advanced Properties" -> "Contents" tab.
// The HeadingPairs property is a collection of <string, int> pairs that
// determines how many document parts a heading spans across.
System::ArrayPtr<System::SharedPtr<System::Object>> headingPairs = doc->get_BuiltInDocumentProperties()->get_HeadingPairs();

// The TitlesOfParts property contains the names of parts that belong to the above headings.
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
## See Also

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
