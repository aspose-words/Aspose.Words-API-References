---
title: PdfCompliance Enum
linktitle: PdfCompliance
articleTitle: PdfCompliance
second_title: Aspose.Words für .NET
description: Aspose.Words.Saving.PdfCompliance opsomming. Gibt den Konformitätsgrad der PDFStandards an in C#.
type: docs
weight: 5410
url: /de/net/aspose.words.saving/pdfcompliance/
---
## PdfCompliance enumeration

Gibt den Konformitätsgrad der PDF-Standards an.

```csharp
public enum PdfCompliance
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Pdf17 | `0` | Die Ausgabedatei entspricht dem Standard PDF 1.7 (ISO 32000-1). |
| Pdf20 | `1` | Die Ausgabedatei entspricht dem Standard PDF 2.0 (ISO 32000-2). |
| PdfA1a | `2` | Die Ausgabedatei entspricht dem Standard PDF/A-1a (ISO 19005-1). Diese Stufe umfasst alle Anforderungen von PDF/A-1b und erfordert zusätzlich , dass die Dokumentstruktur enthalten ist (auch als „getaggt“ bezeichnet). ), mit dem Ziel sicherzustellen, dass Dokumentinhalte durchsucht und wiederverwendet werden können. |
| PdfA1b | `3` | Die Ausgabedatei entspricht dem Standard PDF/A-1b (ISO 19005-1). PDF/A-1b hat das Ziel, eine zuverlässige Reproduktion des visuellen Erscheinungsbilds des Dokuments sicherzustellen. |
| PdfA2a | `4` | Die Ausgabedatei entspricht dem Standard PDF/A-2a (ISO 19005-2). Diese Stufe umfasst alle Anforderungen von PDF/A-2u und erfordert zusätzlich , dass die Dokumentstruktur enthalten ist (auch als „getaggt“ bezeichnet). ), mit dem Ziel sicherzustellen, dass Dokumentinhalte durchsucht und wiederverwendet werden können. |
| PdfA2u | `5` | Die Ausgabedatei entspricht dem Standard PDF/A-2u (ISO 19005-2). PDF/A-2u hat das Ziel, das statische visuelle Erscheinungsbild des Dokuments über die Zeit hinweg beizubehalten, unabhängig von den zum Erstellen und Speichern verwendeten Tools und Systemen oder Rendern der Dateien. Darüber hinaus kann jeder im Dokument enthaltene Text zuverlässig als eine Reihe von Unicode-Codepunkten extrahiert werden. |
| PdfA4 | `6` | Die Ausgabedatei entspricht dem Standard PDF/A-4 (ISO 19005-4:2020). PDF/A-4 hat das Ziel, das statische visuelle Erscheinungsbild des Dokuments über einen längeren Zeitraum hinweg beizubehalten, unabhängig von den für die Erstellung verwendeten Tools und Systemen , Speichern oder Rendern der Dateien. Darüber hinaus kann jeder im Dokument enthaltene Text zuverlässig als eine Reihe von Unicode-Codepunkten extrahiert werden. |
| PdfUa1 | `7` | Die Ausgabedatei entspricht dem Standard PDF/UA-1 (ISO 14289-1). Der Hauptzweck von PDF/UA besteht darin, zu definieren, wie elektronische Dokumente im PDF-Format auf eine Weise dargestellt werden sollen, die es der Datei ermöglicht zugänglich. |

## Beispiele

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

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
