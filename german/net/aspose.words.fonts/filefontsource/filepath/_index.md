---
title: FileFontSource.FilePath
linktitle: FilePath
articleTitle: FilePath
second_title: Aspose.Words für .NET
description: Entdecken Sie die FileFontSource FilePath-Eigenschaft für einfachen Zugriff auf Ihre Schriftdateien. Optimieren Sie Ihren Designprozess mit diesem unverzichtbaren Tool!
type: docs
weight: 30
url: /de/net/aspose.words.fonts/filefontsource/filepath/
---
## FileFontSource.FilePath property

Pfad zur Schriftartdatei.

```csharp
public string FilePath { get; }
```

## Beispiele

Zeigt, wie eine Schriftartdatei im lokalen Dateisystem als Schriftartquelle verwendet wird.

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
* namensraum [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Montage [Aspose.Words](../../../)
