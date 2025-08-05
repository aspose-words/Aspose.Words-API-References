---
title: Aspose::Words::Loading::PdfLoadOptions::get_PageIndex method
linktitle: get_PageIndex
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Loading::PdfLoadOptions::get_PageIndex method. Gets or sets the 0-based index of the first page to read. Default is 0 in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words.loading/pdfloadoptions/get_pageindex/
---
## PdfLoadOptions::get_PageIndex method


Gets or sets the 0-based index of the first page to read. Default is 0.

```cpp
int32_t Aspose::Words::Loading::PdfLoadOptions::get_PageIndex() const
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
