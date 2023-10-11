---
title: PdfSaveOptions.Compliance
second_title: Aspose.Words für .NET-API-Referenz
description: PdfSaveOptions eigendom. Gibt den Konformitätsgrad der PDFStandards für Ausgabedokumente an.
type: docs
weight: 40
url: /de/net/aspose.words.saving/pdfsaveoptions/compliance/
---
## PdfSaveOptions.Compliance property

Gibt den Konformitätsgrad der PDF-Standards für Ausgabedokumente an.

```csharp
public PdfCompliance Compliance { get; set; }
```

### Bemerkungen

Standard istPdf17.

### Beispiele

Zeigt, wie Sie den Konformitätsgrad der PDF-Standards für gespeicherte PDF-Dokumente festlegen.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Erstellen Sie ein „PdfSaveOptions“-Objekt, das wir an die „Save“-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
// Beachten Sie, dass einige PdfSaveOptions beim Speichern nach einem der Standards verboten sind und automatisch behoben werden.
// Verwenden Sie IWarningCallback, um zu erfahren, welche Optionen automatisch behoben werden.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Setzen Sie die Eigenschaft „Compliance“ auf „PdfCompliance.PdfA1b“, um dem Standard „PDF/A-1b“ zu entsprechen.
// Ziel ist es, das visuelle Erscheinungsbild des Dokuments beizubehalten, während Aspose.Words es in PDF konvertiert.
// Setzen Sie die Eigenschaft „Compliance“ auf „PdfCompliance.Pdf17“, um dem Standard „1.7“ zu entsprechen.
// Setzen Sie die Eigenschaft „Compliance“ auf „PdfCompliance.PdfA1a“, um dem Standard „PDF/A-1a“ zu entsprechen.
// das „PDF/A-1b“ entspricht und die Dokumentstruktur des Originaldokuments beibehält.
// Setzen Sie die Eigenschaft „Compliance“ auf „PdfCompliance.PdfUa1“, um dem Standard „PDF/UA-1“ (ISO 14289-1) zu entsprechen.
// Ziel ist es, elektronische Dokumente im PDF-Format darzustellen, die den Zugriff auf die Datei ermöglichen.
// Setzen Sie die Eigenschaft „Compliance“ auf „PdfCompliance.Pdf20“, um dem Standard „PDF 2.0“ (ISO 32000-2) zu entsprechen.
// Setzen Sie die Eigenschaft „Compliance“ auf „PdfCompliance.PdfA4“, um dem Standard „PDF/A-4“ (ISO 19004:2020) zu entsprechen.
// wodurch das statische visuelle Erscheinungsbild des Dokuments im Laufe der Zeit erhalten bleibt.
// Dies hilft dabei, Dokumente durchsuchbar zu machen, kann jedoch die Größe bereits großer Dokumente erheblich erhöhen.
saveOptions.Compliance = pdfCompliance;

doc.Save(ArtifactsDir + "PdfSaveOptions.Compliance.pdf", saveOptions);
```

### Siehe auch

* enum [PdfCompliance](../../pdfcompliance/)
* class [PdfSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../pdfsaveoptions/)
* Montage [Aspose.Words](../../../)


