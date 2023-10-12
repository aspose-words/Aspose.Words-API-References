---
title: Enum PdfFontEmbeddingMode
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Saving.PdfFontEmbeddingMode opsomming. Gibt an wie Aspose.Words Schriftarten einbetten soll.
type: docs
weight: 5470
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
| EmbedNonstandard | `1` | Aspose.Words bettet alle Schriftarten mit Ausnahme der Standard-Windows-Schriftarten Arial und Times New Roman ein. In diesem Modus sind nur die Schriftarten Arial und Times New Roman betroffen, da MS Word beim Speichern des Dokuments als PDF nicht nur diese Schriftarten einbettet . |
| EmbedNone | `2` | Aspose.Words bindet keine Schriftarten ein. |

### Beispiele

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

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)


