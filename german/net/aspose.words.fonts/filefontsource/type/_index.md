---
title: FileFontSource.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words für .NET
description: Entdecken Sie die FileFontSource-Type-Eigenschaft, um Schriftartquellentypen einfach zu identifizieren und Ihre Designprojekte mit präzisen Typografielösungen zu verbessern.
type: docs
weight: 40
url: /de/net/aspose.words.fonts/filefontsource/type/
---
## FileFontSource.Type property

Gibt den Typ der Schriftartquelle zurück.

```csharp
public override FontSourceType Type { get; }
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

* enum [FontSourceType](../../fontsourcetype/)
* class [FileFontSource](../)
* namensraum [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Montage [Aspose.Words](../../../)
