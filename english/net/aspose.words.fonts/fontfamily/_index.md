---
title: FontFamily Enum
linktitle: FontFamily
articleTitle: FontFamily
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Fonts.FontFamily enum—your key to managing diverse font families effortlessly for enhanced document styling and formatting.
type: docs
weight: 3340
url: /net/aspose.words.fonts/fontfamily/
---
## FontFamily enumeration

Represents the font family.

```csharp
public enum FontFamily
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Auto | `0` | Specifies a generic family name. This name is used when information about a font does not exist or does not matter. The default font is used. |
| Roman | `1` | Specifies a proportional font with serifs. An example is Times New Roman. |
| Swiss | `2` | Specifies a proportional font without serifs. An example is Arial. |
| Modern | `3` | Specifies a monospace font with or without serifs. Monospace fonts are usually modern; examples include Pica, Elite, and Courier New. |
| Script | `4` | Specifies a font that is designed to look like handwriting; examples include Script and Cursive. |
| Decorative | `5` | Specifies a novelty font. An example is Old English. |

## Remarks

A font family is a set of fonts having common stroke width and serif characteristics.

## Examples

Shows how to access and print details of each font in a document.

```csharp
Document doc = new Document(MyDir + "Document.docx");

IEnumerator<FontInfo> fontCollectionEnumerator = doc.FontInfos.GetEnumerator();
while (fontCollectionEnumerator.MoveNext())
{
    FontInfo fontInfo = fontCollectionEnumerator.Current;
    if (fontInfo != null)
    {
        Console.WriteLine("Font name: " + fontInfo.Name);

        // Alt names are usually blank.
        Console.WriteLine("Alt name: " + fontInfo.AltName);
        Console.WriteLine("\t- Family: " + fontInfo.Family);
        Console.WriteLine("\t- " + (fontInfo.IsTrueType ? "Is TrueType" : "Is not TrueType"));
        Console.WriteLine("\t- Pitch: " + fontInfo.Pitch);
        Console.WriteLine("\t- Charset: " + fontInfo.Charset);
        Console.WriteLine("\t- Panose:");
        Console.WriteLine("\t\tFamily Kind: " + fontInfo.Panose[0]);
        Console.WriteLine("\t\tSerif Style: " + fontInfo.Panose[1]);
        Console.WriteLine("\t\tWeight: " + fontInfo.Panose[2]);
        Console.WriteLine("\t\tProportion: " + fontInfo.Panose[3]);
        Console.WriteLine("\t\tContrast: " + fontInfo.Panose[4]);
        Console.WriteLine("\t\tStroke Variation: " + fontInfo.Panose[5]);
        Console.WriteLine("\t\tArm Style: " + fontInfo.Panose[6]);
        Console.WriteLine("\t\tLetterform: " + fontInfo.Panose[7]);
        Console.WriteLine("\t\tMidline: " + fontInfo.Panose[8]);
        Console.WriteLine("\t\tX-Height: " + fontInfo.Panose[9]);
    }
}
```

### See Also

* namespace [Aspose.Words.Fonts](../../aspose.words.fonts/)
* assembly [Aspose.Words](../../)
