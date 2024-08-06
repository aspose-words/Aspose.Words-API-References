---
title: FontInfo.IsTrueType
linktitle: IsTrueType
articleTitle: IsTrueType
second_title: Aspose.Words for .NET
description: FontInfo IsTrueType property. Indicates that this font is a TrueType or OpenType font as opposed to a raster or vector font. Default is true in C#.
type: docs
weight: 50
url: /net/aspose.words.fonts/fontinfo/istruetype/
---
## FontInfo.IsTrueType property

Indicates that this font is a TrueType or OpenType font as opposed to a raster or vector font. Default is `true`.

```csharp
public bool IsTrueType { get; set; }
```

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
