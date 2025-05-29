---
title: FolderFontSource Class
linktitle: FolderFontSource
articleTitle: FolderFontSource
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Fonts.FolderFontSource, din lösning för att hantera TrueType-teckensnitt effektivt. Förbättra ditt dokuments typografi idag!
type: docs
weight: 3290
url: /sv/net/aspose.words.fonts/folderfontsource/
---
## FolderFontSource class

Representerar mappen som innehåller TrueType-teckensnittsfiler.

För att lära dig mer, besök[Arbeta med teckensnitt](https://docs.aspose.com/words/net/working-with-fonts/) dokumentationsartikel.

```csharp
public class FolderFontSource : FontSourceBase
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [FolderFontSource](folderfontsource/#constructor)(*string, bool*) | ktor. |
| [FolderFontSource](folderfontsource/#constructor_1)(*string, bool, int*) | ktor. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [FolderPath](../../aspose.words.fonts/folderfontsource/folderpath/) { get; } | Sökväg till mappen. |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | Returnerar teckensnittets källprioritet. |
| [ScanSubfolders](../../aspose.words.fonts/folderfontsource/scansubfolders/) { get; } | Avgör om undermapparna ska genomsökas eller inte. |
| override [Type](../../aspose.words.fonts/folderfontsource/type/) { get; } | Returnerar typen av teckensnittskällan. |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | Anropas under bearbetning av teckensnittskälla när ett problem upptäcks som kan leda till förlust av formateringstillverkning. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | Returnerar en lista över teckensnitt som är tillgängliga via denna källa. |

## Exempel

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
