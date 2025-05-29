---
title: PhysicalFontInfo.FilePath
linktitle: FilePath
articleTitle: FilePath
second_title: Aspose.Words per .NET
description: Scopri la proprietà PhysicalFontInfo FilePath, individua facilmente i file dei tuoi font per un'integrazione perfetta del design e una tipografia migliorata nei tuoi progetti.
type: docs
weight: 20
url: /it/net/aspose.words.fonts/physicalfontinfo/filepath/
---
## PhysicalFontInfo.FilePath property

Percorso al file del font, se presente.

```csharp
public string FilePath { get; }
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
