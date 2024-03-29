---
title: PdfSaveOptions.EmbedFullFonts
linktitle: EmbedFullFonts
articleTitle: EmbedFullFonts
second_title: Aspose.Words für .NET
description: PdfSaveOptions EmbedFullFonts eigendom. Steuert wie Schriftarten in die resultierenden PDFDokumente eingebettet werden in C#.
type: docs
weight: 120
url: /de/net/aspose.words.saving/pdfsaveoptions/embedfullfonts/
---
## PdfSaveOptions.EmbedFullFonts property

Steuert, wie Schriftarten in die resultierenden PDF-Dokumente eingebettet werden.

```csharp
public bool EmbedFullFonts { get; set; }
```

## Bemerkungen

Der Standardwert ist`FALSCH`, was bedeutet, dass die Schriftarten vor dem Einbetten in Teilmengen unterteilt werden. Die Teilmenge ist nützlich, wenn Sie die Größe der Ausgabedatei kleiner halten möchten. Durch die Teilmenge werden alle nicht verwendeten Glyphen aus einer Schriftart entfernt.

Wenn dieser Wert auf eingestellt ist`WAHR`, wird eine vollständige Schriftartdatei ohne -Untereinstellung in das PDF eingebettet. Dies führt zu größeren Ausgabedateien, kann aber eine nützliche Option sein, wenn Sie das resultierende PDF später bearbeiten möchten (z. B. mehr Text hinzufügen).

Einige Schriftarten sind groß (mehrere Megabyte) und ihre Einbettung ohne Untereinstellung führt zu großen Ausgabedokumenten.

## Beispiele

Zeigt, wie die Teilmenge beim Einbetten von Schriftarten beim Rendern eines Dokuments als PDF aktiviert oder deaktiviert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Arvo";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Konfigurieren Sie unsere Schriftartquellen, um sicherzustellen, dass wir Zugriff auf beide Schriftarten in diesem Dokument haben.
FontSourceBase[] originalFontsSources = FontSettings.DefaultInstance.GetFontsSources();
Aspose.Words.Fonts.FolderFontSource folderFontSource = new Aspose.Words.Fonts.FolderFontSource(FontsDir, true);
FontSettings.DefaultInstance.SetFontsSources(new[] { originalFontsSources[0], folderFontSource });

FontSourceBase[] fontSources = FontSettings.DefaultInstance.GetFontsSources();
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(fontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

// Erstellen Sie ein „PdfSaveOptions“-Objekt, das wir an die „Save“-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions options = new PdfSaveOptions();

// Da unser Dokument eine benutzerdefinierte Schriftart enthält, kann eine Einbettung in das Ausgabedokument wünschenswert sein.
// Setzen Sie die Eigenschaft „EmbedFullFonts“ auf „true“, um jedes Glyph jeder eingebetteten Schriftart in die Ausgabe-PDF einzubetten.
// Die Größe des Dokuments kann sehr groß werden, aber wir können alle Schriftarten vollständig nutzen, wenn wir das PDF bearbeiten.
// Setzen Sie die Eigenschaft „EmbedFullFonts“ auf „false“, um die Teilmenge auf Schriftarten anzuwenden und nur die Glyphen zu speichern
// dass das Dokument verwendet. Die Datei wird erheblich kleiner,
// aber wir benötigen möglicherweise Zugriff auf benutzerdefinierte Schriftarten, wenn wir das Dokument bearbeiten.
options.EmbedFullFonts = embedFullFonts;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmbedFullFonts.pdf", options);

if (embedFullFonts)
    Assert.That(500000, Is.LessThan(new FileInfo(ArtifactsDir + "PdfSaveOptions.EmbedFullFonts.pdf").Length));
else
    Assert.That(25000, Is.AtLeast(new FileInfo(ArtifactsDir + "PdfSaveOptions.EmbedFullFonts.pdf").Length));

// Die ursprünglichen Schriftartquellen wiederherstellen.
FontSettings.DefaultInstance.SetFontsSources(originalFontsSources);
```

### Siehe auch

* class [PdfSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
