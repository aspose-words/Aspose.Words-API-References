---
title: StreamFontSource.OpenFontDataStream
linktitle: OpenFontDataStream
articleTitle: OpenFontDataStream
second_title: Aspose.Words per .NET
description: Scopri il metodo StreamFontSource OpenFontDataStream per accedere in modo efficiente ai flussi di dati dei font su richiesta, migliorando il flusso di lavoro di progettazione.
type: docs
weight: 30
url: /it/net/aspose.words.fonts/streamfontsource/openfontdatastream/
---
## StreamFontSource.OpenFontDataStream method

Questo metodo dovrebbe aprire il flusso con i dati del font su richiesta.

```csharp
public abstract Stream OpenFontDataStream()
```

### Valore di ritorno

Flusso di dati dei font.

## Osservazioni

Il flusso verrà chiuso dopo la lettura. Non è necessario chiuderlo esplicitamente.

## Esempi

Mostra come caricare i font dallo stream.

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
/// Carica i dati del font solo quando necessario invece di memorizzarli nella memoria
/// per l'intera durata dell'oggetto "FontSettings".
/// </summary>
private class StreamFontSourceFile : StreamFontSource
{
    public override Stream OpenFontDataStream()
    {
        return File.OpenRead(FontsDir + "Kreon-Regular.ttf");
    }
}
```

### Guarda anche

* class [StreamFontSource](../)
* spazio dei nomi [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../../)
