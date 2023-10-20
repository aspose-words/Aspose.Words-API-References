---
title: SaveOptions.AllowEmbeddingPostScriptFonts
linktitle: AllowEmbeddingPostScriptFonts
articleTitle: AllowEmbeddingPostScriptFonts
second_title: Aspose.Words für .NET
description: SaveOptions AllowEmbeddingPostScriptFonts eigendom. Ruft einen booleschen Wert ab oder legt diesen fest der angibt ob das Einbetten von Schriftarten mit PostScriptUmrissen zulässig ist  wenn TrueTypeSchriftarten in ein Dokument eingebettet werden sobald es gespeichert wird. Der Standardwert istFALSCH  in C#.
type: docs
weight: 20
url: /de/net/aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/
---
## SaveOptions.AllowEmbeddingPostScriptFonts property

Ruft einen booleschen Wert ab oder legt diesen fest, der angibt, ob das Einbetten von Schriftarten mit PostScript-Umrissen zulässig ist , wenn TrueType-Schriftarten in ein Dokument eingebettet werden, sobald es gespeichert wird. Der Standardwert ist`FALSCH` .

```csharp
public bool AllowEmbeddingPostScriptFonts { get; set; }
```

## Bemerkungen

Beachten Sie, dass Word keine PostScript-Schriftarten einbettet, aber Dokumente mit eingebetteten Schriftarten dieses Typs öffnen kann.

Diese Option funktioniert nur, wenn[`EmbedTrueTypeFonts`](../../../aspose.words.fonts/fontinfocollection/embedtruetypefonts/) des [`FontInfos`](../../../aspose.words/documentbase/fontinfos/) Die Eigenschaft ist auf festgelegt`WAHR`.

## Beispiele

Zeigt, wie das Dokument mit der PostScript-Schriftart gespeichert wird.

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

// Das Einbetten von PostScript-Schriftarten beim Einbetten von TrueType-Schriftarten zulassen.
// Microsoft Word bettet keine PostScript-Schriftarten ein, kann aber Dokumente mit eingebetteten Schriftarten dieses Typs öffnen.
SaveOptions saveOptions = SaveOptions.CreateSaveOptions(SaveFormat.Docx);
saveOptions.AllowEmbeddingPostScriptFonts = true;

doc.Save(ArtifactsDir + "Document.AllowEmbeddingPostScriptFonts.docx", saveOptions);
```

### Siehe auch

* class [SaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
