---
title: FontSourceBase.GetAvailableFonts
linktitle: GetAvailableFonts
articleTitle: GetAvailableFonts
second_title: Aspose.Words per .NET
description: Scopri i font disponibili con il metodo GetAvailableFonts di FontSourceBase. Arricchisci i tuoi progetti con un'ampia selezione di caratteri di alta qualità!
type: docs
weight: 40
url: /it/net/aspose.words.fonts/fontsourcebase/getavailablefonts/
---
## FontSourceBase.GetAvailableFonts method

Restituisce l'elenco dei font disponibili tramite questa sorgente.

```csharp
public IList<PhysicalFontInfo> GetAvailableFonts()
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

* class [PhysicalFontInfo](../../physicalfontinfo/)
* class [FontSourceBase](../)
* spazio dei nomi [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../../)
