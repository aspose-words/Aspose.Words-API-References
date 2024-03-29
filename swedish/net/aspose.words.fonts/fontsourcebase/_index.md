---
title: FontSourceBase Class
linktitle: FontSourceBase
articleTitle: FontSourceBase
second_title: Aspose.Words för .NET
description: Aspose.Words.Fonts.FontSourceBase klass. Detta är en abstrakt basklass för klasserna som låter användaren specificera olika teckensnittskällor i C#.
type: docs
weight: 2980
url: /sv/net/aspose.words.fonts/fontsourcebase/
---
## FontSourceBase class

Detta är en abstrakt basklass för klasserna som låter användaren specificera olika teckensnittskällor.

För att lära dig mer, besök[Arbeta med teckensnitt](https://docs.aspose.com/words/net/working-with-fonts/) dokumentationsartikel.

```csharp
public abstract class FontSourceBase
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | Returnerar teckensnittskällans prioritet. |
| abstract [Type](../../aspose.words.fonts/fontsourcebase/type/) { get; } | Returnerar typen av teckensnittskälla. |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | Anropas under bearbetning av teckensnittskällan när ett problem upptäcks som kan resultera i förlust av formatering. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | Returnerar en lista över teckensnitt som är tillgängliga via den här källan. |

## Exempel

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

* namnutrymme [Aspose.Words.Fonts](../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../)
