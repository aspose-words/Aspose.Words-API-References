---
title: FontInfoCollection Class
linktitle: FontInfoCollection
articleTitle: FontInfoCollection
second_title: Aspose.Words para .NET
description: Aspose.Words.Fonts.FontInfoCollection clase. Representa una colección de fuentes utilizadas en un documento en C#.
type: docs
weight: 2930
url: /es/net/aspose.words.fonts/fontinfocollection/
---
## FontInfoCollection class

Representa una colección de fuentes utilizadas en un documento.

Para obtener más información, visite el[Trabajar con fuentes](https://docs.aspose.com/words/net/working-with-fonts/) artículo de documentación.

```csharp
public class FontInfoCollection : IEnumerable<FontInfo>
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Count](../../aspose.words.fonts/fontinfocollection/count/) { get; } | Obtiene el número de elementos contenidos en la colección. |
| [EmbedSystemFonts](../../aspose.words.fonts/fontinfocollection/embedsystemfonts/) { get; set; } | Especifica si se incrustan o no fuentes del sistema en el documento. El valor predeterminado para esta propiedad es`FALSO`. |
| [EmbedTrueTypeFonts](../../aspose.words.fonts/fontinfocollection/embedtruetypefonts/) { get; set; } | Especifica si se incrustan o no fuentes TrueType en un documento cuando se guarda. El valor predeterminado para esta propiedad es`FALSO` . |
| [Item](../../aspose.words.fonts/fontinfocollection/item/) { get; } | Obtiene una fuente con el nombre especificado. (2 indexers) |
| [SaveSubsetFonts](../../aspose.words.fonts/fontinfocollection/savesubsetfonts/) { get; set; } | Especifica si se guarda o no un subconjunto de las fuentes TrueType incrustadas con el documento. El valor predeterminado para esta propiedad es`FALSO`. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Contains](../../aspose.words.fonts/fontinfocollection/contains/)(*string*) | Determina si la colección contiene una fuente con el nombre de pila. |
| [GetEnumerator](../../aspose.words.fonts/fontinfocollection/getenumerator/)() | Devuelve un objeto enumerador que se puede utilizar para iterar sobre todos los elementos de la colección. |

## Observaciones

Los artículos son[`FontInfo`](../fontinfo/) objetos.

No crea instancias de esta clase directamente. Utilice el[`FontInfos`](../../aspose.words/documentbase/fontinfos/) propiedad para acceder a la colección de fuentes definidas en el documento.

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

Muestra cómo guardar un documento con fuentes TrueType incrustadas.

```csharp
Document doc = new Document(MyDir + "Document.docx");

FontInfoCollection fontInfos = doc.FontInfos;
fontInfos.EmbedTrueTypeFonts = embedAllFonts;
fontInfos.EmbedSystemFonts = embedAllFonts;
fontInfos.SaveSubsetFonts = embedAllFonts;

doc.Save(ArtifactsDir + "Font.FontInfoCollection.docx");

if (embedAllFonts)
    Assert.That(25000, Is.LessThan(new FileInfo(ArtifactsDir + "Font.FontInfoCollection.docx").Length));
else
    Assert.That(15000, Is.AtLeast(new FileInfo(ArtifactsDir + "Font.FontInfoCollection.docx").Length));
```

### Ver también

* class [FontInfo](../fontinfo/)
* espacio de nombres [Aspose.Words.Fonts](../../aspose.words.fonts/)
* asamblea [Aspose.Words](../../)
