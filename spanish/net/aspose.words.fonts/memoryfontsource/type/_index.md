---
title: MemoryFontSource.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words para .NET
description: Descubre la propiedad MemoryFontSource Type, que revela el tipo de fuente de tu fuente, mejorando la precisión y creatividad de tu diseño. ¡Libera el potencial de tus fuentes!
type: docs
weight: 40
url: /es/net/aspose.words.fonts/memoryfontsource/type/
---
## MemoryFontSource.Type property

Devuelve el tipo de la fuente de origen.

```csharp
public override FontSourceType Type { get; }
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

* enum [FontSourceType](../../fontsourcetype/)
* class [MemoryFontSource](../)
* espacio de nombres [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* asamblea [Aspose.Words](../../../)
