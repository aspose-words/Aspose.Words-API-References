---
title: FontInfo.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words for .NET
description: Discover the FontInfo Name property to easily access and utilize font names for enhanced typography in your projects.
type: docs
weight: 60
url: /net/aspose.words.fonts/fontinfo/name/
---
## FontInfo.Name property

Gets the name of the font.

```csharp
public string Name { get; }
```

## Remarks

Cannot be `null`. Can be an empty string.

## Examples

Shows how to print the details of what fonts are present in a document.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfoCollection allFonts = doc.FontInfos;
// Print all the used and unused fonts in the document.
for (int i = 0; i < allFonts.Count; i++)
{
    Console.WriteLine($"Font index #{i}");
    Console.WriteLine($"\tName: {allFonts[i].Name}");
    Console.WriteLine($"\tIs {(allFonts[i].IsTrueType ? "" : "not ")}a trueType font");
}
```

### See Also

* class [FontInfo](../)
* namespace [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assembly [Aspose.Words](../../../)
