---
title: PhysicalFontInfo Class
linktitle: PhysicalFontInfo
articleTitle: PhysicalFontInfo
second_title: Aspose.Words für .NET
description: Aspose.Words.Fonts.PhysicalFontInfo klas. Gibt Informationen über die physische Schriftart an die für die Aspose.WordsSchriftartEngine verfügbar ist in C#.
type: docs
weight: 3030
url: /de/net/aspose.words.fonts/physicalfontinfo/
---
## PhysicalFontInfo class

Gibt Informationen über die physische Schriftart an, die für die Aspose.Words-Schriftart-Engine verfügbar ist.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Schriftarten](https://docs.aspose.com/words/net/working-with-fonts/) Dokumentationsartikel.

```csharp
public class PhysicalFontInfo
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [FilePath](../../aspose.words.fonts/physicalfontinfo/filepath/) { get; } | Pfad zur Schriftartdatei, falls vorhanden. |
| [FontFamilyName](../../aspose.words.fonts/physicalfontinfo/fontfamilyname/) { get; } | Familienname der Schriftart. |
| [FullFontName](../../aspose.words.fonts/physicalfontinfo/fullfontname/) { get; } | Vollständiger Name der Schriftart. |
| [Version](../../aspose.words.fonts/physicalfontinfo/version/) { get; } | Versionszeichenfolge der Schriftart. |

## Beispiele

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

* namensraum [Aspose.Words.Fonts](../../aspose.words.fonts/)
* Montage [Aspose.Words](../../)
