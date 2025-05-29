---
title: EmbeddedFontFormat Enum
linktitle: EmbeddedFontFormat
articleTitle: EmbeddedFontFormat
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.EmbeddedFontFormat, que define los formatos de las fuentes incrustadas en el objeto FontInfo para mejorar el estilo del documento.
type: docs
weight: 3260
url: /es/net/aspose.words.fonts/embeddedfontformat/
---
## EmbeddedFontFormat enumeration

Especifica el formato de una fuente incrustada particular en el interior[`FontInfo`](../fontinfo/) objeto.

Al guardar un documento en un archivo, solo se escriben las fuentes incrustadas del formato correspondiente.

```csharp
public enum EmbeddedFontFormat
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| EmbeddedOpenType | `0` | Especifica el formato de archivo Embedded OpenType (EOT). |
| OpenType | `1` | Especifica la fuente, incrustada como copia simple del archivo de fuente OpenType (TrueType). |

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
