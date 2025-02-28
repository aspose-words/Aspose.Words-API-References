---
title: BuiltInDocumentProperties.TitlesOfParts
linktitle: TitlesOfParts
articleTitle: TitlesOfParts
second_title: Aspose.Words for .NET
description: Discover the TitlesOfParts property in BuiltInDocumentProperties. Easily manage document sections with clear, customizable part names for enhanced organization.
type: docs
weight: 330
url: /net/aspose.words.properties/builtindocumentproperties/titlesofparts/
---
## BuiltInDocumentProperties.TitlesOfParts property

Each string in the array specifies the name of a part in the document.

```csharp
public string[] TitlesOfParts { get; set; }
```

## Remarks

Aspose.Words does not update this property.

## Examples

Shows the relationship between "HeadingPairs" and "TitlesOfParts" properties.

```csharp
Document doc = new Document(MyDir + "Heading pairs and titles of parts.docx");

// We can find the combined values of these collections via
// "File" -> "Properties" -> "Advanced Properties" -> "Contents" tab.
// The HeadingPairs property is a collection of <string, int> pairs that
// determines how many document parts a heading spans across.
object[] headingPairs = doc.BuiltInDocumentProperties.HeadingPairs;

// The TitlesOfParts property contains the names of parts that belong to the above headings.
string[] titlesOfParts = doc.BuiltInDocumentProperties.TitlesOfParts;

int headingPairsIndex = 0;
int titlesOfPartsIndex = 0;
while (headingPairsIndex < headingPairs.Length)
{
    Console.WriteLine($"Parts for {headingPairs[headingPairsIndex++]}:");
    int partsCount = Convert.ToInt32(headingPairs[headingPairsIndex++]);

    for (int i = 0; i < partsCount; i++)
        Console.WriteLine($"\t\"{titlesOfParts[titlesOfPartsIndex++]}\"");
}
```

### See Also

* class [BuiltInDocumentProperties](../)
* namespace [Aspose.Words.Properties](../../../aspose.words.properties/)
* assembly [Aspose.Words](../../../)
