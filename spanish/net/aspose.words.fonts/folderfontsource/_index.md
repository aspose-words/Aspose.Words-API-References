---
title: Class FolderFontSource
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Fonts.FolderFontSource clase. Representa la carpeta que contiene archivos de fuentes TrueType.
type: docs
weight: 2880
url: /es/net/aspose.words.fonts/folderfontsource/
---
## FolderFontSource class

Representa la carpeta que contiene archivos de fuentes TrueType.

Para obtener más información, visite el[Trabajar con fuentes](https://docs.aspose.com/words/net/working-with-fonts/) artículo de documentación.

```csharp
public class FolderFontSource : FontSourceBase
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [FolderFontSource](folderfontsource/#constructor)(string, bool) | Director. |
| [FolderFontSource](folderfontsource/#constructor_1)(string, bool, int) | Director. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [FolderPath](../../aspose.words.fonts/folderfontsource/folderpath/) { get; } | Ruta a la carpeta. |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | Devuelve la prioridad de fuente de fuente. |
| [ScanSubfolders](../../aspose.words.fonts/folderfontsource/scansubfolders/) { get; } | Determina si se escanean o no las subcarpetas. |
| override [Type](../../aspose.words.fonts/folderfontsource/type/) { get; } | Devuelve el tipo de fuente fuente. |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | Se llama durante el procesamiento del origen de la fuente cuando se detecta un problema que podría provocar una pérdida de fidelidad del formato. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | Devuelve una lista de fuentes disponibles a través de esta fuente. |

### Ejemplos

Muestra cómo utilizar una carpeta del sistema local que contiene fuentes como fuente de fuentes.

```csharp
// Crea una fuente de fuente desde una carpeta que contiene archivos de fuentes.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false, 1);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

Assert.AreEqual(FontsDir, folderFontSource.FolderPath);
Assert.AreEqual(false, folderFontSource.ScanSubfolders);
Assert.AreEqual(FontSourceType.FontsFolder, folderFontSource.Type);
Assert.AreEqual(1, folderFontSource.Priority);
```

### Ver también

* class [FontSourceBase](../fontsourcebase/)
* espacio de nombres [Aspose.Words.Fonts](../../aspose.words.fonts/)
* asamblea [Aspose.Words](../../)


