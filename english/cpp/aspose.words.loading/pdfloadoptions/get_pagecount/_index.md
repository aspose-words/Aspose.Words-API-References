---
title: Aspose::Words::Loading::PdfLoadOptions::get_PageCount method
linktitle: get_PageCount
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Loading::PdfLoadOptions::get_PageCount method. Gets or sets the number of pages to read. Default is MaxValue which means all pages of the document will be read in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.loading/pdfloadoptions/get_pagecount/
---
## PdfLoadOptions::get_PageCount method


Gets or sets the number of pages to read. Default is MaxValue which means all pages of the document will be read.

```cpp
int32_t Aspose::Words::Loading::PdfLoadOptions::get_PageCount() const
```


## Examples



Shows how to skip images during loading PDF files. 
```cpp
auto options = System::MakeObject<Aspose::Words::Loading::PdfLoadOptions>();
options->set_SkipPdfImages(isSkipPdfImages);
options->set_PageIndex(0);
options->set_PageCount(1);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.pdf", options);
System::SharedPtr<Aspose::Words::NodeCollection> shapeCollection = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true);

if (isSkipPdfImages)
{
    ASSERT_EQ(shapeCollection->get_Count(), 0);
}
else
{
    ASSERT_NE(shapeCollection->get_Count(), 0);
}
```

## See Also

* Class [PdfLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
