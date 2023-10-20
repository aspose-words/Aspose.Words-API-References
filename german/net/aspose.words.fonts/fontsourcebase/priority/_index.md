---
title: FontSourceBase.Priority
linktitle: Priority
articleTitle: Priority
second_title: Aspose.Words für .NET
description: FontSourceBase Priority eigendom. Gibt die Priorität der Schriftartquelle zurück in C#.
type: docs
weight: 10
url: /de/net/aspose.words.fonts/fontsourcebase/priority/
---
## FontSourceBase.Priority property

Gibt die Priorität der Schriftartquelle zurück.

```csharp
public int Priority { get; }
```

## Bemerkungen

Dieser Wert wird verwendet, wenn Schriftarten mit demselben Familiennamen und Stil in verschiedenen Schriftartquellen vorhanden sind. In diesem Fall wählt Aspose.Words die Schriftart aus der Quelle mit dem höheren Prioritätswert aus.

Der Standardwert ist 0.

## Beispiele

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

* class [FontSourceBase](../)
* namensraum [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Montage [Aspose.Words](../../../)
