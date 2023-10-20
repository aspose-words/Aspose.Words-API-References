---
title: PdfSaveOptions.FontEmbeddingMode
linktitle: FontEmbeddingMode
articleTitle: FontEmbeddingMode
second_title: Aspose.Words für .NET
description: PdfSaveOptions FontEmbeddingMode eigendom. Gibt den Schriftarteinbettungsmodus an in C#.
type: docs
weight: 170
url: /de/net/aspose.words.saving/pdfsaveoptions/fontembeddingmode/
---
## PdfSaveOptions.FontEmbeddingMode property

Gibt den Schriftarteinbettungsmodus an.

```csharp
public PdfFontEmbeddingMode FontEmbeddingMode { get; set; }
```

## Bemerkungen

Der Standardwert istEmbedAll.

Diese Einstellung funktioniert nur für Text in ANSI-Codierung (Windows-1252). Wenn das Dokument Nicht-ANSI-Text enthält, werden die entsprechenden Schriftarten unabhängig von dieser Einstellung eingebettet.

Für die PDF/A- und PDF/UA-Konformität müssen alle Schriftarten eingebettet sein. EmbedAll Der Wert wird beim Speichern in PDF/A und PDF/UA automatisch verwendet.

## Beispiele

Zeigt, wie man Aspose.Words so einstellt, dass das Einbetten der Schriftarten Arial und Times New Roman in ein PDF-Dokument übersprungen wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// „Arial“ ist eine Standardschriftart und „Courier New“ ist eine Nichtstandardschriftart.
builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Courier New";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Erstellen Sie ein „PdfSaveOptions“-Objekt, das wir an die „Save“-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions options = new PdfSaveOptions();

// Setzen Sie die Eigenschaft „EmbedFullFonts“ auf „true“, um jedes Glyph jeder eingebetteten Schriftart in die Ausgabe-PDF einzubetten.
options.EmbedFullFonts = true;

// Setzen Sie die Eigenschaft „FontEmbeddingMode“ auf „EmbedAll“, um alle Schriftarten in die Ausgabe-PDF einzubetten.
// Setzen Sie die Eigenschaft „FontEmbeddingMode“ auf „EmbedNonstandard“, um nur die Einbettung nicht standardmäßiger Schriftarten in die Ausgabe-PDF zuzulassen.
// Setzen Sie die Eigenschaft „FontEmbeddingMode“ auf „EmbedNone“, um keine Schriftarten in die Ausgabe-PDF einzubetten.
options.FontEmbeddingMode = pdfFontEmbeddingMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmbedWindowsFonts.pdf", options);

switch (pdfFontEmbeddingMode)
{
    case PdfFontEmbeddingMode.EmbedAll:
        Assert.That(1000000, Is.LessThan(new FileInfo(ArtifactsDir + "PdfSaveOptions.EmbedWindowsFonts.pdf").Length));
        break;
    case PdfFontEmbeddingMode.EmbedNonstandard:
        Assert.That(480000, Is.LessThan(new FileInfo(ArtifactsDir + "PdfSaveOptions.EmbedWindowsFonts.pdf").Length));
        break;
    case PdfFontEmbeddingMode.EmbedNone:
        Assert.That(4255, Is.AtLeast(new FileInfo(ArtifactsDir + "PdfSaveOptions.EmbedWindowsFonts.pdf").Length));
        break;
}
```

### Siehe auch

* enum [PdfFontEmbeddingMode](../../pdffontembeddingmode/)
* class [PdfSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
