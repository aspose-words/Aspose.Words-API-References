---
title: PdfSaveOptions.PageLayout
linktitle: PageLayout
articleTitle: PageLayout
second_title: Aspose.Words for .NET
description: Discover the PdfSaveOptions PageLayout property to customize your PDF’s layout for optimal viewing in any reader. Enhance your document's presentation!
type: docs
weight: 250
url: /net/aspose.words.saving/pdfsaveoptions/pagelayout/
---
## PdfSaveOptions.PageLayout property

Specifies the page layout to be used when the document is opened in a PDF reader.

```csharp
public PdfPageLayout PageLayout { get; set; }
```

## Remarks

The default value is SinglePage.

## Examples

Shows how to display pages when opened in a PDF reader.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

// Display the pages two at a time, with odd-numbered pages on the left.
PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.PageLayout = PdfPageLayout.TwoPageLeft;

doc.Save(ArtifactsDir + "PdfSaveOptions.PageLayout.pdf", saveOptions);
```

### See Also

* enum [PdfPageLayout](../../pdfpagelayout/)
* class [PdfSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
