---
title: Aspose::Words::Document::ExtractPages method
linktitle: ExtractPages
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Document::ExtractPages method. Returns the Document object representing specified range of pages in C++.'
type: docs
weight: 12000
url: /cpp/aspose.words/document/extractpages/
---
## Document::ExtractPages(int32_t, int32_t) method


Returns the [Document](../) object representing specified range of pages.

```cpp
System::SharedPtr<Aspose::Words::Document> Aspose::Words::Document::ExtractPages(int32_t index, int32_t count)
```


| Parameter | Type | Description |
| --- | --- | --- |
| index | int32_t | The zero-based index of the first page to extract. |
| count | int32_t | Number of pages to be extracted. |

## Examples



Shows how to get specified range of pages from the document. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Layout entities.docx");

doc = doc->ExtractPages(0, 2);

doc->Save(get_ArtifactsDir() + u"Document.ExtractPages.docx");
```


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

* Class [Document](../)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::ExtractPages(int32_t, int32_t, const System::SharedPtr\<Aspose::Words::PageExtractOptions\>\&) method


Returns the [Document](../) object representing the specified range of pages and the given page extract options.

```cpp
System::SharedPtr<Aspose::Words::Document> Aspose::Words::Document::ExtractPages(int32_t index, int32_t count, const System::SharedPtr<Aspose::Words::PageExtractOptions> &options)
```


| Parameter | Type | Description |
| --- | --- | --- |
| index | int32_t | The zero-based index of the first page to extract. |
| count | int32_t | Number of pages to be extracted. |
| options | const System::SharedPtr\<Aspose::Words::PageExtractOptions\>\& | Provides options for managing the page extracting process. |

## See Also

* Class [Document](../)
* Class [PageExtractOptions](../../pageextractoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
