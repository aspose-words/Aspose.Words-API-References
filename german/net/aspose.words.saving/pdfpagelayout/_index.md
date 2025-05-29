---
title: PdfPageLayout Enum
linktitle: PdfPageLayout
articleTitle: PdfPageLayout
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aufzählung Aspose.Words.Saving.PdfPageLayout für eine optimale PDF-Anzeige. Passen Sie Seitenlayouts für eine verbesserte Lesbarkeit in jedem PDF-Reader an.
type: docs
weight: 6290
url: /de/net/aspose.words.saving/pdfpagelayout/
---
## PdfPageLayout enumeration

Gibt das Seitenlayout an, das verwendet werden soll, wenn das Dokument in einem PDF-Reader geöffnet wird.

```csharp
public enum PdfPageLayout
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| SinglePage | `0` | Zeigt jeweils nur eine Seite an. |
| OneColumn | `1` | Die Seiten in einer Spalte anzeigen. |
| TwoColumnLeft | `2` | Zeigen Sie die Seiten in zwei Spalten an, mit den ungeraden Seitenzahlen auf der linken Seite. |
| TwoColumnRight | `3` | Zeigen Sie die Seiten in zwei Spalten an, mit den ungeraden Seitenzahlen auf der rechten Seite. |
| TwoPageLeft | `4` | Zeigen Sie die Seiten paarweise an, mit den ungeraden Seitennummern links. |
| TwoPageRight | `5` | Zeigen Sie die Seiten paarweise an, mit den ungeraden Seitenzahlen rechts. |

## Beispiele

Zeigt, wie Seiten angezeigt werden, wenn sie in einem PDF-Reader geöffnet werden.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

// Zeigen Sie die Seiten jeweils zu zweit an, mit den ungeraden Seitennummern auf der linken Seite.
PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.PageLayout = PdfPageLayout.TwoPageLeft;

doc.Save(ArtifactsDir + "PdfSaveOptions.PageLayout.pdf", saveOptions);
```

### Siehe auch

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
