---
title: StreamFontSource Class
linktitle: StreamFontSource
articleTitle: StreamFontSource
second_title: Aspose.Words für .NET
description: Aspose.Words.Fonts.StreamFontSource klas. Basisklasse für benutzerdefinierte StreamSchriftartquelle in C#.
type: docs
weight: 3040
url: /de/net/aspose.words.fonts/streamfontsource/
---
## StreamFontSource class

Basisklasse für benutzerdefinierte Stream-Schriftartquelle.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Schriftarten](https://docs.aspose.com/words/net/working-with-fonts/) Dokumentationsartikel.

```csharp
public abstract class StreamFontSource : FontSourceBase
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [CacheKey](../../aspose.words.fonts/streamfontsource/cachekey/) { get; } | Der Schlüssel dieser Quelle im Cache. |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | Gibt die Priorität der Schriftartquelle zurück. |
| [Type](../../aspose.words.fonts/streamfontsource/type/) { get; } | Gibt den Typ der Schriftartquelle zurück. |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | Wird während der Verarbeitung der Schriftartquelle aufgerufen, wenn ein Problem erkannt wird, das zu einem Verlust der Formatierungstreue führen könnte. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | Gibt eine Liste der über diese Quelle verfügbaren Schriftarten zurück. |
| abstract [OpenFontDataStream](../../aspose.words.fonts/streamfontsource/openfontdatastream/)() | Diese Methode sollte den Stream bei Bedarf mit Schriftartdaten öffnen. |

## Bemerkungen

Um die Stream-Schriftartquelle verwenden zu können, sollten Sie eine abgeleitete Klasse daraus erstellen`StreamFontSource` und stellen die Implementierung bereit[`OpenFontDataStream`](./openfontdatastream/) Methode.

[`OpenFontDataStream`](./openfontdatastream/)Methode könnte mehrmals aufgerufen werden. Zum ersten Mal heißt es , wenn Aspose.Words die bereitgestellten Schriftartquellen durchsucht, um die Liste der verfügbaren Schriftarten zu erhalten. Später kann es aufgerufen werden, wenn die Schriftart im Dokument verwendet wird, um die Schriftartdaten zu analysieren und die Schriftartdaten in einige Ausgabeformate einzubetten.

`StreamFontSource` kann nützlich sein, da es ermöglicht, die Schriftdaten nur dann zu laden, wenn sie benötigt werden und sie nicht im Speicher für den zu speichern[`FontSettings`](../fontsettings/) Lebensdauer.

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

* class [FontSourceBase](../fontsourcebase/)
* namensraum [Aspose.Words.Fonts](../../aspose.words.fonts/)
* Montage [Aspose.Words](../../)
