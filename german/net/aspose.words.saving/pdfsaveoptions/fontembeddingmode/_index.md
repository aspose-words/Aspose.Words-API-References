---
title: PdfSaveOptions.FontEmbeddingMode
linktitle: FontEmbeddingMode
articleTitle: FontEmbeddingMode
second_title: Aspose.Words für .NET
description: Entdecken Sie die FontEmbeddingMode-Eigenschaft von PdfSaveOptions, um die Schriftarteinbettung Ihrer PDF-Datei zu optimieren. Verbessern Sie mühelos die Dokumentqualität und Kompatibilität!
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

Diese Einstellung funktioniert nur für Text in ANSI-Kodierung (Windows-1252). Enthält das Dokument nicht-ANSI-Text, werden die entsprechenden Schriftarten unabhängig von dieser Einstellung eingebettet.

Die PDF/A- und PDF/UA-Konformität erfordert die Einbettung aller Schriftarten. EmbedAll Der Wert wird beim Speichern in PDF/A und PDF/UA automatisch verwendet.

## Beispiele

Zeigt, wie Aspose.Words so eingestellt wird, dass das Einbetten der Schriftarten Arial und Times New Roman in ein PDF-Dokument übersprungen wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// „Arial“ ist eine Standardschriftart und „Courier New“ ist eine Nicht-Standardschriftart.
builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Courier New";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Erstellen Sie ein "PdfSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions options = new PdfSaveOptions();
// Setzen Sie die Eigenschaft „EmbedFullFonts“ auf „true“, um jedes Glyph jeder eingebetteten Schriftart in das Ausgabe-PDF einzubetten.
options.EmbedFullFonts = true;
// Setzen Sie die Eigenschaft „FontEmbeddingMode“ auf „EmbedAll“, um alle Schriftarten in das Ausgabe-PDF einzubetten.
// Setzen Sie die Eigenschaft „FontEmbeddingMode“ auf „EmbedNonstandard“, um nur das Einbetten nicht standardmäßiger Schriftarten in das Ausgabe-PDF zuzulassen.
// Setzen Sie die Eigenschaft „FontEmbeddingMode“ auf „EmbedNone“, um keine Schriftarten in das Ausgabe-PDF einzubetten.
options.FontEmbeddingMode = pdfFontEmbeddingMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmbedWindowsFonts.pdf", options);
```

### Siehe auch

* enum [PdfFontEmbeddingMode](../../pdffontembeddingmode/)
* class [PdfSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
