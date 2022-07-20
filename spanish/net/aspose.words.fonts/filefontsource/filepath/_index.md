---
title: FilePath
second_title: Referencia de API de Aspose.Words para .NET
description: Ruta al archivo de fuente.
type: docs
weight: 30
url: /es/net/aspose.words.fonts/filefontsource/filepath/
---
## FileFontSource.FilePath property

Ruta al archivo de fuente.

```csharp
public string FilePath { get; }
```

### Ejemplos

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

* class [FileFontSource](../../filefontsource)
* espacio de nombres [Aspose.Words.Fonts](../../filefontsource)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->