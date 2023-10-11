---
title: FontInfoCollection.SaveSubsetFonts
second_title: Referencia de API de Aspose.Words para .NET
description: FontInfoCollection propiedad. Especifica si se guarda o no un subconjunto de las fuentes TrueType incrustadas con el documento. El valor predeterminado para esta propiedad esFALSO.
type: docs
weight: 50
url: /es/net/aspose.words.fonts/fontinfocollection/savesubsetfonts/
---
## FontInfoCollection.SaveSubsetFonts property

Especifica si se guarda o no un subconjunto de las fuentes TrueType incrustadas con el documento. El valor predeterminado para esta propiedad es`FALSO`.

Esta opción funciona sólo cuando[`EmbedTrueTypeFonts`](../embedtruetypefonts/) la propiedad está establecida en`verdadero`.

```csharp
public bool SaveSubsetFonts { get; set; }
```

### Observaciones

Esta opción funciona solo para formatos DOC, DOCX y RTF.

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


