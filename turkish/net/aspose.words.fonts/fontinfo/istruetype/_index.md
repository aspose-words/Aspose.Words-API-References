---
title: FontInfo.IsTrueType
linktitle: IsTrueType
articleTitle: IsTrueType
second_title: .NET için Aspose.Words
description: Üstün kalite için yazı tipinizin TrueType veya OpenType olduğundan emin olmak için FontInfo'nun IsTrueType özelliğini keşfedin; net ve ölçeklenebilir tasarımlar için mükemmeldir.
type: docs
weight: 50
url: /tr/net/aspose.words.fonts/fontinfo/istruetype/
---
## FontInfo.IsTrueType property

Bu yazı tipinin raster veya vektör yazı tipinin aksine TrueType veya OpenType yazı tipi olduğunu belirtir. Varsayılan`doğru` .

```csharp
public bool IsTrueType { get; set; }
```

## Örnekler

Bir belgede hangi yazı tiplerinin bulunduğunun ayrıntılarının nasıl yazdırılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfoCollection allFonts = doc.FontInfos;
// Belgedeki tüm kullanılan ve kullanılmayan yazı tiplerini yazdır.
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
