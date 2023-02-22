---
title: SaveOptions.AllowEmbeddingPostScriptFonts
second_title: Referencia de API de Aspose.Words para .NET
description: SaveOptions propiedad. Obtiene o establece un valor booleano que indica si se permiten incrustar fuentes con contornos PostScript al incrustar fuentes TrueType en un documento que se guarda. El valor predeterminado es falso .
type: docs
weight: 20
url: /es/net/aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/
---
## SaveOptions.AllowEmbeddingPostScriptFonts property

Obtiene o establece un valor booleano que indica si se permiten incrustar fuentes con contornos PostScript al incrustar fuentes TrueType en un documento que se guarda. El valor predeterminado es **falso** .

```csharp
public bool AllowEmbeddingPostScriptFonts { get; set; }
```

### Observaciones

Tenga en cuenta que Word no incrusta fuentes PostScript, pero puede abrir documentos con fuentes incrustadas de este tipo.

Esta opción solo funciona cuando[`EmbedTrueTypeFonts`](../../../aspose.words.fonts/fontinfocollection/embedtruetypefonts/) de la [`FontInfos`](../../../aspose.words/documentbase/fontinfos/) la propiedad se establece en`verdadero`.

### Ejemplos

Muestra cómo guardar el documento con fuente PostScript.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "PostScriptFont";
builder.Writeln("Some text with PostScript font.");

// Cargar la fuente con PostScript para usar en el documento.
MemoryFontSource otf = new MemoryFontSource(File.ReadAllBytes(FontsDir + "AllegroOpen.otf"));
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] { otf });

// Incrustar fuentes TrueType.
doc.FontInfos.EmbedTrueTypeFonts = true;

// Permitir incrustar fuentes PostScript al incrustar fuentes TrueType.
// Microsoft Word no incrusta fuentes PostScript, pero puede abrir documentos con fuentes incrustadas de este tipo.
SaveOptions saveOptions = SaveOptions.CreateSaveOptions(SaveFormat.Docx);
saveOptions.AllowEmbeddingPostScriptFonts = true;

doc.Save(ArtifactsDir + "Document.AllowEmbeddingPostScriptFonts.docx", saveOptions);
```

### Ver también

* class [SaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../saveoptions/)
* asamblea [Aspose.Words](../../../)


