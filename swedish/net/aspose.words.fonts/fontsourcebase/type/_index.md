---
title: FontSourceBase.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words för .NET
description: FontSourceBase Type fast egendom. Returnerar typen av teckensnittskälla i C#.
type: docs
weight: 20
url: /sv/net/aspose.words.fonts/fontsourcebase/type/
---
## FontSourceBase.Type property

Returnerar typen av teckensnittskälla.

```csharp
public abstract FontSourceType Type { get; }
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

* enum [FontSourceType](../../fontsourcetype/)
* class [FontSourceBase](../)
* namnutrymme [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../../)
