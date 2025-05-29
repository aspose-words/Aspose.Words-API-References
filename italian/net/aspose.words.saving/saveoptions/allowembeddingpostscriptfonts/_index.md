---
title: SaveOptions.AllowEmbeddingPostScriptFonts
linktitle: AllowEmbeddingPostScriptFonts
articleTitle: AllowEmbeddingPostScriptFonts
second_title: Aspose.Words per .NET
description: Controlla l'incorporamento dei font nei tuoi documenti con AllowEmbeddingPostScriptFonts di SaveOptions. Gestisci facilmente le opzioni dei font TrueType per una migliore qualità dei documenti.
type: docs
weight: 20
url: /it/net/aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/
---
## SaveOptions.AllowEmbeddingPostScriptFonts property

Ottiene o imposta un valore booleano che indica se consentire l'incorporamento di font con contorni PostScript quando si incorporano font TrueType in un documento al momento del salvataggio. Il valore predefinito è`falso` .

```csharp
public bool AllowEmbeddingPostScriptFonts { get; set; }
```

## Osservazioni

Nota: Word non incorpora i font PostScript, ma può aprire documenti con font incorporati di questo tipo.

Questa opzione funziona solo quando[`EmbedTrueTypeFonts`](../../../aspose.words.fonts/fontinfocollection/embedtruetypefonts/) del [`FontInfos`](../../../aspose.words/documentbase/fontinfos/) la proprietà è impostata su`VERO`.

## Esempi

Mostra come salvare il documento con il font PostScript.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "PostScriptFont";
builder.Writeln("Some text with PostScript font.");

// Carica il font con PostScript da utilizzare nel documento.
MemoryFontSource otf = new MemoryFontSource(File.ReadAllBytes(FontsDir + "AllegroOpen.otf"));
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] { otf });

// Incorpora i font TrueType.
doc.FontInfos.EmbedTrueTypeFonts = true;

// Consenti l'incorporamento di font PostScript durante l'incorporamento di font TrueType.
// Microsoft Word non incorpora i font PostScript, ma può aprire documenti con font incorporati di questo tipo.
SaveOptions saveOptions = SaveOptions.CreateSaveOptions(SaveFormat.Docx);
saveOptions.AllowEmbeddingPostScriptFonts = true;

doc.Save(ArtifactsDir + "Document.AllowEmbeddingPostScriptFonts.docx", saveOptions);
```

### Guarda anche

* class [SaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
