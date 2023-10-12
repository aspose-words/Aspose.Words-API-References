---
title: StreamFontSource.OpenFontDataStream
second_title: Referencia de API de Aspose.Words para .NET
description: StreamFontSource método. Este método debería abrir la secuencia con datos de fuente a pedido.
type: docs
weight: 30
url: /es/net/aspose.words.fonts/streamfontsource/openfontdatastream/
---
## StreamFontSource.OpenFontDataStream method

Este método debería abrir la secuencia con datos de fuente a pedido.

```csharp
public abstract Stream OpenFontDataStream()
```

### Valor_devuelto

Flujo de datos de fuentes.

### Observaciones

La transmisión se cerrará después de la lectura. No es necesario cerrarlo explícitamente.

### Ejemplos

Muestra cómo cargar fuentes desde la secuencia.

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
/// Carga los datos de la fuente solo cuando sea necesario en lugar de almacenarlos en la memoria
/// durante toda la vida útil del objeto "FontSettings".
/// </summary>
private class StreamFontSourceFile : StreamFontSource
{
    public override Stream OpenFontDataStream()
    {
        return File.OpenRead(FontsDir + "Kreon-Regular.ttf");
    }
}
```

### Ver también

* class [StreamFontSource](../)
* espacio de nombres [Aspose.Words.Fonts](../../streamfontsource/)
* asamblea [Aspose.Words](../../../)


