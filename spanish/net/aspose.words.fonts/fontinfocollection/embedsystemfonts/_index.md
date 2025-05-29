---
title: FontInfoCollection.EmbedSystemFonts
linktitle: EmbedSystemFonts
articleTitle: EmbedSystemFonts
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad FontInfoCollection EmbedSystemFonts mejora sus documentos al incrustar fuentes del sistema. ¡Conozca su valor predeterminado y sus ventajas!
type: docs
weight: 20
url: /es/net/aspose.words.fonts/fontinfocollection/embedsystemfonts/
---
## FontInfoCollection.EmbedSystemFonts property

Especifica si se deben incrustar o no fuentes del sistema en el documento. El valor predeterminado para esta propiedad es`FALSO`.

Esta opción sólo funciona cuando[`EmbedTrueTypeFonts`](../embedtruetypefonts/) La opción está establecida en`verdadero`.

```csharp
public bool EmbedSystemFonts { get; set; }
```

## Observaciones

Establecer esta propiedad en`verdadero` Es útil si el usuario utiliza un sistema de Asia Oriental y desea crear un documento legible para quienes no tienen fuentes para ese idioma en su sistema. Por ejemplo, un usuario de un sistema japonés podría optar por incrustar las fuentes en un documento para que este sea legible en todos los sistemas.

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
