---
title: Aspose::Words::PageSetup::get_PageHeight method
linktitle: get_PageHeight
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::PageSetup::get_PageHeight method. Returns or sets the height of the page in points in C++.'
type: docs
weight: 33000
url: /cpp/aspose.words/pagesetup/get_pageheight/
---
## PageSetup::get_PageHeight method


Returns or sets the height of the page in points.

```cpp
double Aspose::Words::PageSetup::get_PageHeight()
```


## Examples



Shows how to insert an image, and use it as a watermark. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Insert the image into the header so that it will be visible on every page.
SharedPtr<System::Drawing::Image> image = System::Drawing::Image::FromFile(ImageDir + u"Transparent background logo.png");
builder->MoveToHeaderFooter(HeaderFooterType::HeaderPrimary);
SharedPtr<Shape> shape = builder->InsertImage(image);
shape->set_WrapType(WrapType::None);
shape->set_BehindText(true);

// Place the image at the center of the page.
shape->set_RelativeHorizontalPosition(RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(RelativeVerticalPosition::Page);
shape->set_Left((builder->get_PageSetup()->get_PageWidth() - shape->get_Width()) / 2);
shape->set_Top((builder->get_PageSetup()->get_PageHeight() - shape->get_Height()) / 2);

doc->Save(ArtifactsDir + u"DocumentBuilder.InsertWatermark.docx");
```

## See Also

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
