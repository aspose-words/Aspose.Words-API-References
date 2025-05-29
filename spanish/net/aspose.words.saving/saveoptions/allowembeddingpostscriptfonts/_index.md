---
title: SaveOptions.AllowEmbeddingPostScriptFonts
linktitle: AllowEmbeddingPostScriptFonts
articleTitle: AllowEmbeddingPostScriptFonts
second_title: Aspose.Words para .NET
description: Controle la incrustación de fuentes en sus documentos con AllowEmbeddingPostScriptFonts de SaveOptions. Administre fácilmente las opciones de fuentes TrueType para mejorar la calidad de sus documentos.
type: docs
weight: 20
url: /es/net/aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/
---
## SaveOptions.AllowEmbeddingPostScriptFonts property

Obtiene o establece un valor booleano que indica si se debe permitir la incrustación de fuentes con contornos PostScript al incrustar fuentes TrueType en un documento al guardarlo. El valor predeterminado es`FALSO` .

```csharp
public bool AllowEmbeddingPostScriptFonts { get; set; }
```

## Observaciones

Nota: Word no incorpora fuentes PostScript, pero puede abrir documentos con fuentes de este tipo integradas.

Esta opción sólo funciona cuando[`EmbedTrueTypeFonts`](../../../aspose.words.fonts/fontinfocollection/embedtruetypefonts/) del [`FontInfos`](../../../aspose.words/documentbase/fontinfos/) La propiedad está establecida en`verdadero`.

## Ejemplos

Muestra cómo guardar el documento con fuente PostScript.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "PostScriptFont";
builder.Writeln("Some text with PostScript font.");

//Cargue la fuente con PostScript para usar en el documento.
MemoryFontSource otf = new MemoryFontSource(File.ReadAllBytes(FontsDir + "AllegroOpen.otf"));
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] { otf });

// Incrustar fuentes TrueType.
doc.FontInfos.EmbedTrueTypeFonts = true;

// Permitir incrustar fuentes PostScript mientras se incrustan fuentes TrueType.
// Microsoft Word no incorpora fuentes PostScript, pero puede abrir documentos con fuentes de este tipo integradas.
SaveOptions saveOptions = SaveOptions.CreateSaveOptions(SaveFormat.Docx);
saveOptions.AllowEmbeddingPostScriptFonts = true;

doc.Save(ArtifactsDir + "Document.AllowEmbeddingPostScriptFonts.docx", saveOptions);
```

### Ver también

* class [SaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
