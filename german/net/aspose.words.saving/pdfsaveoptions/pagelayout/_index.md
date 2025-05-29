---
title: PdfSaveOptions.PageLayout
linktitle: PageLayout
articleTitle: PageLayout
second_title: Aspose.Words für .NET
description: Entdecken Sie die PageLayout-Eigenschaft von PdfSaveOptions, um das Layout Ihrer PDF-Datei für eine optimale Anzeige in jedem Reader anzupassen. Verbessern Sie die Präsentation Ihres Dokuments!
type: docs
weight: 250
url: /de/net/aspose.words.saving/pdfsaveoptions/pagelayout/
---
## PdfSaveOptions.PageLayout property

Gibt das Seitenlayout an, das verwendet werden soll, wenn das Dokument in einem PDF-Reader geöffnet wird.

```csharp
public PdfPageLayout PageLayout { get; set; }
```

## Bemerkungen

Der Standardwert istSinglePage .

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

* enum [PdfPageLayout](../../pdfpagelayout/)
* class [PdfSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
