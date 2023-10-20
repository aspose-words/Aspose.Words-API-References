---
title: PhysicalFontInfo Class
linktitle: PhysicalFontInfo
articleTitle: PhysicalFontInfo
second_title: Aspose.Words per .NET
description: Aspose.Words.Fonts.PhysicalFontInfo classe. Specifica le informazioni sul carattere fisico disponibile per il motore dei caratteri Aspose.Words in C#.
type: docs
weight: 3030
url: /it/net/aspose.words.fonts/physicalfontinfo/
---
## PhysicalFontInfo class

Specifica le informazioni sul carattere fisico disponibile per il motore dei caratteri Aspose.Words.

Per saperne di più, visita il[Lavorare con i caratteri](https://docs.aspose.com/words/net/working-with-fonts/) articolo di documentazione.

```csharp
public class PhysicalFontInfo
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [FilePath](../../aspose.words.fonts/physicalfontinfo/filepath/) { get; } | Percorso del file del carattere, se presente. |
| [FontFamilyName](../../aspose.words.fonts/physicalfontinfo/fontfamilyname/) { get; } | Cognome del carattere. |
| [FullFontName](../../aspose.words.fonts/physicalfontinfo/fullfontname/) { get; } | Nome completo del carattere. |
| [Version](../../aspose.words.fonts/physicalfontinfo/version/) { get; } | Stringa della versione del carattere. |

## Esempi

Mostra come elencare i caratteri disponibili.

```csharp
// Configura Aspose.Words per ottenere i caratteri da una cartella personalizzata, quindi stampa tutti i caratteri disponibili.
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
