---
title: FontInfoCollection.EmbedTrueTypeFonts
second_title: Referencia de API de Aspose.Words para .NET
description: FontInfoCollection propiedad. Especifica si se incrustan o no fuentes TrueType en un documento cuando se guarda. El valor predeterminado para esta propiedad es falso .
type: docs
weight: 30
url: /es/net/aspose.words.fonts/fontinfocollection/embedtruetypefonts/
---
## FontInfoCollection.EmbedTrueTypeFonts property

Especifica si se incrustan o no fuentes TrueType en un documento cuando se guarda. El valor predeterminado para esta propiedad es **falso** .

```csharp
public bool EmbedTrueTypeFonts { get; set; }
```

### Observaciones

Incrustar fuentes TrueType permite que otros vean el documento con las mismas fuentes que se usaron para crearlo, pero puede aumentar sustancialmente el tamaño del documento.

Esta opción funciona solo para los formatos DOC, DOCX y RTF.

### Ejemplos

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

* class [FontInfoCollection](../)
* espacio de nombres [Aspose.Words.Fonts](../../fontinfocollection/)
* asamblea [Aspose.Words](../../../)


