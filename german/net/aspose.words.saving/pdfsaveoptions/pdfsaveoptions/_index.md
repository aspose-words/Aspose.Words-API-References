---
title: PdfSaveOptions
linktitle: PdfSaveOptions
articleTitle: PdfSaveOptions
second_title: Aspose.Words für .NET
description: Entdecken Sie den Konstruktor PdfSaveOptions, mit dem Sie Ihre Dokumente mühelos initialisieren und im hochwertigen PDF-Format speichern können. Optimieren Sie Ihren Workflow noch heute!
type: docs
weight: 10
url: /de/net/aspose.words.saving/pdfsaveoptions/pdfsaveoptions/
---
## PdfSaveOptions constructor

Initialisiert eine neue Instanz dieser Klasse, die zum Speichern eines Dokuments im verwendet werden kann.Pdf format.

```csharp
public PdfSaveOptions()
```

## Beispiele

Zeigt, wie Sie beim Einbetten von Schriftarten beim Rendern eines Dokuments in PDF die Untergruppenfunktion aktivieren oder deaktivieren.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Arvo";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Konfigurieren Sie unsere Schriftartquellen, um sicherzustellen, dass wir auf beide Schriftarten in diesem Dokument zugreifen können.
FontSourceBase[] originalFontsSources = FontSettings.DefaultInstance.GetFontsSources();
Aspose.Words.Fonts.FolderFontSource folderFontSource =
    new Aspose.Words.Fonts.FolderFontSource(FontsDir, true);
FontSettings.DefaultInstance.SetFontsSources(new[] { originalFontsSources[0], folderFontSource });

FontSourceBase[] fontSources = FontSettings.DefaultInstance.GetFontsSources();
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(fontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

// Erstellen Sie ein "PdfSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions options = new PdfSaveOptions();

// Da unser Dokument eine benutzerdefinierte Schriftart enthält, kann eine Einbettung in das Ausgabedokument wünschenswert sein.
// Setzen Sie die Eigenschaft „EmbedFullFonts“ auf „true“, um jedes Glyph jeder eingebetteten Schriftart in das Ausgabe-PDF einzubetten.
// Das Dokument kann sehr groß werden, aber wir können alle Schriftarten vollständig nutzen, wenn wir das PDF bearbeiten.
// Setzen Sie die Eigenschaft „EmbedFullFonts“ auf „false“, um eine Untergruppe auf Schriftarten anzuwenden und nur die Glyphen zu speichern
// die das Dokument verwendet. Die Datei wird deutlich kleiner sein,
// aber wir benötigen möglicherweise Zugriff auf benutzerdefinierte Schriftarten, wenn wir das Dokument bearbeiten.
options.EmbedFullFonts = embedFullFonts;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmbedFullFonts.pdf", options);

// Stellen Sie die ursprünglichen Schriftartquellen wieder her.
FontSettings.DefaultInstance.SetFontsSources(originalFontsSources);
```

### Siehe auch

* class [PdfSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
