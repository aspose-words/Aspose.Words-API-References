---
title: FontEmbeddingLicensingRights.BitmapEmbeddingOnly
linktitle: BitmapEmbeddingOnly
articleTitle: BitmapEmbeddingOnly
second_title: .NET için Aspose.Words
description: Gelişmiş tasarım kontrolü için özel Bitmap yerleştirme kısıtlamaları sağlayan FontEmbeddingLicensingRights BitmapEmbeddingOnly özelliğini keşfedin.
type: docs
weight: 10
url: /tr/net/aspose.words.fonts/fontembeddinglicensingrights/bitmapembeddingonly/
---
## FontEmbeddingLicensingRights.BitmapEmbeddingOnly property

"Yalnızca bitmap yerleştirme" kısıtlamasını belirtir.

```csharp
public bool BitmapEmbeddingOnly { get; }
```

## Notlar

Bu bit ayarlandığında, yalnızca yazı tipinde bulunan bit eşlemleri gömülebilir. Anahat verileri gömülemez. Yazı tipinde kullanılabilir bit eşlem yoksa, yazı tipi gömülemez olarak kabul edilir ve embedding hizmetleri başarısız olur. Diğer gömme kısıtlamaları da geçerlidir.

## Örnekler

Gömülü fontlar için lisans hakları bilgilerinin nasıl alınacağını gösterir (FontInfo).

```csharp
Document doc = new Document(MyDir + "Embedded font rights.docx");

// Belge yazı tiplerinin listesini al.
FontInfoCollection fontInfos = doc.FontInfos;
foreach (FontInfo fontInfo in fontInfos) 
{
    if (fontInfo.EmbeddingLicensingRights != null)
    {
        Console.WriteLine(fontInfo.EmbeddingLicensingRights.EmbeddingUsagePermissions);
        Console.WriteLine(fontInfo.EmbeddingLicensingRights.BitmapEmbeddingOnly);
        Console.WriteLine(fontInfo.EmbeddingLicensingRights.NoSubsetting);
    }
}
```

### Ayrıca bakınız

* class [FontEmbeddingLicensingRights](../)
* ad alanı [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../../)
