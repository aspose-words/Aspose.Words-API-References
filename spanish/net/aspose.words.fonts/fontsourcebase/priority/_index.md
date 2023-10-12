---
title: FontSourceBase.Priority
second_title: Referencia de API de Aspose.Words para .NET
description: FontSourceBase propiedad. Devuelve la prioridad de fuente de fuente.
type: docs
weight: 10
url: /es/net/aspose.words.fonts/fontsourcebase/priority/
---
## FontSourceBase.Priority property

Devuelve la prioridad de fuente de fuente.

```csharp
public int Priority { get; }
```

### Observaciones

Este valor se utiliza cuando hay fuentes con el mismo nombre de familia y estilo en diferentes fuentes. En este caso, Aspose.Words selecciona la fuente de la fuente con el valor de prioridad más alto.

El valor predeterminado es 0.

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

* class [FontSourceBase](../)
* espacio de nombres [Aspose.Words.Fonts](../../fontsourcebase/)
* asamblea [Aspose.Words](../../../)


