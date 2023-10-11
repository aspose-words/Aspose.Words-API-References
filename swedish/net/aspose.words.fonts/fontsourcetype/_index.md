---
title: Enum FontSourceType
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Fonts.FontSourceType uppräkning. Anger typen av en teckensnittskälla.
type: docs
weight: 2990
url: /sv/net/aspose.words.fonts/fontsourcetype/
---
## FontSourceType enumeration

Anger typen av en teckensnittskälla.

```csharp
public enum FontSourceType
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| FontFile | `0` | A[`FileFontSource`](../filefontsource/) objekt som representerar en fil med ett teckensnitt. |
| FontsFolder | `1` | A[`FolderFontSource`](../folderfontsource/) objekt som representerar mapp med teckensnittsfiler. |
| MemoryFont | `2` | A[`MemoryFontSource`](../memoryfontsource/) objekt som representerar enstaka teckensnitt i minnet. |
| SystemFonts | `3` | A[`SystemFontSource`](../systemfontsource/) objekt som representerar alla teckensnitt som är installerade i systemet. |
| FontStream | `4` | A[`StreamFontSource`](../streamfontsource/) objekt som representerar en ström med teckensnittsdata. |

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

* namnutrymme [Aspose.Words.Fonts](../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../)


