---
title: StreamFontSource Class
linktitle: StreamFontSource
articleTitle: StreamFontSource
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Fonts.StreamFontSource, su solución ideal para fuentes de flujo personalizadas que mejoran la flexibilidad y el diseño de los documentos.
type: docs
weight: 3470
url: /es/net/aspose.words.fonts/streamfontsource/
---
## StreamFontSource class

Clase base para la fuente de flujo definida por el usuario.

Para obtener más información, visite el[Trabajar con fuentes](https://docs.aspose.com/words/net/working-with-fonts/) Artículo de documentación.

```csharp
public abstract class StreamFontSource : FontSourceBase,   
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [CacheKey](../../aspose.words.fonts/streamfontsource/cachekey/) { get; } | La clave de esta fuente en la caché. |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | Devuelve la prioridad de la fuente. |
| [Type](../../aspose.words.fonts/streamfontsource/type/) { get; } | Devuelve el tipo de la fuente de origen. |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | Se llama durante el procesamiento de la fuente de origen cuando se detecta un problema que podría provocar la pérdida de fidelidad del formato. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | Devuelve la lista de fuentes disponibles a través de esta fuente. |
| abstract [OpenFontDataStream](../../aspose.words.fonts/streamfontsource/openfontdatastream/)() | Este método debería abrir la secuencia con datos de fuente a pedido. |

## Observaciones

Para poder utilizar la fuente de flujo, debe crear una clase derivada de la`StreamFontSource` y proporcionar la implementación de la[`OpenFontDataStream`](./openfontdatastream/) método.

[`OpenFontDataStream`](./openfontdatastream/)El método podría llamarse varias veces. La primera vez, se llamará cuando Aspose.Words analice las fuentes proporcionadas para obtener la lista de fuentes disponibles. Posteriormente, podría llamarse si se utiliza la fuente en el documento para analizar los datos de la fuente e incrustarlos en algunos formatos de salida.

`StreamFontSource` Puede ser útil porque permite cargar los datos de fuente solo cuando es requerido y no almacenarlos en la memoria para el resto.[`FontSettings`](../fontsettings/) vida.

## Ejemplos

Muestra cómo cargar fuentes desde la transmisión.

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
* interface [  ](../../global/%02  /)
* espacio de nombres [Aspose.Words.Fonts](../../aspose.words.fonts/)
* asamblea [Aspose.Words](../../)
