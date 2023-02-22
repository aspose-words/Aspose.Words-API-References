---
title: Class StreamFontSource
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Fonts.StreamFontSource klas. Basisklasse für benutzerdefinierte StreamSchriftquelle.
type: docs
weight: 2860
url: /de/net/aspose.words.fonts/streamfontsource/
---
## StreamFontSource class

Basisklasse für benutzerdefinierte Stream-Schriftquelle.

```csharp
public abstract class StreamFontSource : FontSourceBase
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [CacheKey](../../aspose.words.fonts/streamfontsource/cachekey/) { get; } | Der Schlüssel dieser Quelle im Cache. |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | Gibt die Priorität der Schriftquelle zurück. |
| [Type](../../aspose.words.fonts/streamfontsource/type/) { get; } | Gibt den Typ der Schriftartquelle zurück. |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | Wird während der Verarbeitung der Schriftartquelle aufgerufen, wenn ein Problem erkannt wird, das zu einem Verlust der Formatierungstreue führen kann. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | Gibt eine Liste der Schriftarten zurück, die über diese Quelle verfügbar sind. |
| abstract [OpenFontDataStream](../../aspose.words.fonts/streamfontsource/openfontdatastream/)() | Diese Methode sollte den Stream mit Schriftdaten bei Bedarf öffnen. |

### Bemerkungen

Um die Stream-Font-Quelle zu verwenden, sollten Sie eine abgeleitete Klasse aus der erstellen`StreamFontSource` und Bereitstellung der Implementierung der[`OpenFontDataStream`](./openfontdatastream/) Methode.

[`OpenFontDataStream`](./openfontdatastream/)Methode konnte mehrmals aufgerufen werden. Zum ersten Mal wird es genannt, wenn Aspose.Words die bereitgestellten Schriftartquellen durchsucht, um die Liste der verfügbaren Schriftarten zu erhalten. Später kann es aufgerufen werden, wenn der Font im Dokument verwendet wird, um die Fontdaten zu parsen und die Fontdaten in einige Ausgabeformate einzubetten.

`StreamFontSource` kann nützlich sein, da es erlaubt, die Schriftdaten nur dann zu laden, wenn sie benötigt werden und sie nicht im Speicher für die zu speichern[`FontSettings`](../fontsettings/) Lebensdauer.

### Beispiele

Zeigt, wie Schriftarten aus dem Stream geladen werden.

```csharp
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
/// für die gesamte Lebensdauer des "FontSettings"-Objekts.
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

* class [FontSourceBase](../fontsourcebase/)
* namensraum [Aspose.Words.Fonts](../../aspose.words.fonts/)
* Montage [Aspose.Words](../../)


