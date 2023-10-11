---
title: StreamFontSource.OpenFontDataStream
second_title: Aspose.Words per .NET API Reference
description: StreamFontSource metodo. Questo metodo dovrebbe aprire lo stream con i dati dei caratteri su richiesta.
type: docs
weight: 30
url: /it/net/aspose.words.fonts/streamfontsource/openfontdatastream/
---
## StreamFontSource.OpenFontDataStream method

Questo metodo dovrebbe aprire lo stream con i dati dei caratteri su richiesta.

```csharp
public abstract Stream OpenFontDataStream()
```

### Valore di ritorno

Flusso di dati dei caratteri.

### Osservazioni

Lo stream verrà chiuso dopo la lettura. Non è necessario chiuderlo esplicitamente.

### Esempi

Mostra come caricare i caratteri dallo stream.

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
/// Carica i dati dei caratteri solo quando richiesto invece di archiviarli nella memoria
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
* spazio dei nomi [Aspose.Words.Fonts](../../streamfontsource/)
* assemblea [Aspose.Words](../../../)


