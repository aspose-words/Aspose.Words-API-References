---
title: PhysicalFontInfo.EmbeddingLicensingRights
linktitle: EmbeddingLicensingRights
articleTitle: EmbeddingLicensingRights
second_title: Aspose.Words per .NET
description: Scopri la proprietà PhysicalFontInfo EmbeddingLicensingRights: sblocca i diritti essenziali di incorporamento dei font per un'integrazione di design impeccabile.
type: docs
weight: 10
url: /it/net/aspose.words.fonts/physicalfontinfo/embeddinglicensingrights/
---
## PhysicalFontInfo.EmbeddingLicensingRights property

Incorporamento dei diritti di licenza per il font.

```csharp
public FontEmbeddingLicensingRights EmbeddingLicensingRights { get; }
```

## Esempi

Mostra come ottenere informazioni sui diritti di licenza per i font incorporati (PhysicalFontInfo).

```csharp
FontSettings settings = FontSettings.DefaultInstance;
FontSourceBase source = settings.GetFontsSources()[0];

// Ottieni l'elenco dei font disponibili.
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

### Guarda anche

* class [FontEmbeddingLicensingRights](../../fontembeddinglicensingrights/)
* class [PhysicalFontInfo](../)
* spazio dei nomi [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../../)
