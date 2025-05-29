---
title: PhysicalFontInfo.FontFamilyName
linktitle: FontFamilyName
articleTitle: FontFamilyName
second_title: Aspose.Words für .NET
description: Entdecken Sie die PhysicalFontInfo FontFamilyName-Eigenschaft, Ihren Schlüssel zum Identifizieren und effektiven Verwenden von Schriftfamilien in Ihren Projekten.
type: docs
weight: 30
url: /de/net/aspose.words.fonts/physicalfontinfo/fontfamilyname/
---
## PhysicalFontInfo.FontFamilyName property

Familienname der Schriftart.

```csharp
public string FontFamilyName { get; }
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
