---
title: FontInfo.EmbeddingLicensingRights
linktitle: EmbeddingLicensingRights
articleTitle: EmbeddingLicensingRights
second_title: Aspose.Words per .NET
description: Scopri la proprietà FontInfo EmbeddingLicensingRights per accedere e gestire facilmente i diritti di licenza dei tuoi font incorporati, per un'integrazione di design senza soluzione di continuità.
type: docs
weight: 30
url: /it/net/aspose.words.fonts/fontinfo/embeddinglicensingrights/
---
## FontInfo.EmbeddingLicensingRights property

Ottiene i diritti di licenza del font incorporato.

```csharp
public FontEmbeddingLicensingRights EmbeddingLicensingRights { get; }
```

## Osservazioni

Il valore potrebbe essere nullo se il font non è incorporato.

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

* class [FontEmbeddingLicensingRights](../../fontembeddinglicensingrights/)
* class [FontInfo](../)
* spazio dei nomi [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../../)
