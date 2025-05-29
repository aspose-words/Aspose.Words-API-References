---
title: PhysicalFontInfo Class
linktitle: PhysicalFontInfo
articleTitle: PhysicalFontInfo
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Fonts.PhysicalFontInfo, die wichtige Details zu physischen Schriftarten für eine verbesserte Dokumentverarbeitung und -gestaltung bereitstellt.
type: docs
weight: 3460
url: /de/net/aspose.words.fonts/physicalfontinfo/
---
## PhysicalFontInfo class

Gibt Informationen über die physische Schriftart an, die der Aspose.Words-Schriftarten-Engine zur Verfügung steht.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Schriftarten](https://docs.aspose.com/words/net/working-with-fonts/) Dokumentationsartikel.

```csharp
public class PhysicalFontInfo
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [EmbeddingLicensingRights](../../aspose.words.fonts/physicalfontinfo/embeddinglicensingrights/) { get; } | Einbettungslizenzrechte für die Schriftart. |
| [FilePath](../../aspose.words.fonts/physicalfontinfo/filepath/) { get; } | Pfad zur Schriftartdatei, falls vorhanden. |
| [FontFamilyName](../../aspose.words.fonts/physicalfontinfo/fontfamilyname/) { get; } | Familienname der Schriftart. |
| [FullFontName](../../aspose.words.fonts/physicalfontinfo/fullfontname/) { get; } | Vollständiger Name der Schriftart. |
| [Version](../../aspose.words.fonts/physicalfontinfo/version/) { get; } | Versionszeichenfolge der Schriftart. |

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

* namensraum [Aspose.Words.Fonts](../../aspose.words.fonts/)
* Montage [Aspose.Words](../../)
