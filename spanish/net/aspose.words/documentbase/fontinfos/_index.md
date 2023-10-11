---
title: DocumentBase.FontInfos
second_title: Referencia de API de Aspose.Words para .NET
description: DocumentBase propiedad. Proporciona acceso a las propiedades de las fuentes utilizadas en este documento.
type: docs
weight: 30
url: /es/net/aspose.words/documentbase/fontinfos/
---
## DocumentBase.FontInfos property

Proporciona acceso a las propiedades de las fuentes utilizadas en este documento.

```csharp
public FontInfoCollection FontInfos { get; }
```

### Observaciones

Esta colección de definiciones de fuentes se carga tal cual desde el documento. Las definiciones de fuentes pueden ser opcionales, faltar o estar incompletas en algunos documentos.

No confíe en esta colección para determinar si se utiliza una fuente concreta en el documento. Sólo debe utilizar esta colección para obtener información sobre las fuentes que podrían utilizarse en el documento.

### Ejemplos

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

* class [FontInfoCollection](../../../aspose.words.fonts/fontinfocollection/)
* class [DocumentBase](../)
* espacio de nombres [Aspose.Words](../../documentbase/)
* asamblea [Aspose.Words](../../../)


