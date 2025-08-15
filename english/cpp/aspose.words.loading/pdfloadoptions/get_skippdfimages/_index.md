---
title: Aspose::Words::Loading::PdfLoadOptions::get_SkipPdfImages method
linktitle: get_SkipPdfImages
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Loading::PdfLoadOptions::get_SkipPdfImages method. Gets or sets the flag indicating whether images must be skipped while loading PDF document. Default is false in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words.loading/pdfloadoptions/get_skippdfimages/
---
## PdfLoadOptions::get_SkipPdfImages method


Gets or sets the flag indicating whether images must be skipped while loading PDF document. Default is **false**.

```cpp
bool Aspose::Words::Loading::PdfLoadOptions::get_SkipPdfImages() const
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
