---
title: FontInfo.Name
linktitle: Name
articleTitle: Name
second_title: .NET için Aspose.Words
description: Projelerinizde gelişmiş tipografi için font adlarına kolayca erişmek ve kullanmak amacıyla FontInfo Name özelliğini keşfedin.
type: docs
weight: 60
url: /tr/net/aspose.words.fonts/fontinfo/name/
---
## FontInfo.Name property

Yazı tipinin adını alır.

```csharp
public string Name { get; }
```

## Notlar

Olamaz`hükümsüz`. Boş bir dize olabilir.

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
