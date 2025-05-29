---
title: FontEmbeddingLicensingRights.BitmapEmbeddingOnly
linktitle: BitmapEmbeddingOnly
articleTitle: BitmapEmbeddingOnly
second_title: Aspose.Words per .NET
description: Scopri la proprietà FontEmbeddingLicensingRights BitmapEmbeddingOnly, che garantisce restrizioni esclusive all'incorporamento Bitmap per un controllo di progettazione avanzato.
type: docs
weight: 10
url: /it/net/aspose.words.fonts/fontembeddinglicensingrights/bitmapembeddingonly/
---
## FontEmbeddingLicensingRights.BitmapEmbeddingOnly property

Indica la restrizione "Solo incorporamento bitmap".

```csharp
public bool BitmapEmbeddingOnly { get; }
```

## Osservazioni

Quando questo bit è impostato, è possibile incorporare solo le bitmap contenute nel font. Non è possibile incorporare dati di contorno. Se non sono disponibili bitmap nel font, il font viene considerato non incorporabile e i servizi di incorporamento falliranno. Si applicano anche altre restrizioni di incorporamento.

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

* class [FontEmbeddingLicensingRights](../)
* spazio dei nomi [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../../)
