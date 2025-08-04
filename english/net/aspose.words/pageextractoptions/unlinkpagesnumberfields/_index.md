---
title: PageExtractOptions.UnlinkPagesNumberFields
linktitle: UnlinkPagesNumberFields
articleTitle: UnlinkPagesNumberFields
second_title: Aspose.Words for .NET
description: Replace NUMPAGES fields with actual values in extracted pages for accurate numbering using UnlinkPagesNumberFields.
type: docs
weight: 20
url: /net/aspose.words/pageextractoptions/unlinkpagesnumberfields/
---
## PageExtractOptions.UnlinkPagesNumberFields property

Specifies whether NUMPAGES fields in the resulting document will be replaced with their actual resulting values. Default value is `true`.

```csharp
public bool UnlinkPagesNumberFields { get; set; }
```

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

* class [PageExtractOptions](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
