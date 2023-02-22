---
title: Enum PdfFontEmbeddingMode
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Saving.PdfFontEmbeddingMode opsomming. Gibt an wie Aspose.Words Schriftarten einbetten soll.
type: docs
weight: 5190
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
| EmbedNonstandard | `1` | Aspose.Words bettet alle Schriftarten mit Ausnahme der Standard-Windows-Schriftarten Arial und Times New Roman ein. Nur Arial- und Times New Roman-Schriftarten sind in diesem Modus betroffen, da MS Word nicht nur diese Schriftarten einbettet , wenn das Dokument als PDF gespeichert wird. |
| EmbedNone | `2` | Aspose.Words bettet keine Schriftarten ein. |

### Beispiele

Zeigt, wie Aspose.Words so eingestellt wird, dass das Einbetten von Arial- und Times New Roman-Schriftarten in ein PDF-Dokument übersprungen wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// "Arial" ist eine Standardschriftart und "Courier New" ist eine Nicht-Standardschriftart.
builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Courier New";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Erstellen Sie ein "PdfSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions options = new PdfSaveOptions();

// Setzen Sie die Eigenschaft "EmbedFullFonts" auf "true", um jede Glyphe jeder eingebetteten Schriftart in die Ausgabe-PDF einzubetten.
options.EmbedFullFonts = true;

// Legen Sie die Eigenschaft „FontEmbeddingMode“ auf „EmbedAll“ fest, um alle Schriftarten in die Ausgabe-PDF einzubetten.
// Legen Sie die Eigenschaft „FontEmbeddingMode“ auf „EmbedNonstandard“ fest, um nur das Einbetten von nicht standardmäßigen Schriftarten in die Ausgabe-PDF zuzulassen.
// Legen Sie die Eigenschaft „FontEmbeddingMode“ auf „EmbedNone“ fest, um keine Schriftarten in die Ausgabe-PDF einzubetten.
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
        Assert.That(4217, Is.AtLeast(new FileInfo(ArtifactsDir + "PdfSaveOptions.EmbedWindowsFonts.pdf").Length));
        break;
}
```

### Siehe auch

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)


