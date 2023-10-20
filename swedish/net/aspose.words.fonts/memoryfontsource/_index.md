---
title: MemoryFontSource Class
linktitle: MemoryFontSource
articleTitle: MemoryFontSource
second_title: Aspose.Words för .NET
description: Aspose.Words.Fonts.MemoryFontSource klass. Representerar den enda TrueTypeteckensnittsfilen som är lagrad i minnet i C#.
type: docs
weight: 3020
url: /sv/net/aspose.words.fonts/memoryfontsource/
---
## MemoryFontSource class

Representerar den enda TrueType-teckensnittsfilen som är lagrad i minnet.

För att lära dig mer, besök[Arbeta med teckensnitt](https://docs.aspose.com/words/net/working-with-fonts/) dokumentationsartikel.

```csharp
public class MemoryFontSource : FontSourceBase
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [MemoryFontSource](memoryfontsource/#constructor)(*byte[]*) | Ctor. |
| [MemoryFontSource](memoryfontsource/#constructor_1)(*byte[], int*) | Ctor. |
| [MemoryFontSource](memoryfontsource/#constructor_2)(*byte[], int, string*) | Ctor. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [CacheKey](../../aspose.words.fonts/memoryfontsource/cachekey/) { get; } | Nyckeln till denna källa i cachen. |
| [FontData](../../aspose.words.fonts/memoryfontsource/fontdata/) { get; } | Binära teckensnittsdata. |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | Returnerar teckensnittskällans prioritet. |
| override [Type](../../aspose.words.fonts/memoryfontsource/type/) { get; } | Returnerar typen av teckensnittskälla. |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | Anropas under bearbetning av teckensnittskällan när ett problem upptäcks som kan resultera i förlust av formatering. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | Returnerar en lista över teckensnitt som är tillgängliga via den här källan. |

## Exempel

Visar hur man använder en byte-array med data från en teckensnittsfil som teckensnittskälla.

```csharp
byte[] fontBytes = File.ReadAllBytes(MyDir + "Alte DIN 1451 Mittelschrift.ttf");
MemoryFontSource memoryFontSource = new MemoryFontSource(fontBytes, 0);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {memoryFontSource});

Assert.AreEqual(FontSourceType.MemoryFont, memoryFontSource.Type);
Assert.AreEqual(0, memoryFontSource.Priority);
```

### Se även

* class [FontSourceBase](../fontsourcebase/)
* namnutrymme [Aspose.Words.Fonts](../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../)
