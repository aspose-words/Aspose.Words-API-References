---
title: FontInfo.IsTrueType
linktitle: IsTrueType
articleTitle: IsTrueType
second_title: Aspose.Words for .NET
description: FontInfo IsTrueType mülk. Bu yazı tipinin raster veya vektör yazı tipi yerine TrueType veya OpenType yazı tipi olduğunu belirtir. Varsayılandoğru  C#'da.
type: docs
weight: 40
url: /tr/net/aspose.words.fonts/fontinfo/istruetype/
---
## FontInfo.IsTrueType property

Bu yazı tipinin raster veya vektör yazı tipi yerine TrueType veya OpenType yazı tipi olduğunu belirtir. Varsayılan:`doğru` .

```csharp
public bool IsTrueType { get; set; }
```

## Örnekler

Bir belgede hangi yazı tiplerinin mevcut olduğuna ilişkin ayrıntıların nasıl yazdırılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfoCollection allFonts = doc.FontInfos;
// Belgedeki tüm kullanılan ve kullanılmayan yazı tiplerini yazdırın.
for (int i = 0; i < allFonts.Count; i++)
{
    Console.WriteLine($"Font index #{i}");
    Console.WriteLine($"\tName: {allFonts[i].Name}");
    Console.WriteLine($"\tIs {(allFonts[i].IsTrueType ? "" : "not ")}a trueType font");
}
```

### Ayrıca bakınız

* class [FontInfo](../)
* ad alanı [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../../)
