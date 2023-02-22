---
title: FontInfoCollection.EmbedSystemFonts
second_title: Referencia de API de Aspose.Words para .NET
description: FontInfoCollection propiedad. Especifica si se incrustan o no las fuentes del sistema en el documento. El valor predeterminado para esta propiedad es falso.
type: docs
weight: 20
url: /es/net/aspose.words.fonts/fontinfocollection/embedsystemfonts/
---
## FontInfoCollection.EmbedSystemFonts property

Especifica si se incrustan o no las fuentes del sistema en el documento. El valor predeterminado para esta propiedad es **falso**.

Esta opción solo funciona cuando[`EmbedTrueTypeFonts`](../embedtruetypefonts/) la opción está configurada para **verdadero**.

```csharp
public bool EmbedSystemFonts { get; set; }
```

### Observaciones

Establecer esta propiedad en`Verdadero`es útil si el usuario está en un sistema de Asia oriental y desea crear un documento que puedan leer otras personas que no tienen fuentes para ese idioma en su sistema. Por ejemplo, un usuario en un sistema japonés podría elegir incrustar las fuentes en un documento para que el documento japonés sea legible en todos los sistemas.

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


