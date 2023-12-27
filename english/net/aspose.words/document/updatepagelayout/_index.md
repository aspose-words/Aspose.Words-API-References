---
title: Document.UpdatePageLayout
linktitle: UpdatePageLayout
articleTitle: UpdatePageLayout
second_title: Aspose.Words for .NET
description: Document UpdatePageLayout method. Rebuilds the page layout of the document in C#.
type: docs
weight: 800
url: /net/aspose.words/document/updatepagelayout/
---
## Document.UpdatePageLayout method

Rebuilds the page layout of the document.

```csharp
public void UpdatePageLayout()
```

## Remarks

This method formats a document into pages and updates the page number related fields in the document such as PAGE, PAGES, PAGEREF and REF. The up-to-date page layout information is required for a correct rendering of the document to fixed-page formats.

This method is automatically invoked when you first convert a document to PDF, XPS, image or print it. However, if you modify the document after rendering and then attempt to render it again - Aspose.Words will not update the page layout automatically. In this case you should call `UpdatePageLayout` before rendering again.

## Examples

Shows when to recalculate the page layout of the document.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Saving a document to PDF, to an image, or printing for the first time will automatically
// cache the layout of the document within its pages.
doc.Save(ArtifactsDir + "Document.UpdatePageLayout.1.pdf");

// Modify the document in some way.
doc.Styles["Normal"].Font.Size = 6;
doc.Sections[0].PageSetup.Orientation = Aspose.Words.Orientation.Landscape;
doc.Sections[0].PageSetup.Margins = Margins.Mirrored;

// In the current version of Aspose.Words, modifying the document does not automatically rebuild 
// the cached page layout. If we wish for the cached layout
// to stay up to date, we will need to update it manually.
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.UpdatePageLayout.2.pdf");
```

### See Also

* class [Document](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
