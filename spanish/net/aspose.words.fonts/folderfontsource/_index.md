---
title: FolderFontSource Class
linktitle: FolderFontSource
articleTitle: FolderFontSource
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Fonts.FolderFontSource, su solución para gestionar fuentes TrueType eficientemente. ¡Mejore la tipografía de sus documentos hoy mismo!
type: docs
weight: 3290
url: /es/net/aspose.words.fonts/folderfontsource/
---
## FolderFontSource class

Representa la carpeta que contiene los archivos de fuentes TrueType.

Para obtener más información, visite el[Trabajar con fuentes](https://docs.aspose.com/words/net/working-with-fonts/) Artículo de documentación.

```csharp
public class FolderFontSource : FontSourceBase
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [FolderFontSource](folderfontsource/#constructor)(*string, bool*) | Ctor. |
| [FolderFontSource](folderfontsource/#constructor_1)(*string, bool, int*) | Ctor. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [FolderPath](../../aspose.words.fonts/folderfontsource/folderpath/) { get; } | Ruta a la carpeta. |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | Devuelve la prioridad de la fuente. |
| [ScanSubfolders](../../aspose.words.fonts/folderfontsource/scansubfolders/) { get; } | Determina si se deben escanear o no las subcarpetas. |
| override [Type](../../aspose.words.fonts/folderfontsource/type/) { get; } | Devuelve el tipo de la fuente de origen. |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | Se llama durante el procesamiento de la fuente de origen cuando se detecta un problema que podría provocar la pérdida de fidelidad del formato. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | Devuelve la lista de fuentes disponibles a través de esta fuente. |

## Ejemplos

Muestra cómo utilizar una carpeta de sistema local que contiene fuentes como fuente de fuentes.

```csharp
// Crea una fuente de fuente desde una carpeta que contiene archivos de fuente.
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
