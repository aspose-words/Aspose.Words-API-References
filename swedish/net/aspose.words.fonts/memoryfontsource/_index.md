---
title: MemoryFontSource Class
linktitle: MemoryFontSource
articleTitle: MemoryFontSource
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Fonts.MemoryFontSource, som möjliggör sömlös åtkomst till TrueType-teckensnitt som lagras i minnet för förbättrad dokumentbehandling.
type: docs
weight: 3450
url: /sv/net/aspose.words.fonts/memoryfontsource/
---
## MemoryFontSource class

Representerar den enda TrueType-teckensnittsfilen som lagras i minnet.

För att lära dig mer, besök[Arbeta med teckensnitt](https://docs.aspose.com/words/net/working-with-fonts/) dokumentationsartikel.

```csharp
public class MemoryFontSource : FontSourceBase
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [MemoryFontSource](memoryfontsource/#constructor)(*byte[]*) | ktor. |
| [MemoryFontSource](memoryfontsource/#constructor_1)(*byte[], int*) | ktor. |
| [MemoryFontSource](memoryfontsource/#constructor_2)(*byte[], int, string*) | ktor. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [CacheKey](../../aspose.words.fonts/memoryfontsource/cachekey/) { get; } | Nyckeln till denna källa i cachen. |
| [FontData](../../aspose.words.fonts/memoryfontsource/fontdata/) { get; } | Binära teckensnittsdata. |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | Returnerar teckensnittets källprioritet. |
| override [Type](../../aspose.words.fonts/memoryfontsource/type/) { get; } | Returnerar typen av teckensnittskällan. |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | Anropas under bearbetning av teckensnittskälla när ett problem upptäcks som kan leda till förlust av formateringstillverkning. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | Returnerar en lista över teckensnitt som är tillgängliga via denna källa. |

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
