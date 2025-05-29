---
title: PhysicalFontInfo.FilePath
linktitle: FilePath
articleTitle: FilePath
second_title: Aspose.Words für .NET
description: Entdecken Sie die PhysicalFontInfo FilePath-Eigenschaft, finden Sie Ihre Schriftdateien einfach für eine nahtlose Designintegration und verbesserte Typografie in Ihren Projekten.
type: docs
weight: 20
url: /de/net/aspose.words.fonts/physicalfontinfo/filepath/
---
## PhysicalFontInfo.FilePath property

Pfad zur Schriftartdatei, falls vorhanden.

```csharp
public string FilePath { get; }
```

## Beispiele

Zeigt, wie verfügbare Schriftarten aufgelistet werden.

```csharp
// Konfigurieren Sie Aspose.Words so, dass Schriftarten aus einem benutzerdefinierten Ordner bezogen werden, und drucken Sie dann alle verfügbaren Schriftarten.
FontSourceBase[] folderFontSource = { new FolderFontSource(FontsDir, true) };

foreach (PhysicalFontInfo fontInfo in folderFontSource[0].GetAvailableFonts())
{
    Console.WriteLine("FontFamilyName : {0}", fontInfo.FontFamilyName);
    Console.WriteLine("FullFontName  : {0}", fontInfo.FullFontName);
    Console.WriteLine("Version  : {0}", fontInfo.Version);
    Console.WriteLine("FilePath : {0}\n", fontInfo.FilePath);
}
```

### Siehe auch

* class [PhysicalFontInfo](../)
* namensraum [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Montage [Aspose.Words](../../../)
