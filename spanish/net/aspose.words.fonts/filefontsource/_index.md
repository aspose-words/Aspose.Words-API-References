---
title: FileFontSource Class
linktitle: FileFontSource
articleTitle: FileFontSource
second_title: Aspose.Words para .NET
description: Aspose.Words.Fonts.FileFontSource clase. Representa el único archivo de fuente TrueType almacenado en el sistema de archivos en C#.
type: docs
weight: 2870
url: /es/net/aspose.words.fonts/filefontsource/
---
## FileFontSource class

Representa el único archivo de fuente TrueType almacenado en el sistema de archivos.

Para obtener más información, visite el[Trabajar con fuentes](https://docs.aspose.com/words/net/working-with-fonts/) artículo de documentación.

```csharp
public class FileFontSource : FontSourceBase
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [FileFontSource](filefontsource/#constructor)(*string*) | Director. |
| [FileFontSource](filefontsource/#constructor_1)(*string, int*) | Director. |
| [FileFontSource](filefontsource/#constructor_2)(*string, int, string*) | Director. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [CacheKey](../../aspose.words.fonts/filefontsource/cachekey/) { get; } | La clave de esta fuente en el caché. |
| [FilePath](../../aspose.words.fonts/filefontsource/filepath/) { get; } | Ruta al archivo de fuente. |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | Devuelve la prioridad de fuente de fuente. |
| override [Type](../../aspose.words.fonts/filefontsource/type/) { get; } | Devuelve el tipo de fuente fuente. |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | Se llama durante el procesamiento del origen de la fuente cuando se detecta un problema que podría provocar una pérdida de fidelidad del formato. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | Devuelve una lista de fuentes disponibles a través de esta fuente. |

## Ejemplos

Muestra cómo utilizar un archivo de fuente en el sistema de archivos local como fuente de fuente.

```csharp
FileFontSource fileFontSource = new FileFontSource(MyDir + "Alte DIN 1451 Mittelschrift.ttf", 0);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {fileFontSource});

Assert.AreEqual(MyDir + "Alte DIN 1451 Mittelschrift.ttf", fileFontSource.FilePath);
Assert.AreEqual(FontSourceType.FontFile, fileFontSource.Type);
Assert.AreEqual(0, fileFontSource.Priority);
```

### Ver también

* class [FontSourceBase](../fontsourcebase/)
* espacio de nombres [Aspose.Words.Fonts](../../aspose.words.fonts/)
* asamblea [Aspose.Words](../../)
