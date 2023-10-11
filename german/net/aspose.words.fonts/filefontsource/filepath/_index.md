---
title: FileFontSource.FilePath
second_title: Aspose.Words für .NET-API-Referenz
description: FileFontSource eigendom. Pfad zur Schriftartdatei.
type: docs
weight: 30
url: /de/net/aspose.words.fonts/filefontsource/filepath/
---
## FileFontSource.FilePath property

Pfad zur Schriftartdatei.

```csharp
public string FilePath { get; }
```

### Beispiele

Zeigt, wie eine Schriftartendatei im lokalen Dateisystem als Schriftartenquelle verwendet wird.

```csharp
FileFontSource fileFontSource = new FileFontSource(MyDir + "Alte DIN 1451 Mittelschrift.ttf", 0);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {fileFontSource});

Assert.AreEqual(MyDir + "Alte DIN 1451 Mittelschrift.ttf", fileFontSource.FilePath);
Assert.AreEqual(FontSourceType.FontFile, fileFontSource.Type);
Assert.AreEqual(0, fileFontSource.Priority);
```

### Siehe auch

* class [FileFontSource](../)
* namensraum [Aspose.Words.Fonts](../../filefontsource/)
* Montage [Aspose.Words](../../../)


