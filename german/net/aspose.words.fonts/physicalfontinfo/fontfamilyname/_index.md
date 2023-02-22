---
title: PhysicalFontInfo.FontFamilyName
second_title: Aspose.Words für .NET-API-Referenz
description: PhysicalFontInfo eigendom. Familienname der Schriftart.
type: docs
weight: 20
url: /de/net/aspose.words.fonts/physicalfontinfo/fontfamilyname/
---
## PhysicalFontInfo.FontFamilyName property

Familienname der Schriftart.

```csharp
public string FontFamilyName { get; }
```

### Beispiele

Zeigt, wie verfügbare Schriftarten aufgelistet werden.

```csharp
// Konfigurieren Sie Aspose.Words, um Schriftarten aus einem benutzerdefinierten Ordner zu beziehen, und drucken Sie dann jede verfügbare Schriftart.
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


