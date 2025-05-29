---
title: FontSourceBase Class
linktitle: FontSourceBase
articleTitle: FontSourceBase
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Fonts.FontSourceBase, den viktiga abstrakta klassen för att definiera olika teckensnittskällor i dina applikationer. Förbättra din dokumentformatering!
type: docs
weight: 3410
url: /sv/net/aspose.words.fonts/fontsourcebase/
---
## FontSourceBase class

Detta är en abstrakt basklass för de klasser som låter användaren ange olika teckensnittskällor.

För att lära dig mer, besök[Arbeta med teckensnitt](https://docs.aspose.com/words/net/working-with-fonts/) dokumentationsartikel.

```csharp
public abstract class FontSourceBase
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | Returnerar teckensnittets källprioritet. |
| abstract [Type](../../aspose.words.fonts/fontsourcebase/type/) { get; } | Returnerar typen av teckensnittskällan. |
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

* namnutrymme [Aspose.Words.Fonts](../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../)
