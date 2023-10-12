---
title: SaveOptions.AllowEmbeddingPostScriptFonts
second_title: Referencia de API de Aspose.Words para .NET
description: SaveOptions propiedad. Obtiene o establece un valor booleano que indica si se permite incrustar fuentes con contornos PostScript al incrustar fuentes TrueType en un documento una vez guardado. El valor predeterminado esFALSO .
type: docs
weight: 20
url: /es/net/aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/
---
## SaveOptions.AllowEmbeddingPostScriptFonts property

Obtiene o establece un valor booleano que indica si se permite incrustar fuentes con contornos PostScript al incrustar fuentes TrueType en un documento una vez guardado. El valor predeterminado es`FALSO` .

```csharp
public bool AllowEmbeddingPostScriptFonts { get; set; }
```

### Observaciones

Tenga en cuenta que Word no incorpora fuentes PostScript, pero puede abrir documentos con fuentes incrustadas de este tipo.

Esta opción sólo funciona cuando[`EmbedTrueTypeFonts`](../../../aspose.words.fonts/fontinfocollection/embedtruetypefonts/) del [`FontInfos`](../../../aspose.words/documentbase/fontinfos/) la propiedad está establecida en`verdadero`.

### Ejemplos

Muestra cómo guardar el documento con fuente PostScript.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "PostScriptFont";
builder.Writeln("Some text with PostScript font.");

// Carga la fuente con PostScript para usar en el documento.
MemoryFontSource otf = new MemoryFontSource(File.ReadAllBytes(FontsDir + "AllegroOpen.otf"));
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] { otf });

// Incrustar fuentes TrueType.
doc.FontInfos.EmbedTrueTypeFonts = true;

// Permitir incrustar fuentes PostScript mientras se incrustan fuentes TrueType.
// Microsoft Word no incorpora fuentes PostScript, pero puede abrir documentos con fuentes incrustadas de este tipo.
SaveOptions saveOptions = SaveOptions.CreateSaveOptions(SaveFormat.Docx);
saveOptions.AllowEmbeddingPostScriptFonts = true;

doc.Save(ArtifactsDir + "Document.AllowEmbeddingPostScriptFonts.docx", saveOptions);
```

### Ver también

* class [SaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../saveoptions/)
* asamblea [Aspose.Words](../../../)


