---
title: FontEmbeddingLicensingRights Class
linktitle: FontEmbeddingLicensingRights
articleTitle: FontEmbeddingLicensingRights
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Fonts.FontEmbeddingLicensingRights per gestire senza sforzo i diritti di incorporamento dei font e migliorare la presentazione del tuo documento.
type: docs
weight: 3310
url: /it/net/aspose.words.fonts/fontembeddinglicensingrights/
---
## FontEmbeddingLicensingRights class

Rappresenta i diritti di licenza di incorporamento per il font.

```csharp
public class FontEmbeddingLicensingRights
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [BitmapEmbeddingOnly](../../aspose.words.fonts/fontembeddinglicensingrights/bitmapembeddingonly/) { get; } | Indica la restrizione "Solo incorporamento bitmap". |
| [EmbeddingUsagePermissions](../../aspose.words.fonts/fontembeddinglicensingrights/embeddingusagepermissions/) { get; } | Permessi di utilizzo. |
| [NoSubsetting](../../aspose.words.fonts/fontembeddinglicensingrights/nosubsetting/) { get; } | Indica la restrizione "Nessun sottoinsieme". |

## Osservazioni

Per saperne di più, visita [Sezione delle specifiche OpenType](https://learn.microsoft.com/en-us/typography/opentype/spec/os2#fstype) sul portale Microsoft Typography.

## Esempi

Mostra come ottenere informazioni sui diritti di licenza per i font incorporati (FontInfo).

```csharp
Document doc = new Document(MyDir + "Embedded font rights.docx");

// Ottieni l'elenco dei font del documento.
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

### Guarda anche

* spazio dei nomi [Aspose.Words.Fonts](../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../)
