---
title: PdfFontEmbeddingMode Enum
linktitle: PdfFontEmbeddingMode
articleTitle: PdfFontEmbeddingMode
second_title: Aspose.Words für .NET
description: Entdecken Sie die Enumeration Aspose.Words.PdfFontEmbeddingMode für die optimale Einbettung von Schriftarten in PDFs. Verbessern Sie die Dokumentqualität und sorgen Sie für eine konsistente Textanzeige.
type: docs
weight: 6260
url: /de/net/aspose.words.saving/pdffontembeddingmode/
---
## PdfFontEmbeddingMode enumeration

Gibt an, wie Aspose.Words Schriftarten einbetten soll.

```csharp
public enum PdfFontEmbeddingMode
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| EmbedAll | `0` | Aspose.Words bettet alle Schriftarten ein. |
| EmbedNonstandard | `1` | Aspose.Words bettet alle Schriftarten außer den Standard-Windows-Schriftarten Arial und Times New Roman ein. In diesem Modus sind nur die Schriftarten Arial und Times New Roman betroffen, da MS Word beim Speichern des Dokuments im PDF-Format nicht nur diese Schriftarten einbettet. |
| EmbedNone | `2` | Aspose.Words bettet keine Schriftarten ein. |

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

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
