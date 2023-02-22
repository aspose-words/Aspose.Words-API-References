---
title: Class StreamFontSource
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Fonts.StreamFontSource clase. Clase base para fuente de fuente de transmisión definida por el usuario.
type: docs
weight: 2860
url: /es/net/aspose.words.fonts/streamfontsource/
---
## StreamFontSource class

Clase base para fuente de fuente de transmisión definida por el usuario.

```csharp
public abstract class StreamFontSource : FontSourceBase
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [CacheKey](../../aspose.words.fonts/streamfontsource/cachekey/) { get; } | La clave de esta fuente en el caché. |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | Devuelve la prioridad de origen de la fuente. |
| [Type](../../aspose.words.fonts/streamfontsource/type/) { get; } | Devuelve el tipo de fuente fuente. |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | Llamado durante el procesamiento del origen de la fuente cuando se detecta un problema que podría resultar en la pérdida de fidelidad del formato. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | Devuelve la lista de fuentes disponibles a través de esta fuente. |
| abstract [OpenFontDataStream](../../aspose.words.fonts/streamfontsource/openfontdatastream/)() | Este método debería abrir la secuencia con datos de fuentes a pedido. |

### Observaciones

Para usar la fuente de fuente de flujo, debe crear una clase derivada del`StreamFontSource` y proporcionar la implementación del[`OpenFontDataStream`](./openfontdatastream/) método.

[`OpenFontDataStream`](./openfontdatastream/)El método podría llamarse varias veces. Por primera vez, se llamará cuando Aspose.Words analice las fuentes de fuentes proporcionadas para obtener la lista de fuentes disponibles. Posteriormente se puede llamar si la fuente se usa en el documento para analizar los datos de la fuente y para incrustar los datos de la fuente en algunos formatos de salida.

`StreamFontSource` puede ser útil porque permite cargar los datos de la fuente solo cuando se requiere y no almacenarlos en la memoria para el[`FontSettings`](../fontsettings/) toda la vida.

### Ejemplos

Muestra cómo cargar fuentes desde la transmisión.

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
/// Cargue los datos de la fuente solo cuando sea necesario en lugar de almacenarlos en la memoria
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

* class [FontSourceBase](../fontsourcebase/)
* espacio de nombres [Aspose.Words.Fonts](../../aspose.words.fonts/)
* asamblea [Aspose.Words](../../)


