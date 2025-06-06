---
title: MemoryFontSource.FontData
linktitle: FontData
articleTitle: FontData
second_title: Aspose.Words para .NET
description: Descubra la propiedad FontData de MemoryFontSource para una integración fluida de fuentes binarias. Optimice sus proyectos con soluciones eficientes de gestión de fuentes.
type: docs
weight: 30
url: /es/net/aspose.words.fonts/memoryfontsource/fontdata/
---
## MemoryFontSource.FontData property

Datos de fuente binarios.

```csharp
public byte[] FontData { get; }
```

## Ejemplos

Muestra cómo utilizar una matriz de bytes con datos de un archivo de fuente como fuente.

```csharp
byte[] fontBytes = File.ReadAllBytes(MyDir + "Alte DIN 1451 Mittelschrift.ttf");
MemoryFontSource memoryFontSource = new MemoryFontSource(fontBytes, 0);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {memoryFontSource});

Assert.AreEqual(FontSourceType.MemoryFont, memoryFontSource.Type);
Assert.AreEqual(0, memoryFontSource.Priority);
```

### Ver también

* class [MemoryFontSource](../)
* espacio de nombres [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* asamblea [Aspose.Words](../../../)
