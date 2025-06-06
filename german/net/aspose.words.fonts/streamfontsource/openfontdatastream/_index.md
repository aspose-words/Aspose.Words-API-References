---
title: StreamFontSource.OpenFontDataStream
linktitle: OpenFontDataStream
articleTitle: OpenFontDataStream
second_title: Aspose.Words für .NET
description: Entdecken Sie die StreamFontSource OpenFontDataStream-Methode für den effizienten Zugriff auf Schriftartdatenströme bei Bedarf und verbessern Sie so Ihren Design-Workflow.
type: docs
weight: 30
url: /de/net/aspose.words.fonts/streamfontsource/openfontdatastream/
---
## StreamFontSource.OpenFontDataStream method

Diese Methode sollte den Stream bei Bedarf mit Schriftdaten öffnen.

```csharp
public abstract Stream OpenFontDataStream()
```

### Rückgabewert

Schriftartdatenstrom.

## Bemerkungen

Der Stream wird nach dem Lesen geschlossen. Ein explizites Schließen ist nicht erforderlich.

## Beispiele

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
/// Laden Sie die Schriftdaten nur bei Bedarf, anstatt sie im Speicher zu speichern
/// für die gesamte Lebensdauer des Objekts „FontSettings“.
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
* namensraum [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Montage [Aspose.Words](../../../)
