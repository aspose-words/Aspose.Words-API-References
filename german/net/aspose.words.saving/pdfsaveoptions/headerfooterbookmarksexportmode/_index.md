---
title: PdfSaveOptions.HeaderFooterBookmarksExportMode
linktitle: HeaderFooterBookmarksExportMode
articleTitle: HeaderFooterBookmarksExportMode
second_title: Aspose.Words für .NET
description: PdfSaveOptions HeaderFooterBookmarksExportMode eigendom. Legt fest wie Lesezeichen in Kopf/Fußzeilen exportiert werden in C#.
type: docs
weight: 180
url: /de/net/aspose.words.saving/pdfsaveoptions/headerfooterbookmarksexportmode/
---
## PdfSaveOptions.HeaderFooterBookmarksExportMode property

Legt fest, wie Lesezeichen in Kopf-/Fußzeilen exportiert werden.

```csharp
public HeaderFooterBookmarksExportMode HeaderFooterBookmarksExportMode { get; set; }
```

## Bemerkungen

Der Standardwert istAll.

Diese Eigenschaft wird in Verbindung mit verwendet[`OutlineOptions`](../outlineoptions/) Möglichkeit.

## Beispiele

Zeigt an, dass Lesezeichen in Kopf-/Fußzeilen in einem Dokument verarbeitet werden, das wir als PDF rendern.

```csharp
Document doc = new Document(MyDir + "Bookmarks in headers and footers.docx");

// Erstellen Sie ein „PdfSaveOptions“-Objekt, das wir an die „Save“-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Setzen Sie die Eigenschaft „PageMode“ auf „PdfPageMode.UseOutlines“, um den Gliederungsnavigationsbereich im Ausgabe-PDF anzuzeigen.
saveOptions.PageMode = PdfPageMode.UseOutlines;

// Setzen Sie die Eigenschaft „DefaultBookmarksOutlineLevel“ auf „1“, um alle anzuzeigen
// Lesezeichen auf der ersten Ebene der Gliederung im Ausgabe-PDF.
saveOptions.OutlineOptions.DefaultBookmarksOutlineLevel = 1;

// Setzen Sie die Eigenschaft „HeaderFooterBookmarksExportMode“ auf „HeaderFooterBookmarksExportMode.None“.
// keine Lesezeichen exportieren, die sich in Kopf-/Fußzeilen befinden.
// Setzen Sie die Eigenschaft „HeaderFooterBookmarksExportMode“ auf „HeaderFooterBookmarksExportMode.First“.
// Exportiert nur Lesezeichen in der Kopf-/Fußzeile des ersten Abschnitts.
// Setzen Sie die Eigenschaft „HeaderFooterBookmarksExportMode“ auf „HeaderFooterBookmarksExportMode.All“.
// Lesezeichen exportieren, die in allen Kopf-/Fußzeilen enthalten sind.
saveOptions.HeaderFooterBookmarksExportMode = headerFooterBookmarksExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.HeaderFooterBookmarksExportMode.pdf", saveOptions);
```

### Siehe auch

* enum [HeaderFooterBookmarksExportMode](../../headerfooterbookmarksexportmode/)
* class [PdfSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
