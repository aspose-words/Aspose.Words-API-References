---
title: FileFontSource.FilePath
linktitle: FilePath
articleTitle: FilePath
second_title: Aspose.Words för .NET
description: FileFontSource FilePath fast egendom. Sökväg till teckensnittsfilen i C#.
type: docs
weight: 30
url: /sv/net/aspose.words.fonts/filefontsource/filepath/
---
## FileFontSource.FilePath property

Sökväg till teckensnittsfilen.

```csharp
public string FilePath { get; }
```

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

* class [FileFontSource](../)
* namnutrymme [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../../)
