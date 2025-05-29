---
title: SaveOptions.AllowEmbeddingPostScriptFonts
linktitle: AllowEmbeddingPostScriptFonts
articleTitle: AllowEmbeddingPostScriptFonts
second_title: Aspose.Words für .NET
description: Steuern Sie die Schriftarteinbettung in Ihren Dokumenten mit AllowEmbeddingPostScriptFonts von SaveOptions. Verwalten Sie TrueType-Schriftoptionen ganz einfach für eine verbesserte Dokumentqualität.
type: docs
weight: 20
url: /de/net/aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/
---
## SaveOptions.AllowEmbeddingPostScriptFonts property

Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, ob das Einbetten von Schriftarten mit PostScript-Konturen beim Einbetten von TrueType-Schriftarten in ein Dokument beim Speichern zulässig ist. Der Standardwert ist`FALSCH` .

```csharp
public bool AllowEmbeddingPostScriptFonts { get; set; }
```

## Bemerkungen

Beachten Sie, dass Word keine PostScript-Schriftarten einbettet, aber Dokumente mit eingebetteten Schriftarten dieses Typs öffnen kann.

Diese Option funktioniert nur, wenn[`EmbedTrueTypeFonts`](../../../aspose.words.fonts/fontinfocollection/embedtruetypefonts/) von the [`FontInfos`](../../../aspose.words/documentbase/fontinfos/) Eigenschaft ist auf`WAHR`.

## Beispiele

Zeigt, wie das Dokument mit der Schriftart PostScript gespeichert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "PostScriptFont";
builder.Writeln("Some text with PostScript font.");

// Laden Sie die Schriftart mit PostScript, um sie im Dokument zu verwenden.
MemoryFontSource otf = new MemoryFontSource(File.ReadAllBytes(FontsDir + "AllegroOpen.otf"));
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] { otf });

// TrueType-Schriftarten einbetten.
doc.FontInfos.EmbedTrueTypeFonts = true;

// Erlaubt das Einbetten von PostScript-Schriftarten beim Einbetten von TrueType-Schriftarten.
// Microsoft Word bettet keine PostScript-Schriftarten ein, kann aber Dokumente mit eingebetteten Schriftarten dieses Typs öffnen.
SaveOptions saveOptions = SaveOptions.CreateSaveOptions(SaveFormat.Docx);
saveOptions.AllowEmbeddingPostScriptFonts = true;

doc.Save(ArtifactsDir + "Document.AllowEmbeddingPostScriptFonts.docx", saveOptions);
```

### Siehe auch

* class [SaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
