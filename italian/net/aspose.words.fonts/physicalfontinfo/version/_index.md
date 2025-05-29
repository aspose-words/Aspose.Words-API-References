---
title: PhysicalFontInfo.Version
linktitle: Version
articleTitle: Version
second_title: Aspose.Words per .NET
description: Scopri la proprietà Versione di PhysicalFontInfo, accedi facilmente alla stringa della versione del font per una maggiore coerenza di design e una tipografia migliorata.
type: docs
weight: 50
url: /it/net/aspose.words.fonts/physicalfontinfo/version/
---
## PhysicalFontInfo.Version property

Stringa della versione del font.

```csharp
public string Version { get; }
```

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

* class [PhysicalFontInfo](../)
* spazio dei nomi [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../../)
