---
title: PdfCompliance Enum
linktitle: PdfCompliance
articleTitle: PdfCompliance
second_title: Aspose.Words für .NET
description: Entdecken Sie die Enumeration Aspose.Words.Saving.PdfCompliance, um die Einhaltung Ihrer PDF-Standards zu verbessern. Steigern Sie die Dokumentqualität mit maßgeschneiderten Optionen für jeden Bedarf!
type: docs
weight: 6200
url: /de/net/aspose.words.saving/pdfcompliance/
---
## PdfCompliance enumeration

Gibt den Grad der Konformität mit PDF-Standards an.

```csharp
public enum PdfCompliance
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Pdf17 | `0` | Die Ausgabedatei entspricht dem Standard PDF 1.7 (ISO 32000-1). |
| Pdf20 | `1` | Die Ausgabedatei entspricht dem PDF 2.0-Standard (ISO 32000-2). |
| PdfA1a | `2` | Die Ausgabedatei entspricht dem Standard PDF/A-1a (ISO 19005-1). Diese Ebene umfasst alle Anforderungen von PDF/A-1b und erfordert zusätzlich die Einbeziehung der Dokumentstruktur (auch als „Tagging“ bezeichnet), um sicherzustellen, dass Dokumentinhalte durchsucht und wiederverwendet werden können. |
| PdfA1b | `3` | Die Ausgabedatei entspricht dem Standard PDF/A-1b (ISO 19005-1). PDF/A-1b hat das Ziel, eine zuverlässige Reproduktion des visuellen Erscheinungsbilds des Dokuments zu gewährleisten. |
| PdfA2a | `4` | Die Ausgabedatei entspricht dem Standard PDF/A-2a (ISO 19005-2). Diese Ebene umfasst alle Anforderungen von PDF/A-2u und erfordert zusätzlich die Einbeziehung der Dokumentstruktur (auch als „Tagging“ bezeichnet), um sicherzustellen, dass Dokumentinhalte durchsucht und wiederverwendet werden können. |
| PdfA2u | `5` | Die Ausgabedatei entspricht dem PDF/A-2u-Standard (ISO 19005-2). PDF/A-2u hat das Ziel, das statische Erscheinungsbild von Dokumenten langfristig zu erhalten, unabhängig von den zum Erstellen, Speichern oder Rendern der Dateien verwendeten Werkzeugen und Systemen. Darüber hinaus kann der im Dokument enthaltene Text zuverlässig als eine Reihe von Unicode-Codepunkten extrahiert werden. |
| PdfA3a | `6` | Die Ausgabedatei entspricht dem Standard PDF/A-3a (ISO 19005-3). Diese Ebene umfasst alle Anforderungen von PDF/A-3u und erfordert zusätzlich die Einbeziehung der Dokumentstruktur (auch als „Tagging“ bezeichnet), um sicherzustellen, dass Dokumentinhalte durchsucht und wiederverwendet werden können. |
| PdfA3u | `7` | Die Ausgabedatei entspricht dem PDF/A-3u-Standard (ISO 19005-3). PDF/A-3u (ebenso wie PDF/A-2u) verfolgt das Ziel, das statische Erscheinungsbild von Dokumenten langfristig zu erhalten, unabhängig von den zum Erstellen, Speichern oder Rendern der Dateien verwendeten Werkzeugen und Systemen. Darüber hinaus kann der im Dokument enthaltene Text zuverlässig als Reihe von Unicode-Codepunkten extrahiert werden. Neben PDF/A-2u ermöglicht PDF/A-3u das Einbetten von Anhängen in das PDF-Dokument. |
| PdfA4 | `8` | Die Ausgabedatei entspricht dem PDF/A-4-Standard (ISO 19005-4:2020). PDF/A-4 hat das Ziel, das statische Erscheinungsbild von Dokumenten langfristig zu erhalten, unabhängig von den zum Erstellen, Speichern oder Rendern der Dateien verwendeten Tools und Systemen. Darüber hinaus kann der im Dokument enthaltene Text zuverlässig als Reihe von Unicode-Codepunkten extrahiert werden. |
| PdfA4f | `9` | Die Ausgabedatei entspricht dem Standard PDF/A-4f (ISO 19005-4:2020). Diese Ebene umfasst alle Anforderungen von PDF/A-4 und ermöglicht zusätzlich das Einbetten von Anhängen in das PDF-Dokument. |
| PdfA4Ua2 | `10` | Die Ausgabedatei entspricht sowohl den Standards PDF/A-4 (ISO 19005-4:2020) als auch PDF/UA-2 (ISO 14289-2:2024). PDF/A-4 hat das Ziel, das statische Erscheinungsbild von Dokumenten langfristig zu erhalten, unabhängig von den zum Erstellen, Speichern oder Rendern der Dateien verwendeten Tools und Systemen. Der Hauptzweck von PDF/UA besteht darin, zu definieren, wie elektronische Dokumente im PDF-Format barrierefrei dargestellt werden. |
| PdfUa1 | `11` | Die Ausgabedatei entspricht dem Standard PDF/UA-1 (ISO 14289-1). Der Hauptzweck von PDF/UA besteht darin, zu definieren, wie elektronische Dokumente im PDF-Format auf eine Weise dargestellt werden, die die Zugänglichkeit der Datei ermöglicht. |
| PdfUa2 | `12` | Die Ausgabedatei entspricht dem Standard PDF/UA-2 (ISO 14289-2:2024). Der Hauptzweck von PDF/UA besteht darin, zu definieren, wie elektronische Dokumente im PDF-Format auf eine Weise dargestellt werden, die die Zugänglichkeit der Datei ermöglicht. |

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

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
