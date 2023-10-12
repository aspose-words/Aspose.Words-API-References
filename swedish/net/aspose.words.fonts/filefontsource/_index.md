---
title: Class FileFontSource
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Fonts.FileFontSource klass. Representerar den enda TrueTypeteckensnittsfilen som är lagrad i filsystemet.
type: docs
weight: 2870
url: /sv/net/aspose.words.fonts/filefontsource/
---
## FileFontSource class

Representerar den enda TrueType-teckensnittsfilen som är lagrad i filsystemet.

För att lära dig mer, besök[Arbeta med teckensnitt](https://docs.aspose.com/words/net/working-with-fonts/) dokumentationsartikel.

```csharp
public class FileFontSource : FontSourceBase
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [FileFontSource](filefontsource/#constructor)(string) | Ctor. |
| [FileFontSource](filefontsource/#constructor_1)(string, int) | Ctor. |
| [FileFontSource](filefontsource/#constructor_2)(string, int, string) | Ctor. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [CacheKey](../../aspose.words.fonts/filefontsource/cachekey/) { get; } | Nyckeln till denna källa i cachen. |
| [FilePath](../../aspose.words.fonts/filefontsource/filepath/) { get; } | Sökväg till teckensnittsfilen. |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | Returnerar teckensnittskällans prioritet. |
| override [Type](../../aspose.words.fonts/filefontsource/type/) { get; } | Returnerar typen av teckensnittskälla. |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | Anropas under bearbetning av teckensnittskällan när ett problem upptäcks som kan resultera i förlust av formatering. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | Returnerar en lista över teckensnitt som är tillgängliga via den här källan. |

### Exempel

Visar hur man använder en teckensnittsfil i det lokala filsystemet som en teckensnittskälla.

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


