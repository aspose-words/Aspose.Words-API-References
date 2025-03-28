---
title: PageSetup.Margins
linktitle: Margins
articleTitle: Margins
second_title: Aspose.Words for .NET
description: Adjust your page's Margins effortlessly with the PageSetup property. Customize settings for optimal layout and presentation. Enhance your document's appearance!
type: docs
weight: 260
url: /net/aspose.words/pagesetup/margins/
---
## PageSetup.Margins property

Returns or sets preset [`Margins`](../../margins/) of the page.

```csharp
public Margins Margins { get; set; }
```

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

* enum [Margins](../../margins/)
* class [PageSetup](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
