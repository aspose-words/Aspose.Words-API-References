---
title: PdfSaveOptions.Compliance
second_title: Aspose.Words für .NET-API-Referenz
description: PdfSaveOptions eigendom. Gibt die Konformitätsstufe des PDFStandards für Ausgabedokumente an.
type: docs
weight: 30
url: /de/net/aspose.words.saving/pdfsaveoptions/compliance/
---
## PdfSaveOptions.Compliance property

Gibt die Konformitätsstufe des PDF-Standards für Ausgabedokumente an.

```csharp
public PdfCompliance Compliance { get; set; }
```

### Bemerkungen

Standard istPdf17.

### Beispiele

Zeigt, wie Sie die Konformitätsstufe für PDF-Standards gespeicherter PDF-Dokumente festlegen.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Erstellen Sie ein "PdfSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
// Beachten Sie, dass einige PdfSaveOptions beim Speichern in einem der Standards verboten und automatisch behoben werden.
// Verwenden Sie IWarningCallback, um zu erfahren, welche Optionen automatisch behoben werden.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Legen Sie die Eigenschaft „Compliance“ auf „PdfCompliance.PdfA1b“ fest, um dem „PDF/A-1b“-Standard zu entsprechen,
// was darauf abzielt, das visuelle Erscheinungsbild des Dokuments beizubehalten, während Aspose.Words es in PDF konvertiert.
// Legen Sie die Eigenschaft „Compliance“ auf „PdfCompliance.Pdf17“ fest, um dem „1.7“-Standard zu entsprechen.
// Legen Sie die Eigenschaft „Compliance“ auf „PdfCompliance.PdfA1a“ fest, um dem „PDF/A-1a“-Standard zu entsprechen,
// die "PDF/A-1b" entspricht und die Dokumentstruktur des Originaldokuments beibehält.
// Legen Sie die Eigenschaft "Compliance" auf "PdfCompliance.PdfUa1" fest, um dem Standard "PDF/UA-1" (ISO 14289-1) zu entsprechen,
// die darauf abzielt, elektronische Dokumente in PDF darzustellen, die den Zugriff auf die Datei ermöglichen.
// Dies hilft dabei, Dokumente durchsuchbar zu machen, kann aber die Größe bereits großer Dokumente erheblich erhöhen.
saveOptions.Compliance = pdfCompliance;

doc.Save(ArtifactsDir + "PdfSaveOptions.Compliance.pdf", saveOptions);
```

### Siehe auch

* enum [PdfCompliance](../../pdfcompliance/)
* class [PdfSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../pdfsaveoptions/)
* Montage [Aspose.Words](../../../)


