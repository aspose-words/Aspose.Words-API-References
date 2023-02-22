---
title: SaveOptions.AllowEmbeddingPostScriptFonts
second_title: Aspose.Words per .NET API Reference
description: SaveOptions proprietà. Ottiene o imposta un valore booleano che indica se consentire lincorporamento di caratteri con contorni PostScript quando lincorporamento di caratteri TrueType in un documento viene salvato. Il valore predefinito è falso .
type: docs
weight: 20
url: /it/net/aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/
---
## SaveOptions.AllowEmbeddingPostScriptFonts property

Ottiene o imposta un valore booleano che indica se consentire l'incorporamento di caratteri con contorni PostScript quando l'incorporamento di caratteri TrueType in un documento viene salvato. Il valore predefinito è **falso** .

```csharp
public bool AllowEmbeddingPostScriptFonts { get; set; }
```

### Osservazioni

Nota, Word non incorpora i caratteri PostScript, ma può aprire documenti con caratteri incorporati di questo tipo.

Questa opzione funziona solo quando[`EmbedTrueTypeFonts`](../../../aspose.words.fonts/fontinfocollection/embedtruetypefonts/) del [`FontInfos`](../../../aspose.words/documentbase/fontinfos/) la proprietà è impostata su`VERO`.

### Esempi

Mostra come salvare il documento con il carattere PostScript.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "PostScriptFont";
builder.Writeln("Some text with PostScript font.");

// Carica il font con PostScript da utilizzare nel documento.
MemoryFontSource otf = new MemoryFontSource(File.ReadAllBytes(FontsDir + "AllegroOpen.otf"));
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] { otf });

// Incorpora i caratteri TrueType.
doc.FontInfos.EmbedTrueTypeFonts = true;

// Consenti l'incorporamento di caratteri PostScript durante l'incorporamento di caratteri TrueType.
// Microsoft Word non incorpora font PostScript, ma può aprire documenti con font incorporati di questo tipo.
SaveOptions saveOptions = SaveOptions.CreateSaveOptions(SaveFormat.Docx);
saveOptions.AllowEmbeddingPostScriptFonts = true;

doc.Save(ArtifactsDir + "Document.AllowEmbeddingPostScriptFonts.docx", saveOptions);
```

### Guarda anche

* class [SaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../saveoptions/)
* assemblea [Aspose.Words](../../../)


