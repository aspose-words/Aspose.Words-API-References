---
title: EmbeddedFontStyle Enum
linktitle: EmbeddedFontStyle
articleTitle: EmbeddedFontStyle
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words EmbeddedFontStyle para administrar fácilmente estilos de fuente incrustados en objetos FontInfo, mejorando sus capacidades de formato de documentos.
type: docs
weight: 3270
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
| Regular | `0` | Especifica la fuente incrustada Regular. |
| Bold | `1` | Especifica la fuente incrustada en negrita. |
| Italic | `2` | Especifica la fuente itálica incrustada. |
| BoldItalic | `3` | Especifica la fuente incrustada en negrita y cursiva. |

## Ejemplos

Muestra cómo extraer una fuente incrustada de un documento y guardarla en el sistema de archivos local.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfo embeddedFont = doc.FontInfos["Alte DIN 1451 Mittelschrift"];
byte[] embeddedFontBytes = embeddedFont.GetEmbeddedFont(EmbeddedFontFormat.OpenType, EmbeddedFontStyle.Regular);
File.WriteAllBytes(ArtifactsDir + "Alte DIN 1451 Mittelschrift.ttf", embeddedFontBytes);

// Los formatos de fuentes incrustadas pueden ser diferentes en otros formatos como .doc.
//Necesitamos saber el formato correcto antes de poder extraer la fuente.
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
