---
title: FontEmbeddingLicensingRights.EmbeddingUsagePermissions
linktitle: EmbeddingUsagePermissions
articleTitle: EmbeddingUsagePermissions
second_title: Aspose.Words per .NET
description: Sprigiona il tuo potenziale creativo con i diritti di licenza per l'incorporamento dei font. Esplora le autorizzazioni di utilizzo per una perfetta integrazione dei font nei tuoi progetti.
type: docs
weight: 20
url: /it/net/aspose.words.fonts/fontembeddinglicensingrights/embeddingusagepermissions/
---
## FontEmbeddingLicensingRights.EmbeddingUsagePermissions property

Permessi di utilizzo.

```csharp
public FontEmbeddingUsagePermissions EmbeddingUsagePermissions { get; }
```

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

* enum [FontEmbeddingUsagePermissions](../../fontembeddingusagepermissions/)
* class [FontEmbeddingLicensingRights](../)
* spazio dei nomi [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../../)
