---
title: PhysicalFontInfo.EmbeddingLicensingRights
linktitle: EmbeddingLicensingRights
articleTitle: EmbeddingLicensingRights
second_title: .NET için Aspose.Words
description: PhysicalFontInfo EmbeddingLicensingRights özelliğini keşfedin; kusursuz tasarım entegrasyonu için temel font yerleştirme haklarının kilidini açın.
type: docs
weight: 10
url: /tr/net/aspose.words.fonts/physicalfontinfo/embeddinglicensingrights/
---
## PhysicalFontInfo.EmbeddingLicensingRights property

Yazı tipi için lisanslama haklarının gömülmesi.

```csharp
public FontEmbeddingLicensingRights EmbeddingLicensingRights { get; }
```

## Örnekler

Gömülü fontlar için lisans hakları bilgilerinin nasıl alınacağını gösterir (PhysicalFontInfo).

```csharp
FontSettings settings = FontSettings.DefaultInstance;
FontSourceBase source = settings.GetFontsSources()[0];

// Kullanılabilir yazı tiplerinin listesini al.
IList<PhysicalFontInfo> fontInfos = source.GetAvailableFonts();
foreach (PhysicalFontInfo fontInfo in fontInfos)
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

* class [FontEmbeddingLicensingRights](../../fontembeddinglicensingrights/)
* class [PhysicalFontInfo](../)
* ad alanı [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../../)
