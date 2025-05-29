---
title: PhysicalFontInfo.FullFontName
linktitle: FullFontName
articleTitle: FullFontName
second_title: Aspose.Words per .NET
description: Scopri la proprietà FullFontName di PhysicalFontInfo per accedere facilmente ai nomi dei font. Migliora la tua tipografia con un'identificazione precisa dei font!
type: docs
weight: 40
url: /it/net/aspose.words.fonts/physicalfontinfo/fullfontname/
---
## PhysicalFontInfo.FullFontName property

Nome completo del font.

```csharp
public string FullFontName { get; }
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
