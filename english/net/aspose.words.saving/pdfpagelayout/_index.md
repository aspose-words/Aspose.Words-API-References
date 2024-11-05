---
title: PdfPageLayout Enum
linktitle: PdfPageLayout
articleTitle: PdfPageLayout
second_title: Aspose.Words for .NET
description: Aspose.Words.Saving.PdfPageLayout enum. Specifies the page layout to be used when the document is opened in a PDF reader in C#.
type: docs
weight: 5950
url: /net/aspose.words.saving/pdfpagelayout/
---
## PdfPageLayout enumeration

Specifies the page layout to be used when the document is opened in a PDF reader.

```csharp
public enum PdfPageLayout
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| SinglePage | `0` | Display one page at a time. |
| OneColumn | `1` | Display the pages in one column. |
| TwoColumnLeft | `2` | Display the pages in two columns, with odd-numbered pages on the left. |
| TwoColumnRight | `3` | Display the pages in two columns, with odd-numbered pages on the right. |
| TwoPageLeft | `4` | Display the pages two at a time, with odd-numbered pages on the left. |
| TwoPageRight | `5` | Display the pages two at a time, with odd-numbered pages on the right. |

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

* namespace [Aspose.Words.Saving](../../aspose.words.saving/)
* assembly [Aspose.Words](../../)
