---
title: FontInfo.GetEmbeddedFontAsOpenType
second_title: Referencia de API de Aspose.Words para .NET
description: FontInfo método. Obtiene un archivo de fuente incrustado en formato OpenType. Las fuentes en formato OpenType incrustado se convierten a OpenType.
type: docs
weight: 90
url: /es/net/aspose.words.fonts/fontinfo/getembeddedfontasopentype/
---
## FontInfo.GetEmbeddedFontAsOpenType method

Obtiene un archivo de fuente incrustado en formato OpenType. Las fuentes en formato OpenType incrustado se convierten a OpenType.

```csharp
public byte[] GetEmbeddedFontAsOpenType(EmbeddedFontStyle style)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| style | EmbeddedFontStyle | Especifica el estilo de fuente a recuperar. |

### Valor_devuelto

Devoluciones`nulo`si la fuente especificada no está incrustada.

### Ejemplos

Muestra cómo extraer una fuente incrustada de un documento y guardarla en el sistema de archivos local.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfo embeddedFont = doc.FontInfos["Alte DIN 1451 Mittelschrift"];
byte[] embeddedFontBytes = embeddedFont.GetEmbeddedFont(EmbeddedFontFormat.OpenType, EmbeddedFontStyle.Regular);
File.WriteAllBytes(ArtifactsDir + "Alte DIN 1451 Mittelschrift.ttf", embeddedFontBytes);

// Los formatos de fuentes incrustadas pueden ser diferentes en otros formatos como .doc.
// Necesitamos saber el formato correcto antes de poder extraer la fuente.
doc = new Document(MyDir + "Embedded font.doc");

Assert.IsNull(doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFont(EmbeddedFontFormat.OpenType, EmbeddedFontStyle.Regular));
Assert.IsNotNull(doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFont(EmbeddedFontFormat.EmbeddedOpenType, EmbeddedFontStyle.Regular));

// Además, podemos convertir el formato OpenType incrustado, que proviene de documentos .doc, a OpenType.
embeddedFontBytes = doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFontAsOpenType(EmbeddedFontStyle.Regular);

File.WriteAllBytes(ArtifactsDir + "Alte DIN 1451 Mittelschrift.otf", embeddedFontBytes);
```

### Ver también

* enum [EmbeddedFontStyle](../../embeddedfontstyle/)
* class [FontInfo](../)
* espacio de nombres [Aspose.Words.Fonts](../../fontinfo/)
* asamblea [Aspose.Words](../../../)


