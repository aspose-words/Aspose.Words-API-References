---
title: FontEmbeddingLicensingRights Class
linktitle: FontEmbeddingLicensingRights
articleTitle: FontEmbeddingLicensingRights
second_title: .NET için Aspose.Words
description: Font yerleştirme haklarını zahmetsizce yönetmek ve belgenizin sunumunu geliştirmek için Aspose.Words.Fonts.FontEmbeddingLicensingRights sınıfını keşfedin.
type: docs
weight: 3310
url: /tr/net/aspose.words.fonts/fontembeddinglicensingrights/
---
## FontEmbeddingLicensingRights class

Yazı tipi için gömülü lisanslama haklarını temsil eder.

```csharp
public class FontEmbeddingLicensingRights
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [BitmapEmbeddingOnly](../../aspose.words.fonts/fontembeddinglicensingrights/bitmapembeddingonly/) { get; } | "Yalnızca bitmap yerleştirme" kısıtlamasını belirtir. |
| [EmbeddingUsagePermissions](../../aspose.words.fonts/fontembeddinglicensingrights/embeddingusagepermissions/) { get; } | Kullanım izinleri. |
| [NoSubsetting](../../aspose.words.fonts/fontembeddinglicensingrights/nosubsetting/) { get; } | "Alt kümeleme yok" kısıtlamasını belirtir. |

## Notlar

Daha fazla bilgi edinmek için adresini ziyaret edin[OpenType spesifikasyon bölümü](https://learn.microsoft.com/en-us/typography/opentype/spec/os2#fstype) Microsoft Tipografi portalında.

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

* ad alanı [Aspose.Words.Fonts](../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../)
