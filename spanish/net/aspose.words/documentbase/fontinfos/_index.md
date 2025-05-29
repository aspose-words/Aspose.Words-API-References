---
title: DocumentBase.FontInfos
linktitle: FontInfos
articleTitle: FontInfos
second_title: Aspose.Words para .NET
description: Acceda a propiedades de fuente detalladas con la función FontInfos de DocumentBase, mejorando el diseño y la legibilidad de su documento sin esfuerzo.
type: docs
weight: 30
url: /es/net/aspose.words/documentbase/fontinfos/
---
## DocumentBase.FontInfos property

Proporciona acceso a las propiedades de las fuentes utilizadas en este documento.

```csharp
public FontInfoCollection FontInfos { get; }
```

## Observaciones

Esta colección de definiciones de fuentes se carga tal cual desde el documento. Las definiciones de fuentes pueden ser opcionales, faltantes o estar incompletas en algunos documentos.

No confíe en esta colección para determinar si se utiliza una fuente particular en el documento. Solo debe utilizar esta colección para obtener información sobre las fuentes que podrían usarse en el documento.

## Ejemplos

Muestra cómo guardar un documento con fuentes TrueType incrustadas.

```csharp
Document doc = new Document(MyDir + "Document.docx");

FontInfoCollection fontInfos = doc.FontInfos;
fontInfos.EmbedTrueTypeFonts = embedAllFonts;
fontInfos.EmbedSystemFonts = embedAllFonts;
fontInfos.SaveSubsetFonts = embedAllFonts;

doc.Save(ArtifactsDir + "Font.FontInfoCollection.docx");
```

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

* class [FontInfoCollection](../../../aspose.words.fonts/fontinfocollection/)
* class [DocumentBase](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
