---
title: Class MemoryFontSource
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Fonts.MemoryFontSource clase. Representa el único archivo de fuente TrueType almacenado en la memoria.
type: docs
weight: 2840
url: /es/net/aspose.words.fonts/memoryfontsource/
---
## MemoryFontSource class

Representa el único archivo de fuente TrueType almacenado en la memoria.

```csharp
public class MemoryFontSource : FontSourceBase
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [MemoryFontSource](memoryfontsource/#constructor)(byte[]) | Director |
| [MemoryFontSource](memoryfontsource/#constructor_1)(byte[], int) | Director |
| [MemoryFontSource](memoryfontsource/#constructor_2)(byte[], int, string) | Director |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [CacheKey](../../aspose.words.fonts/memoryfontsource/cachekey/) { get; } | La clave de esta fuente en el caché. |
| [FontData](../../aspose.words.fonts/memoryfontsource/fontdata/) { get; } | Datos de fuentes binarias. |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | Devuelve la prioridad de origen de la fuente. |
| override [Type](../../aspose.words.fonts/memoryfontsource/type/) { get; } | Devuelve el tipo de fuente fuente. |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | Llamado durante el procesamiento del origen de la fuente cuando se detecta un problema que podría resultar en la pérdida de fidelidad del formato. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | Devuelve la lista de fuentes disponibles a través de esta fuente. |

### Ejemplos

Muestra cómo usar una matriz de bytes con datos de un archivo de fuente como fuente de fuente.

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

* class [FontSourceBase](../fontsourcebase/)
* espacio de nombres [Aspose.Words.Fonts](../../aspose.words.fonts/)
* asamblea [Aspose.Words](../../)


