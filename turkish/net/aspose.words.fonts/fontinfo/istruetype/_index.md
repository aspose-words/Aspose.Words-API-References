---
title: FontInfo.IsTrueType
second_title: Aspose.Words for .NET API Referansı
description: FontInfo mülk. Bu yazı tipinin raster veya vektör yazı tipinin aksine bir TrueType veya OpenType yazı tipi olduğunu gösterir. Varsayılan değer true.
type: docs
weight: 40
url: /tr/net/aspose.words.fonts/fontinfo/istruetype/
---
## FontInfo.IsTrueType property

Bu yazı tipinin raster veya vektör yazı tipinin aksine bir TrueType veya OpenType yazı tipi olduğunu gösterir. Varsayılan değer true.

```csharp
public bool IsTrueType { get; set; }
```

### Örnekler

Bir belgede hangi yazı tiplerinin bulunduğunun ayrıntılarının nasıl yazdırılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfoCollection allFonts = doc.FontInfos;
// Belgedeki tüm kullanılmış ve kullanılmayan yazı tiplerini yazdırın.
for (int i = 0; i < allFonts.Count; i++)
{
    Console.WriteLine($"Font index #{i}");
    Console.WriteLine($"\tName: {allFonts[i].Name}");
    Console.WriteLine($"\tIs {(allFonts[i].IsTrueType ? "" : "not ")}a trueType font");
}
```

### Ayrıca bakınız

* class [FontInfo](../)
* ad alanı [Aspose.Words.Fonts](../../fontinfo/)
* toplantı [Aspose.Words](../../../)


