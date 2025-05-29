---
title: FontInfo Class
linktitle: FontInfo
articleTitle: FontInfo
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Fonts.FontInfo, su clave para obtener información detallada sobre fuentes para documentos, mejorando la calidad del texto y el atractivo visual.
type: docs
weight: 3350
url: /es/net/aspose.words.fonts/fontinfo/
---
## FontInfo class

Especifica información sobre una fuente utilizada en el documento.

Para obtener más información, visite el[Trabajar con fuentes](https://docs.aspose.com/words/net/working-with-fonts/) Artículo de documentación.

```csharp
public class FontInfo
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [AltName](../../aspose.words.fonts/fontinfo/altname/) { get; set; } | Obtiene o establece el nombre alternativo para la fuente. |
| [Charset](../../aspose.words.fonts/fontinfo/charset/) { get; set; } | Obtiene o establece el conjunto de caracteres para la fuente. |
| [EmbeddingLicensingRights](../../aspose.words.fonts/fontinfo/embeddinglicensingrights/) { get; } | Obtiene los derechos de licencia de fuentes incrustadas. |
| [Family](../../aspose.words.fonts/fontinfo/family/) { get; set; } | Obtiene o establece la familia de fuentes a la que pertenece esta fuente. |
| [IsTrueType](../../aspose.words.fonts/fontinfo/istruetype/) { get; set; } | Indica que esta fuente es una fuente TrueType u OpenType en lugar de una fuente raster o vectorial. El valor predeterminado es`verdadero` . |
| [Name](../../aspose.words.fonts/fontinfo/name/) { get; } | Obtiene el nombre de la fuente. |
| [Panose](../../aspose.words.fonts/fontinfo/panose/) { get; set; } | Obtiene o establece el número de clasificación de tipografía PANOSE. |
| [Pitch](../../aspose.words.fonts/fontinfo/pitch/) { get; set; } | El paso indica si la fuente tiene un paso fijo, está espaciada proporcionalmente o se basa en una configuración predeterminada. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [GetEmbeddedFont](../../aspose.words.fonts/fontinfo/getembeddedfont/)(*[EmbeddedFontFormat](../embeddedfontformat/), [EmbeddedFontStyle](../embeddedfontstyle/)*) | Obtiene un archivo de fuente incrustado específico. |
| [GetEmbeddedFontAsOpenType](../../aspose.words.fonts/fontinfo/getembeddedfontasopentype/)(*[EmbeddedFontStyle](../embeddedfontstyle/)*) | Obtiene un archivo de fuente incrustada en formato OpenType. Las fuentes en formato OpenType incrustado se convierten a OpenType. |

## Observaciones

No se crean instancias de esta clase directamente. Utilice el[`FontInfos`](../../aspose.words/documentbase/fontinfos/) propiedad para acceder a la colección de fonts definidas en un documento.

## Ejemplos

Muestra cómo imprimir los detalles de las fuentes presentes en un documento.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfoCollection allFonts = doc.FontInfos;
// Imprime todas las fuentes utilizadas y no utilizadas en el documento.
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
