---
title: FontInfo.EmbeddingLicensingRights
linktitle: EmbeddingLicensingRights
articleTitle: EmbeddingLicensingRights
second_title: .NET için Aspose.Words
description: Kusursuz tasarım entegrasyonu için gömülü font lisanslama haklarınıza kolayca erişmek ve bunları yönetmek amacıyla FontInfo EmbeddingLicensingRights özelliğini keşfedin.
type: docs
weight: 30
url: /tr/net/aspose.words.fonts/fontinfo/embeddinglicensingrights/
---
## FontInfo.EmbeddingLicensingRights property

Gömülü yazı tipi lisanslama haklarını alır.

```csharp
public FontEmbeddingLicensingRights EmbeddingLicensingRights { get; }
```

## Notlar

Yazı tipi gömülmemişse değer null olabilir.

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

* class [FontEmbeddingLicensingRights](../../fontembeddinglicensingrights/)
* class [FontInfo](../)
* ad alanı [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../../)
