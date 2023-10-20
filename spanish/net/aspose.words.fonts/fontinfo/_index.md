---
title: FontInfo Class
linktitle: FontInfo
articleTitle: FontInfo
second_title: Aspose.Words para .NET
description: Aspose.Words.Fonts.FontInfo clase. Especifica información sobre una fuente utilizada en el documento en C#.
type: docs
weight: 2920
url: /es/net/aspose.words.fonts/fontinfo/
---
## FontInfo class

Especifica información sobre una fuente utilizada en el documento.

Para obtener más información, visite el[Trabajar con fuentes](https://docs.aspose.com/words/net/working-with-fonts/) artículo de documentación.

```csharp
public class FontInfo
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [AltName](../../aspose.words.fonts/fontinfo/altname/) { get; set; } | Obtiene o establece el nombre alternativo de la fuente. |
| [Charset](../../aspose.words.fonts/fontinfo/charset/) { get; set; } | Obtiene o establece el juego de caracteres para la fuente. |
| [Family](../../aspose.words.fonts/fontinfo/family/) { get; set; } | Obtiene o establece la familia de fuentes a la que pertenece esta fuente. |
| [IsTrueType](../../aspose.words.fonts/fontinfo/istruetype/) { get; set; } | Indica que esta fuente es una fuente TrueType u OpenType en lugar de una fuente rasterizada o vectorial. El valor predeterminado es`verdadero` . |
| [Name](../../aspose.words.fonts/fontinfo/name/) { get; } | Obtiene el nombre de la fuente. |
| [Panose](../../aspose.words.fonts/fontinfo/panose/) { get; set; } | Obtiene o establece el número de clasificación del tipo de letra PANOSE. |
| [Pitch](../../aspose.words.fonts/fontinfo/pitch/) { get; set; } | El paso indica si la fuente tiene un paso fijo, un espaciado proporcional o se basa en una configuración predeterminada. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [GetEmbeddedFont](../../aspose.words.fonts/fontinfo/getembeddedfont/)(*[EmbeddedFontFormat](../embeddedfontformat/), [EmbeddedFontStyle](../embeddedfontstyle/)*) | Obtiene un archivo de fuente incrustado específico. |
| [GetEmbeddedFontAsOpenType](../../aspose.words.fonts/fontinfo/getembeddedfontasopentype/)(*[EmbeddedFontStyle](../embeddedfontstyle/)*) | Obtiene un archivo de fuente incrustado en formato OpenType. Las fuentes en formato OpenType incrustado se convierten a OpenType. |

## Observaciones

No crea instancias de esta clase directamente. Utilice el[`FontInfos`](../../aspose.words/documentbase/fontinfos/) Propiedad para acceder a la colección de fuentes definidas en un documento.

## Ejemplos

Muestra cómo imprimir los detalles de las fuentes presentes en un documento.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfoCollection allFonts = doc.FontInfos;
// Imprime todas las fuentes usadas y no utilizadas en el documento.
for (int i = 0; i < allFonts.Count; i++)
{
    Console.WriteLine($"Font index #{i}");
    Console.WriteLine($"\tName: {allFonts[i].Name}");
    Console.WriteLine($"\tIs {(allFonts[i].IsTrueType ? "" : "not ")}a trueType font");
}
```

### Ver también

* espacio de nombres [Aspose.Words.Fonts](../../aspose.words.fonts/)
* asamblea [Aspose.Words](../../)
