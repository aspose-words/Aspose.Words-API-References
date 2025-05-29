---
title: FontSourceType Enum
linktitle: FontSourceType
articleTitle: FontSourceType
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.Fonts.FontSourceType para una gestión eficiente de las fuentes. Optimice el procesamiento de sus documentos con opciones flexibles de fuentes.
type: docs
weight: 3420
url: /es/net/aspose.words.fonts/fontsourcetype/
---
## FontSourceType enumeration

Especifica el tipo de fuente de origen.

```csharp
public enum FontSourceType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| FontFile | `0` | A[`FileFontSource`](../filefontsource/) objeto que representa un solo archivo de fuente. |
| FontsFolder | `1` | A[`FolderFontSource`](../folderfontsource/) objeto que representa la carpeta con archivos de fuentes. |
| MemoryFont | `2` | A[`MemoryFontSource`](../memoryfontsource/) objeto que representa una sola fuente en la memoria. |
| SystemFonts | `3` | A[`SystemFontSource`](../systemfontsource/) objeto que representa todas las fuentes instaladas en el sistema. |
| FontStream | `4` | A[`StreamFontSource`](../streamfontsource/) objeto que representa una secuencia con datos de fuente. |

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

* espacio de nombres [Aspose.Words.Fonts](../../aspose.words.fonts/)
* asamblea [Aspose.Words](../../)
