---
title: FontSourceBase.Priority
linktitle: Priority
articleTitle: Priority
second_title: Aspose.Words för .NET
description: FontSourceBase Priority fast egendom. Returnerar teckensnittskällans prioritet i C#.
type: docs
weight: 10
url: /sv/net/aspose.words.fonts/fontsourcebase/priority/
---
## FontSourceBase.Priority property

Returnerar teckensnittskällans prioritet.

```csharp
public int Priority { get; }
```

## Anmärkningar

Detta värde används när det finns typsnitt med samma efternamn och stil i olika teckensnittskällor. I det här fallet väljer Aspose.Words typsnittet från källan med det högre prioritetsvärdet.

Standardvärdet är 0.

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

* class [FontSourceBase](../)
* namnutrymme [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../../)
