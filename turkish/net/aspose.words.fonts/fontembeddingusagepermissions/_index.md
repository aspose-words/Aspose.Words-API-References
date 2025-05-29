---
title: FontEmbeddingUsagePermissions Enum
linktitle: FontEmbeddingUsagePermissions
articleTitle: FontEmbeddingUsagePermissions
second_title: .NET için Aspose.Words
description: Gelişmiş belge yönetimi için font yerleştirme izinleri üzerinde hassas kontrol sağlayan Aspose.Words.Fonts.FontEmbeddingUsagePermissions numaralandırmasını keşfedin.
type: docs
weight: 3320
url: /tr/net/aspose.words.fonts/fontembeddingusagepermissions/
---
## FontEmbeddingUsagePermissions enumeration

Yazı tipi yerleştirme kullanım izinlerini temsil eder.

```csharp
public enum FontEmbeddingUsagePermissions
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Installable | `0` | Yazı tipi gömülebilir ve uzak sistemlerde veya diğer kullanıcılar tarafından kullanılmak üzere kalıcı olarak kurulabilir. |
| RestrictedLicense | `1` | Yazı tipi, yasal sahibinin açık izni alınmadan hiçbir şekilde değiştirilemez, gömülemez veya değiştirilemez. |
| PrintAndPreview | `2` | Yazı tipi gömülebilir ve belgeyi görüntüleme veya yazdırma amaçlarıyla geçici olarak diğer sistemlere yüklenebilir. |
| Editable | `3` | Yazı tipi gömülebilir ve geçici olarak diğer sistemlere yüklenebilir. |

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
