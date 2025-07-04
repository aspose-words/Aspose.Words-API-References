---
title: Aspose::Words::Document::get_PageCount method
linktitle: get_PageCount
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Document::get_PageCount method. Gets the number of pages in the document as calculated by the most recent page layout operation in C++.'
type: docs
weight: 43000
url: /cpp/aspose.words/document/get_pagecount/
---
## Document::get_PageCount method


Gets the number of pages in the document as calculated by the most recent page layout operation.

```cpp
int32_t Aspose::Words::Document::get_PageCount()
```


## Examples



Shows how to count the number of pages in the document. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Page 1");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Write(u"Page 2");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Write(u"Page 3");

// Verify the expected page count of the document.
ASSERT_EQ(3, doc->get_PageCount());

// Getting the PageCount property invoked the document's page layout to calculate the value.
// This operation will not need to be re-done when rendering the document to a fixed page save format,
// such as .pdf. So you can save some time, especially with more complex documents.
doc->Save(get_ArtifactsDir() + u"Document.GetPageCount.pdf");
```

## See Also

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
