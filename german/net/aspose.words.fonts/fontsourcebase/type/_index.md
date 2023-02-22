---
title: FontSourceBase.Type
second_title: Aspose.Words für .NET-API-Referenz
description: FontSourceBase eigendom. Gibt den Typ der Schriftartquelle zurück.
type: docs
weight: 20
url: /de/net/aspose.words.fonts/fontsourcebase/type/
---
## FontSourceBase.Type property

Gibt den Typ der Schriftartquelle zurück.

```csharp
public abstract FontSourceType Type { get; }
```

### Beispiele

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

* enum [FontSourceType](../../fontsourcetype/)
* class [FontSourceBase](../)
* namensraum [Aspose.Words.Fonts](../../fontsourcebase/)
* Montage [Aspose.Words](../../../)


