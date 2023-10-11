---
title: PhysicalFontInfo.FilePath
second_title: Aspose.Words für .NET-API-Referenz
description: PhysicalFontInfo eigendom. Pfad zur Schriftartdatei falls vorhanden.
type: docs
weight: 10
url: /de/net/aspose.words.fonts/physicalfontinfo/filepath/
---
## PhysicalFontInfo.FilePath property

Pfad zur Schriftartdatei, falls vorhanden.

```csharp
public string FilePath { get; }
```

### Beispiele

Zeigt, wie verfügbare Schriftarten aufgelistet werden.

```csharp
// Aspose.Words so konfigurieren, dass Schriftarten aus einem benutzerdefinierten Ordner stammen, und dann jede verfügbare Schriftart drucken.
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
* namensraum [Aspose.Words.Fonts](../../physicalfontinfo/)
* Montage [Aspose.Words](../../../)


