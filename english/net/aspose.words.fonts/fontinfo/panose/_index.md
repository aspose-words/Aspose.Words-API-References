---
title: FontInfo.Panose
second_title: Aspose.Words for .NET API Reference
description: FontInfo property. Gets or sets the PANOSE typeface classification number in C#.
type: docs
weight: 60
url: /net/aspose.words.fonts/fontinfo/panose/
---
## FontInfo.Panose property

Gets or sets the PANOSE typeface classification number.

```csharp
public byte[] Panose { get; set; }
```

## Remarks

PANOSE is a compact 10-byte description of a fonts critical visual characteristics, such as contrast, weight, and serif style. The digits represent Family Kind, Serif Style, Weight, Proportion, Contrast, Stroke Variation, Arm Style, Letterform, Midline, and X-Height.

Can be `null`.

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

* class [FontInfo](../)
* namespace [Aspose.Words.Fonts](../../fontinfo/)
* assembly [Aspose.Words](../../../)
