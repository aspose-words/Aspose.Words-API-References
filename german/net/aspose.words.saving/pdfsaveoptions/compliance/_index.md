---
title: PdfSaveOptions.Compliance
linktitle: Compliance
articleTitle: Compliance
second_title: Aspose.Words für .NET
description: Entdecken Sie die Compliance-Eigenschaft von PdfSaveOptions, um sicherzustellen, dass Ihre PDF-Dokumente den Industriestandards für Qualität und Kompatibilität entsprechen.
type: docs
weight: 50
url: /de/net/aspose.words.saving/pdfsaveoptions/compliance/
---
## PdfSaveOptions.Compliance property

Gibt den Konformitätsgrad mit PDF-Standards für Ausgabedokumente an.

```csharp
public PdfCompliance Compliance { get; set; }
```

## Bemerkungen

Standard istPdf17.

## Beispiele

Zeigt, wie die Konformitätsstufe mit PDF-Standards für gespeicherte PDF-Dokumente festgelegt wird.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Erstellen Sie ein "PdfSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
// Beachten Sie, dass einige PdfSaveOptions beim Speichern in einem der Standards verboten und automatisch behoben sind.
// Verwenden Sie IWarningCallback, um zu erfahren, welche Optionen automatisch behoben werden.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Setzen Sie die Eigenschaft „Compliance“ auf „PdfCompliance.PdfA1b“, um dem Standard „PDF/A-1b“ zu entsprechen.
// Ziel ist es, das visuelle Erscheinungsbild des Dokuments beizubehalten, während Aspose.Words es in PDF konvertiert.
// Setzen Sie die Eigenschaft „Compliance“ auf „PdfCompliance.Pdf17“, um dem Standard „1.7“ zu entsprechen.
// Setzen Sie die Eigenschaft „Compliance“ auf „PdfCompliance.PdfA1a“, um dem Standard „PDF/A-1a“ zu entsprechen.
// das „PDF/A-1b“ entspricht und gleichzeitig die Dokumentstruktur des Originaldokuments beibehält.
// Setzen Sie die Eigenschaft „Compliance“ auf „PdfCompliance.PdfUa1“, um dem Standard „PDF/UA-1“ (ISO 14289-1) zu entsprechen.
// Ziel ist die Darstellung elektronischer Dokumente im PDF-Format, die den Zugriff auf die Datei ermöglicht.
// Setzen Sie die Eigenschaft „Compliance“ auf „PdfCompliance.Pdf20“, um dem Standard „PDF 2.0“ (ISO 32000-2) zu entsprechen.
// Setzen Sie die Eigenschaft „Compliance“ auf „PdfCompliance.PdfA4“, um dem Standard „PDF/A-4“ (ISO 19004:2020) zu entsprechen,
// wodurch das statische visuelle Erscheinungsbild des Dokuments im Laufe der Zeit erhalten bleibt.
// Setzen Sie die Eigenschaft „Compliance“ auf „PdfCompliance.PdfA4Ua2“, um sowohl PDF/A-4 (ISO 19005-4:2020) als auch PDF/A-4 (ISO 19005-4:2020) zu erfüllen.
// und PDF/UA-2 (ISO 14289-2:2024)-Standards.
// Setzen Sie die Eigenschaft „Compliance“ auf „PdfCompliance.PdfUa2“, um dem Standard PDF/UA-2 (ISO 14289-2:2024) zu entsprechen.
// Dies trägt dazu bei, Dokumente durchsuchbar zu machen, kann aber die Größe bereits großer Dokumente erheblich erhöhen.
saveOptions.Compliance = pdfCompliance;

doc.Save(ArtifactsDir + "PdfSaveOptions.Compliance.pdf", saveOptions);
```

### Siehe auch

* enum [PdfCompliance](../../pdfcompliance/)
* class [PdfSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
