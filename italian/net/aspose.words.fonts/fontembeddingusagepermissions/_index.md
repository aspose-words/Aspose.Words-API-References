---
title: FontEmbeddingUsagePermissions Enum
linktitle: FontEmbeddingUsagePermissions
articleTitle: FontEmbeddingUsagePermissions
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.Fonts.FontEmbeddingUsagePermissions, che consente un controllo preciso sulle autorizzazioni di incorporamento dei font per una migliore gestione dei documenti.
type: docs
weight: 3320
url: /it/net/aspose.words.fonts/fontembeddingusagepermissions/
---
## FontEmbeddingUsagePermissions enumeration

Rappresenta i permessi di utilizzo dell'incorporamento del font.

```csharp
public enum FontEmbeddingUsagePermissions
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Installable | `0` | Il font può essere incorporato e può essere installato in modo permanente per l'uso su sistemi remoti o per l'uso da parte di altri utenti. |
| RestrictedLicense | `1` | Il font non deve essere modificato, incorporato o scambiato in alcun modo senza prima ottenere l'esplicita autorizzazione del legittimo proprietario. |
| PrintAndPreview | `2` | Il font potrebbe essere incorporato e potrebbe essere caricato temporaneamente su altri sistemi allo scopo di visualizzare o stampare il documento. |
| Editable | `3` | Il font potrebbe essere incorporato e potrebbe essere caricato temporaneamente su altri sistemi. |

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
