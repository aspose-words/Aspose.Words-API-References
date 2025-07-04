---
title: Aspose::Words::Margins enum
linktitle: Margins
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Margins enum. Specifies preset margins in C++.'
type: docs
weight: 99000
url: /cpp/aspose.words/margins/
---
## Margins enum


Specifies preset margins.

```cpp
enum class Margins
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Normal | 0 | Normal margins. |
| Narrow | 1 | Narrow margins. |
| Moderate | 2 | Moderate margins. |
| Wide | 3 | Wide margins. |
| Mirrored | 4 | Mirrored margins. |
| Custom | 5 | Custom margins. |


## Examples



Shows when to recalculate the page layout of the document. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Saving a document to PDF, to an image, or printing for the first time will automatically
// cache the layout of the document within its pages.
doc->Save(get_ArtifactsDir() + u"Document.UpdatePageLayout.1.pdf");

// Modify the document in some way.
doc->get_Styles()->idx_get(u"Normal")->get_Font()->set_Size(6);
doc->get_Sections()->idx_get(0)->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
doc->get_Sections()->idx_get(0)->get_PageSetup()->set_Margins(Aspose::Words::Margins::Mirrored);

// In the current version of Aspose.Words, modifying the document does not automatically rebuild
// the cached page layout. If we wish for the cached layout
// to stay up to date, we will need to update it manually.
doc->UpdatePageLayout();

doc->Save(get_ArtifactsDir() + u"Document.UpdatePageLayout.2.pdf");
```

## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
