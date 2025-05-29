---
title: PdfSaveOptions.PageMode
linktitle: PageMode
articleTitle: PageMode
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die PageMode-Eigenschaft von PdfSaveOptions Ihr PDF-Anzeigeerlebnis verbessert, indem Sie die Dokumentanzeige in jedem PDF-Reader anpassen.
type: docs
weight: 260
url: /de/net/aspose.words.saving/pdfsaveoptions/pagemode/
---
## PdfSaveOptions.PageMode property

Gibt an, wie das PDF-Dokument angezeigt werden soll, wenn es in einem PDF-Reader geöffnet wird.

```csharp
public PdfPageMode PageMode { get; set; }
```

## Bemerkungen

Der Standardwert istUseOutlines .

## Beispiele

Zeigt, wie Sie für einige PDF-Reader Anweisungen festlegen, die beim Öffnen eines Ausgabedokuments befolgt werden sollen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Erstellen Sie ein "PdfSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions options = new PdfSaveOptions();

// Setzen Sie die Eigenschaft „PageMode“ auf „PdfPageMode.FullScreen“, damit der PDF-Reader die gespeicherte
// Dokument im Vollbildmodus, der die Anzeige des Monitors übernimmt und keine sichtbaren Steuerelemente hat.
// Setzen Sie die Eigenschaft „PageMode“ auf „PdfPageMode.UseThumbs“, damit der PDF-Reader ein separates Panel anzeigt
// mit einer Miniaturansicht für jede Seite im Dokument.
// Setzen Sie die Eigenschaft „PageMode“ auf „PdfPageMode.UseOC“, damit der PDF-Reader ein separates Panel anzeigt
// Dadurch können wir mit allen im Dokument vorhandenen Ebenen arbeiten.
// Setzen Sie die Eigenschaft "PageMode" auf "PdfPageMode.UseOutlines", um den PDF-Reader zu erhalten
// auch um die Gliederung anzuzeigen, wenn möglich.
// Setzen Sie die Eigenschaft „PageMode“ auf „PdfPageMode.UseNone“, damit der PDF-Reader nur das Dokument selbst anzeigt.
// Setzen Sie die Eigenschaft „PageMode“ auf „PdfPageMode.UseAttachments“, um das Anhängefenster sichtbar zu machen.
options.PageMode = pageMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.PageMode.pdf", options);
```

Zeigt die Verarbeitung von Lesezeichen in Kopf-/Fußzeilen in einem Dokument, das wir in PDF rendern.

```csharp
Document doc = new Document(MyDir + "Bookmarks in headers and footers.docx");

// Erstellen Sie ein "PdfSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Setzen Sie die Eigenschaft „PageMode“ auf „PdfPageMode.UseOutlines“, um den Gliederungsnavigationsbereich im Ausgabe-PDF anzuzeigen.
saveOptions.PageMode = PdfPageMode.UseOutlines;

// Setzen Sie die Eigenschaft "DefaultBookmarksOutlineLevel" auf "1", um alle
// Lesezeichen auf der ersten Ebene der Gliederung im Ausgabe-PDF.
saveOptions.OutlineOptions.DefaultBookmarksOutlineLevel = 1;

// Setzen Sie die Eigenschaft "HeaderFooterBookmarksExportMode" auf "HeaderFooterBookmarksExportMode.None" auf
// keine Lesezeichen exportieren, die sich in Kopf-/Fußzeilen befinden.
// Setzen Sie die Eigenschaft "HeaderFooterBookmarksExportMode" auf "HeaderFooterBookmarksExportMode.First" auf
// Exportiere nur Lesezeichen in der Kopf-/Fußzeile des ersten Abschnitts.
// Setzen Sie die Eigenschaft "HeaderFooterBookmarksExportMode" auf "HeaderFooterBookmarksExportMode.All" auf
// Lesezeichen exportieren, die in allen Kopf-/Fußzeilen enthalten sind.
saveOptions.HeaderFooterBookmarksExportMode = headerFooterBookmarksExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.HeaderFooterBookmarksExportMode.pdf", saveOptions);
```

### Siehe auch

* enum [PdfPageMode](../../pdfpagemode/)
* class [PdfSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
