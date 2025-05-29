---
title: FileFontSource.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words para .NET
description: Descubra la propiedad Tipo FileFontSource para identificar fácilmente los tipos de fuentes y mejorar sus proyectos de diseño con soluciones tipográficas precisas.
type: docs
weight: 40
url: /es/net/aspose.words.fonts/filefontsource/type/
---
## FileFontSource.Type property

Devuelve el tipo de la fuente de origen.

```csharp
public override FontSourceType Type { get; }
```

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

* enum [FontSourceType](../../fontsourcetype/)
* class [FileFontSource](../)
* espacio de nombres [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* asamblea [Aspose.Words](../../../)
