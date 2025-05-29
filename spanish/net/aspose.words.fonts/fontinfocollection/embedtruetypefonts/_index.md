---
title: FontInfoCollection.EmbedTrueTypeFonts
linktitle: EmbedTrueTypeFonts
articleTitle: EmbedTrueTypeFonts
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad EmbedTrueTypeFonts de FontInfoCollection mejora la calidad del documento al permitir la incrustación de fuentes TrueType. El valor predeterminado es falso.
type: docs
weight: 30
url: /es/net/aspose.words.fonts/fontinfocollection/embedtruetypefonts/
---
## FontInfoCollection.EmbedTrueTypeFonts property

Especifica si se deben incrustar o no fuentes TrueType en un documento cuando se guarda. El valor predeterminado para esta propiedad es`FALSO` .

```csharp
public bool EmbedTrueTypeFonts { get; set; }
```

## Observaciones

La incorporación de fuentes TrueType permite que otros vean el documento con las mismas fuentes que se utilizaron para crearlo, pero puede aumentar sustancialmente el tamaño del documento.

Esta opción funciona solo para formatos DOC, DOCX y RTF.

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
