---
title: UpdatePageLayout
second_title: Aspose.Words for C++ API Reference
description: Rebuilds the page layout of the document.
type: docs
weight: 1171
url: /cpp/aspose.words/document/updatepagelayout/
---
## Document::UpdatePageLayout method


Rebuilds the page layout of the document.

```cpp
void Aspose::Words::Document::UpdatePageLayout()
```

## Remarks


This method formats a document into pages and updates the page number related fields in the document such as PAGE, PAGES, PAGEREF and REF. The up-to-date page layout information is required for a correct rendering of the document to fixed-page formats.

This method is automatically invoked when you first convert a document to PDF, XPS, image or print it. However, if you modify the document after rendering and then attempt to render it again - Aspose.Words will not update the page layout automatically. In this case you should call [UpdatePageLayout](./) before rendering again.

## Examples



Shows when to recalculate the page layout of the document. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Rendering.docx");

// Saving a document to PDF, to an image, or printing for the first time will automatically
// cache the layout of the document within its pages.
doc->Save(ArtifactsDir + u"Document.UpdatePageLayout.1.pdf");

// Modify the document in some way.
doc->get_Styles()->idx_get(u"Normal")->get_Font()->set_Size(6);
doc->get_Sections()->idx_get(0)->get_PageSetup()->set_Orientation(Orientation::Landscape);

// In the current version of Aspose.Words, modifying the document does not automatically rebuild
// the cached page layout. If we wish for the cached layout
// to stay up to date, we will need to update it manually.
doc->UpdatePageLayout();

doc->Save(ArtifactsDir + u"Document.UpdatePageLayout.2.pdf");
```

## See Also

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
