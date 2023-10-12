---
title: StreamFontSource.OpenFontDataStream
second_title: Aspose.Words für .NET-API-Referenz
description: StreamFontSource methode. Diese Methode sollte den Stream bei Bedarf mit Schriftartdaten öffnen.
type: docs
weight: 30
url: /de/net/aspose.words.fonts/streamfontsource/openfontdatastream/
---
## StreamFontSource.OpenFontDataStream method

Diese Methode sollte den Stream bei Bedarf mit Schriftartdaten öffnen.

```csharp
public abstract Stream OpenFontDataStream()
```

### Rückgabewert

Schriftartdatenstrom.

### Bemerkungen

Der Stream wird nach dem Lesen geschlossen. Es ist nicht erforderlich, es explizit zu schließen.

### Beispiele

Zeigt, wie Schriftarten aus dem Stream geladen werden.

```csharp
public void StreamFontSourceFileRendering()
{
    FontSettings fontSettings = new FontSettings();
    fontSettings.SetFontsSources(new FontSourceBase[] {new StreamFontSourceFile()});

    DocumentBuilder builder = new DocumentBuilder();
    builder.Document.FontSettings = fontSettings;
    builder.Font.Name = "Kreon-Regular";
    builder.Writeln("Test aspose text when saving to PDF.");

    builder.Document.Save(ArtifactsDir + "FontSettings.StreamFontSourceFileRendering.pdf");
}

/// <summary>
/// Laden Sie die Schriftartdaten nur bei Bedarf, anstatt sie im Speicher zu speichern
/// für die gesamte Lebensdauer des „FontSettings“-Objekts.
/// </summary>
private class StreamFontSourceFile : StreamFontSource
{
    public override Stream OpenFontDataStream()
    {
        return File.OpenRead(FontsDir + "Kreon-Regular.ttf");
    }
}
```

### Siehe auch

* class [StreamFontSource](../)
* namensraum [Aspose.Words.Fonts](../../streamfontsource/)
* Montage [Aspose.Words](../../../)


