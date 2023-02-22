---
title: Class PhysicalFontInfo
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Fonts.PhysicalFontInfo klas. Gibt Informationen über physische Schriftarten an die für die Aspose.WordsSchriftartEngine verfügbar sind.
type: docs
weight: 2850
url: /de/net/aspose.words.fonts/physicalfontinfo/
---
## PhysicalFontInfo class

Gibt Informationen über physische Schriftarten an, die für die Aspose.Words-Schriftart-Engine verfügbar sind.

```csharp
public class PhysicalFontInfo
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [FilePath](../../aspose.words.fonts/physicalfontinfo/filepath/) { get; } | Pfad zur Schriftdatei, falls vorhanden. |
| [FontFamilyName](../../aspose.words.fonts/physicalfontinfo/fontfamilyname/) { get; } | Familienname der Schriftart. |
| [FullFontName](../../aspose.words.fonts/physicalfontinfo/fullfontname/) { get; } | Vollständiger Name der Schriftart. |
| [Version](../../aspose.words.fonts/physicalfontinfo/version/) { get; } | Versionsstring der Schriftart. |

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

* namensraum [Aspose.Words.Fonts](../../aspose.words.fonts/)
* Montage [Aspose.Words](../../)


