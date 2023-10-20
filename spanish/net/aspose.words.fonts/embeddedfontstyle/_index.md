---
title: EmbeddedFontStyle Enum
linktitle: EmbeddedFontStyle
articleTitle: EmbeddedFontStyle
second_title: Aspose.Words para .NET
description: Aspose.Words.Fonts.EmbeddedFontStyle enumeración. Especifica el estilo de una fuente incrustada dentro de unFontInfo objeto en C#.
type: docs
weight: 2860
url: /es/net/aspose.words.fonts/embeddedfontstyle/
---
## EmbeddedFontStyle enumeration

Especifica el estilo de una fuente incrustada dentro de un[`FontInfo`](../fontinfo/) objeto.

```csharp
[Flags]
public enum EmbeddedFontStyle
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Regular | `0` | Especifica la fuente incrustada normal. |
| Bold | `1` | Especifica la fuente incrustada en negrita. |
| Italic | `2` | Especifica la fuente incrustada en cursiva. |
| BoldItalic | `3` | Especifica la fuente incrustada negrita-cursiva. |

## Ejemplos

Muestra cómo extraer una fuente incrustada de un documento y guardarla en el sistema de archivos local.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfo embeddedFont = doc.FontInfos["Alte DIN 1451 Mittelschrift"];
byte[] embeddedFontBytes = embeddedFont.GetEmbeddedFont(EmbeddedFontFormat.OpenType, EmbeddedFontStyle.Regular);
File.WriteAllBytes(ArtifactsDir + "Alte DIN 1451 Mittelschrift.ttf", embeddedFontBytes);

// Los formatos de fuentes incrustados pueden ser diferentes en otros formatos como .doc.
// Necesitamos saber el formato correcto antes de poder extraer la fuente.
doc = new Document(MyDir + "Embedded font.doc");

Assert.IsNull(doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFont(EmbeddedFontFormat.OpenType, EmbeddedFontStyle.Regular));
Assert.IsNotNull(doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFont(EmbeddedFontFormat.EmbeddedOpenType, EmbeddedFontStyle.Regular));

// Además, podemos convertir el formato OpenType incrustado, que proviene de documentos .doc, a OpenType.
embeddedFontBytes = doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFontAsOpenType(EmbeddedFontStyle.Regular);

File.WriteAllBytes(ArtifactsDir + "Alte DIN 1451 Mittelschrift.otf", embeddedFontBytes);
```

### Ver también

* espacio de nombres [Aspose.Words.Fonts](../../aspose.words.fonts/)
* asamblea [Aspose.Words](../../)
