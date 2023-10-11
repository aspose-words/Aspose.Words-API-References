---
title: FontInfoCollection.EmbedSystemFonts
second_title: Referencia de API de Aspose.Words para .NET
description: FontInfoCollection propiedad. Especifica si se incrustan o no fuentes del sistema en el documento. El valor predeterminado para esta propiedad esFALSO.
type: docs
weight: 20
url: /es/net/aspose.words.fonts/fontinfocollection/embedsystemfonts/
---
## FontInfoCollection.EmbedSystemFonts property

Especifica si se incrustan o no fuentes del sistema en el documento. El valor predeterminado para esta propiedad es`FALSO`.

Esta opción funciona sólo cuando[`EmbedTrueTypeFonts`](../embedtruetypefonts/) La opción está configurada en`verdadero`.

```csharp
public bool EmbedSystemFonts { get; set; }
```

### Observaciones

Establecer esta propiedad en`verdadero`es útil si el usuario está en un sistema del este de Asia y desea crear un documento que sea legible por otras personas que no tienen fuentes para ese idioma en su sistema. Por ejemplo, un usuario de un sistema japonés podría optar por incrustar las fuentes en un documento para que el documento japonés sea legible en todos los sistemas.

Esta opción sólo funciona con formatos DOC, DOCX y RTF.

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


