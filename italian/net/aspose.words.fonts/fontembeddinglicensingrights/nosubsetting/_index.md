---
title: FontEmbeddingLicensingRights.NoSubsetting
linktitle: NoSubsetting
articleTitle: NoSubsetting
second_title: Aspose.Words per .NET
description: Scopri i diritti di licenza per l'incorporamento dei font senza sottoinsiemi. Garantisci la conformità e proteggi i tuoi font, migliorando al contempo i tuoi progetti di design.
type: docs
weight: 30
url: /it/net/aspose.words.fonts/fontembeddinglicensingrights/nosubsetting/
---
## FontEmbeddingLicensingRights.NoSubsetting property

Indica la restrizione "Nessun sottoinsieme".

```csharp
public bool NoSubsetting { get; }
```

## Osservazioni

Quando questo flag è impostato, il font non deve essere sottoposto a subset prima dell'incorporamento. Si applicano anche altre restrizioni di incorporamento .

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
