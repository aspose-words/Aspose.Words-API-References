---
title: PhysicalFontInfo.FontFamilyName
linktitle: FontFamilyName
articleTitle: FontFamilyName
second_title: Aspose.Words per .NET
description: Scopri la proprietà FontFamilyName di PhysicalFontInfo, la chiave per identificare e utilizzare in modo efficace le famiglie di font nei tuoi progetti.
type: docs
weight: 30
url: /it/net/aspose.words.fonts/physicalfontinfo/fontfamilyname/
---
## PhysicalFontInfo.FontFamilyName property

Nome della famiglia del font.

```csharp
public string FontFamilyName { get; }
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
