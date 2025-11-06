---
title: PageExtractOptions Class
linktitle: PageExtractOptions
articleTitle: PageExtractOptions
second_title: Aspose.Words for .NET
description: Easily extract document pages with Aspose.Words.PageExtractOptions. Customize output with flexible page extraction settings.
type: docs
weight: 5120
url: /net/aspose.words/pageextractoptions/
---
## PageExtractOptions class

Allows to specify options for document page extracting.

```csharp
public class PageExtractOptions
```

## Constructors

| Name | Description |
| --- | --- |
| [PageExtractOptions](pageextractoptions/)() | The default constructor. |

## Properties

| Name | Description |
| --- | --- |
| [UnlinkPagesNumberFields](../../aspose.words/pageextractoptions/unlinkpagesnumberfields/) { get; set; } | Specifies whether NUMPAGES fields in the resulting document will be replaced with their actual resulting values. Default value is `true`. |
| [UpdatePageStartingNumber](../../aspose.words/pageextractoptions/updatepagestartingnumber/) { get; set; } | Specifies whether the start page number in the resulting document shall be updated. Default value is `true`. |

## Examples

Show how to reset the initial page numbering and save the NUMPAGE field.

```csharp
Document doc = new Document(MyDir + "Page fields.docx");

// Default behavior:
// The extracted page numbering is the same as in the original document, as if we had selected "Print 2 pages" in MS Word.
// The start page will be set to 2 and the field indicating the number of pages will be removed
// and replaced with a constant value equal to the number of pages.
Document extractedDoc1 = doc.ExtractPages(1, 1);
extractedDoc1.Save(ArtifactsDir + "Document.ExtractPagesWithOptions.Default.docx");

// Altered behavior:
// The extracted page numbering is reset and a new one begins,
// as if we had copied the contents of the second page and pasted it into a new document.
// The start page will be set to 1 and the field indicating the number of pages will be left unchanged
// and will show the current number of pages.
PageExtractOptions extractOptions = new PageExtractOptions();
extractOptions.UpdatePageStartingNumber = false;
extractOptions.UnlinkPagesNumberFields = false;
Document extractedDoc2 = doc.ExtractPages(1, 1, extractOptions);
extractedDoc2.Save(ArtifactsDir + "Document.ExtractPagesWithOptions.Options.docx");
```

### See Also

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
