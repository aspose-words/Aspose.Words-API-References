---
title: FontSourceBase.GetAvailableFonts
second_title: Aspose.Words per .NET API Reference
description: FontSourceBase metodo. Restituisce lelenco dei caratteri disponibili tramite questa origine.
type: docs
weight: 40
url: /it/net/aspose.words.fonts/fontsourcebase/getavailablefonts/
---
## FontSourceBase.GetAvailableFonts method

Restituisce l'elenco dei caratteri disponibili tramite questa origine.

```csharp
public IList<PhysicalFontInfo> GetAvailableFonts()
```

### Esempi

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

* class [PhysicalFontInfo](../../physicalfontinfo/)
* class [FontSourceBase](../)
* spazio dei nomi [Aspose.Words.Fonts](../../fontsourcebase/)
* assemblea [Aspose.Words](../../../)


