---
title: Aspose::Words::PageExtractOptions::get_UnlinkPagesNumberFields method
linktitle: get_UnlinkPagesNumberFields
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::PageExtractOptions::get_UnlinkPagesNumberFields method. Specifies whether NUMPAGES fields in the resulting document will be replaced with their actual resulting values. Default value is true in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words/pageextractoptions/get_unlinkpagesnumberfields/
---
## PageExtractOptions::get_UnlinkPagesNumberFields method


Specifies whether NUMPAGES fields in the resulting document will be replaced with their actual resulting values. Default value is **true**.

```cpp
bool Aspose::Words::PageExtractOptions::get_UnlinkPagesNumberFields() const
```


## Examples



Show how to reset the initial page numbering and save the NUMPAGE field. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Page fields.docx");

// Default behavior:
// The extracted page numbering is the same as in the original document, as if we had selected "Print 2 pages" in MS Word.
// The start page will be set to 2 and the field indicating the number of pages will be removed
// and replaced with a constant value equal to the number of pages.
System::SharedPtr<Aspose::Words::Document> extractedDoc1 = doc->ExtractPages(1, 1);
extractedDoc1->Save(get_ArtifactsDir() + u"Document.ExtractPagesWithOptions.Default.docx");

// Altered behavior:
// The extracted page numbering is reset and a new one begins,
// as if we had copied the contents of the second page and pasted it into a new document.
// The start page will be set to 1 and the field indicating the number of pages will be left unchanged
// and will show the current number of pages.
auto extractOptions = System::MakeObject<Aspose::Words::PageExtractOptions>();
extractOptions->set_UpdatePageStartingNumber(false);
extractOptions->set_UnlinkPagesNumberFields(false);
System::SharedPtr<Aspose::Words::Document> extractedDoc2 = doc->ExtractPages(1, 1, extractOptions);
extractedDoc2->Save(get_ArtifactsDir() + u"Document.ExtractPagesWithOptions.Options.docx");
```

## See Also

* Class [PageExtractOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
