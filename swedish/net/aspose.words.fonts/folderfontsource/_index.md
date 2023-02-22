---
title: Class FolderFontSource
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Fonts.FolderFontSource klass. Representerar mappen som innehåller TrueTypeteckensnittsfiler.
type: docs
weight: 2700
url: /sv/net/aspose.words.fonts/folderfontsource/
---
## FolderFontSource class

Representerar mappen som innehåller TrueType-teckensnittsfiler.

```csharp
public class FolderFontSource : FontSourceBase
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [FolderFontSource](folderfontsource/#constructor)(string, bool) | Ctor. |
| [FolderFontSource](folderfontsource/#constructor_1)(string, bool, int) | Ctor. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [FolderPath](../../aspose.words.fonts/folderfontsource/folderpath/) { get; } | Sökväg till mappen. |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | Returnerar teckensnittskällans prioritet. |
| [ScanSubfolders](../../aspose.words.fonts/folderfontsource/scansubfolders/) { get; } | Bestämmer om undermapparna ska skannas eller inte. |
| override [Type](../../aspose.words.fonts/folderfontsource/type/) { get; } | Returnerar typen av teckensnittskälla. |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | Anropas under bearbetning av teckensnittskällan när ett problem upptäcks som kan resultera i förlust av formatering. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | Returnerar en lista över teckensnitt som är tillgängliga via den här källan. |

### Exempel

Visar hur man använder en lokal systemmapp som innehåller teckensnitt som teckensnittskälla.

```csharp
// Skapa en teckensnittskälla från en mapp som innehåller teckensnittsfiler.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false, 1);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

Assert.AreEqual(FontsDir, folderFontSource.FolderPath);
Assert.AreEqual(false, folderFontSource.ScanSubfolders);
Assert.AreEqual(FontSourceType.FontsFolder, folderFontSource.Type);
Assert.AreEqual(1, folderFontSource.Priority);
```

### Se även

* class [FontSourceBase](../fontsourcebase/)
* namnutrymme [Aspose.Words.Fonts](../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../)


