---
title: FontEmbeddingLicensingRights.NoSubsetting
linktitle: NoSubsetting
articleTitle: NoSubsetting
second_title: .NET için Aspose.Words
description: Alt Kümeleme Olmadan Font Gömme Lisanslama Haklarını Keşfedin. Uyumluluğu sağlayın ve tasarım projelerinizi geliştirirken fontlarınızı koruyun.
type: docs
weight: 30
url: /tr/net/aspose.words.fonts/fontembeddinglicensingrights/nosubsetting/
---
## FontEmbeddingLicensingRights.NoSubsetting property

"Alt kümeleme yok" kısıtlamasını belirtir.

```csharp
public bool NoSubsetting { get; }
```

## Notlar

Bu bayrak ayarlandığında, yazı tipi gömülmeden önce alt kümeye alınmamalıdır. Diğer gömme kısıtlamaları da geçerlidir.

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
