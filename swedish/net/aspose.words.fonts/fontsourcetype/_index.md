---
title: FontSourceType Enum
linktitle: FontSourceType
articleTitle: FontSourceType
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Fonts.FontSourceType-enum för effektiv hantering av teckensnittskällor. Optimera din dokumenthantering med flexibla teckensnittsalternativ.
type: docs
weight: 3420
url: /sv/net/aspose.words.fonts/fontsourcetype/
---
## FontSourceType enumeration

Anger typ av teckensnittskälla.

```csharp
public enum FontSourceType
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| FontFile | `0` | A[`FileFontSource`](../filefontsource/) objekt som representerar en enda teckensnittsfil. |
| FontsFolder | `1` | A[`FolderFontSource`](../folderfontsource/) objekt som representerar mapp med teckensnittsfiler. |
| MemoryFont | `2` | A[`MemoryFontSource`](../memoryfontsource/) objekt som representerar ett enda teckensnitt i minnet. |
| SystemFonts | `3` | A[`SystemFontSource`](../systemfontsource/) objekt som representerar alla teckensnitt som är installerade i systemet. |
| FontStream | `4` | A[`StreamFontSource`](../streamfontsource/) objekt som representerar en ström med teckensnittsdata. |

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
