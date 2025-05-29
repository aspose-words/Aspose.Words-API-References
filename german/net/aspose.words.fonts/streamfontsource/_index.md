---
title: StreamFontSource Class
linktitle: StreamFontSource
articleTitle: StreamFontSource
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Fonts.StreamFontSource, Ihre Lösung für benutzerdefinierte Stream-Font-Quellen, die die Flexibilität und das Design von Dokumenten verbessern.
type: docs
weight: 3470
url: /de/net/aspose.words.fonts/streamfontsource/
---
## StreamFontSource class

Basisklasse für benutzerdefinierte Stream-Font-Quelle.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Schriftarten](https://docs.aspose.com/words/net/working-with-fonts/) Dokumentationsartikel.

```csharp
public abstract class StreamFontSource : FontSourceBase,   
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [CacheKey](../../aspose.words.fonts/streamfontsource/cachekey/) { get; } | Der Schlüssel dieser Quelle im Cache. |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | Gibt die Priorität der Schriftartquelle zurück. |
| [Type](../../aspose.words.fonts/streamfontsource/type/) { get; } | Gibt den Typ der Schriftartquelle zurück. |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | Wird während der Verarbeitung der Schriftartquelle aufgerufen, wenn ein Problem erkannt wird, das zu einem Verlust der Formatierungstreue führen kann. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | Gibt eine Liste der über diese Quelle verfügbaren Schriftarten zurück. |
| abstract [OpenFontDataStream](../../aspose.words.fonts/streamfontsource/openfontdatastream/)() | Diese Methode sollte den Stream bei Bedarf mit Schriftdaten öffnen. |

## Bemerkungen

Um die Stream-Font-Quelle zu verwenden, sollten Sie eine abgeleitete Klasse aus der`StreamFontSource` und bieten die Implementierung der[`OpenFontDataStream`](./openfontdatastream/) Verfahren.

[`OpenFontDataStream`](./openfontdatastream/)Die Methode kann mehrmals aufgerufen werden. Das erste Mal wird sie aufgerufen , wenn Aspose.Words die bereitgestellten Schriftquellen durchsucht, um die Liste der verfügbaren Schriftarten abzurufen. Später kann sie aufgerufen werden, wenn die Schriftart im Dokument verwendet wird, um die Schriftdaten zu analysieren und in einige Ausgabeformate einzubetten.

`StreamFontSource` kann nützlich sein, da es ermöglicht, die Schriftdaten nur dann zu laden, wenn sie benötigt werden und sie nicht für die[`FontSettings`](../fontsettings/) Lebensdauer.

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

* class [FontSourceBase](../fontsourcebase/)
* interface [  ](../../global/%02  /)
* namensraum [Aspose.Words.Fonts](../../aspose.words.fonts/)
* Montage [Aspose.Words](../../)
