---
title: FileFontSource Class
linktitle: FileFontSource
articleTitle: FileFontSource
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Fonts.FileFontSource. Hantera enkelt TrueType-teckensnittsfiler på ditt system för förbättrad dokumentformatering och designflexibilitet.
type: docs
weight: 3280
url: /sv/net/aspose.words.fonts/filefontsource/
---
## FileFontSource class

Representerar den enda TrueType-teckensnittsfilen som lagras i filsystemet.

För att lära dig mer, besök[Arbeta med teckensnitt](https://docs.aspose.com/words/net/working-with-fonts/) dokumentationsartikel.

```csharp
public class FileFontSource : FontSourceBase
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [FileFontSource](filefontsource/#constructor)(*string*) | ktor. |
| [FileFontSource](filefontsource/#constructor_1)(*string, int*) | ktor. |
| [FileFontSource](filefontsource/#constructor_2)(*string, int, string*) | ktor. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [CacheKey](../../aspose.words.fonts/filefontsource/cachekey/) { get; } | Nyckeln till denna källa i cachen. |
| [FilePath](../../aspose.words.fonts/filefontsource/filepath/) { get; } | Sökväg till typsnittsfilen. |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | Returnerar teckensnittets källprioritet. |
| override [Type](../../aspose.words.fonts/filefontsource/type/) { get; } | Returnerar typen av teckensnittskällan. |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | Anropas under bearbetning av teckensnittskälla när ett problem upptäcks som kan leda till förlust av formateringstillverkning. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | Returnerar en lista över teckensnitt som är tillgängliga via denna källa. |

## Exempel

Visar hur man använder en teckensnittsfil i det lokala filsystemet som teckensnittskälla.

```csharp
FileFontSource fileFontSource = new FileFontSource(MyDir + "Alte DIN 1451 Mittelschrift.ttf", 0);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {fileFontSource});

Assert.AreEqual(MyDir + "Alte DIN 1451 Mittelschrift.ttf", fileFontSource.FilePath);
Assert.AreEqual(FontSourceType.FontFile, fileFontSource.Type);
Assert.AreEqual(0, fileFontSource.Priority);
```

### Se även

* class [FontSourceBase](../fontsourcebase/)
* namnutrymme [Aspose.Words.Fonts](../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../)
