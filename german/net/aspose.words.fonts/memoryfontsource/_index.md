---
title: Class MemoryFontSource
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Fonts.MemoryFontSource klas. Stellt die einzelne im Speicher gespeicherte TrueTypeSchriftartdatei dar.
type: docs
weight: 3020
url: /de/net/aspose.words.fonts/memoryfontsource/
---
## MemoryFontSource class

Stellt die einzelne im Speicher gespeicherte TrueType-Schriftartdatei dar.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Schriftarten](https://docs.aspose.com/words/net/working-with-fonts/) Dokumentationsartikel.

```csharp
public class MemoryFontSource : FontSourceBase
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [MemoryFontSource](memoryfontsource/#constructor)(byte[]) | Ctor. |
| [MemoryFontSource](memoryfontsource/#constructor_1)(byte[], int) | Ctor. |
| [MemoryFontSource](memoryfontsource/#constructor_2)(byte[], int, string) | Ctor. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [CacheKey](../../aspose.words.fonts/memoryfontsource/cachekey/) { get; } | Der Schlüssel dieser Quelle im Cache. |
| [FontData](../../aspose.words.fonts/memoryfontsource/fontdata/) { get; } | Binäre Schriftartdaten. |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | Gibt die Priorität der Schriftartquelle zurück. |
| override [Type](../../aspose.words.fonts/memoryfontsource/type/) { get; } | Gibt den Typ der Schriftartquelle zurück. |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | Wird während der Verarbeitung der Schriftartquelle aufgerufen, wenn ein Problem erkannt wird, das zu einem Verlust der Formatierungstreue führen könnte. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | Gibt eine Liste der über diese Quelle verfügbaren Schriftarten zurück. |

### Beispiele

Zeigt, wie ein Byte-Array mit Daten aus einer Schriftartdatei als Schriftartquelle verwendet wird.

```csharp
byte[] fontBytes = File.ReadAllBytes(MyDir + "Alte DIN 1451 Mittelschrift.ttf");
MemoryFontSource memoryFontSource = new MemoryFontSource(fontBytes, 0);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {memoryFontSource});

Assert.AreEqual(FontSourceType.MemoryFont, memoryFontSource.Type);
Assert.AreEqual(0, memoryFontSource.Priority);
```

### Siehe auch

* class [FontSourceBase](../fontsourcebase/)
* namensraum [Aspose.Words.Fonts](../../aspose.words.fonts/)
* Montage [Aspose.Words](../../)


