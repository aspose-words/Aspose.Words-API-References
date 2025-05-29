---
title: FontInfoCollection.SaveSubsetFonts
linktitle: SaveSubsetFonts
articleTitle: SaveSubsetFonts
second_title: Aspose.Words para .NET
description: Descubra la propiedad SaveSubsetFonts de FontInfoCollection, controle los subconjuntos de fuentes TrueType integrados en sus documentos para optimizar el tamaño y el rendimiento de los archivos.
type: docs
weight: 50
url: /es/net/aspose.words.fonts/fontinfocollection/savesubsetfonts/
---
## FontInfoCollection.SaveSubsetFonts property

Especifica si se debe guardar o no un subconjunto de las fuentes TrueType incrustadas con el documento. El valor predeterminado para esta propiedad es`FALSO`.

Esta opción sólo funciona cuando[`EmbedTrueTypeFonts`](../embedtruetypefonts/) La propiedad está establecida en`verdadero`.

```csharp
public bool SaveSubsetFonts { get; set; }
```

## Observaciones

Esta opción funciona únicamente para formatos DOC, DOCX y RTF.

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

### Ver también

* class [FontInfoCollection](../)
* espacio de nombres [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* asamblea [Aspose.Words](../../../)
