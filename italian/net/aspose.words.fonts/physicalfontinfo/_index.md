---
title: PhysicalFontInfo Class
linktitle: PhysicalFontInfo
articleTitle: PhysicalFontInfo
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Fonts.PhysicalFontInfo, che fornisce dettagli essenziali sui font fisici per migliorare l'elaborazione e la progettazione dei documenti.
type: docs
weight: 3460
url: /it/net/aspose.words.fonts/physicalfontinfo/
---
## PhysicalFontInfo class

Specifica informazioni sul font fisico disponibile per il motore di font Aspose.Words.

Per saperne di più, visita il[Lavorare con i font](https://docs.aspose.com/words/net/working-with-fonts/) articolo di documentazione.

```csharp
public class PhysicalFontInfo
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [EmbeddingLicensingRights](../../aspose.words.fonts/physicalfontinfo/embeddinglicensingrights/) { get; } | Incorporamento dei diritti di licenza per il font. |
| [FilePath](../../aspose.words.fonts/physicalfontinfo/filepath/) { get; } | Percorso al file del font, se presente. |
| [FontFamilyName](../../aspose.words.fonts/physicalfontinfo/fontfamilyname/) { get; } | Nome della famiglia del font. |
| [FullFontName](../../aspose.words.fonts/physicalfontinfo/fullfontname/) { get; } | Nome completo del font. |
| [Version](../../aspose.words.fonts/physicalfontinfo/version/) { get; } | Stringa della versione del font. |

## Esempi

Mostra come elencare i font disponibili.

```csharp
// Configurare Aspose.Words per ottenere i font da una cartella personalizzata e quindi stampare tutti i font disponibili.
FontSourceBase[] folderFontSource = { new FolderFontSource(FontsDir, true) };

foreach (PhysicalFontInfo fontInfo in folderFontSource[0].GetAvailableFonts())
{
    Console.WriteLine("FontFamilyName : {0}", fontInfo.FontFamilyName);
    Console.WriteLine("FullFontName  : {0}", fontInfo.FullFontName);
    Console.WriteLine("Version  : {0}", fontInfo.Version);
    Console.WriteLine("FilePath : {0}\n", fontInfo.FilePath);
}
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Fonts](../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../)
