---
title: Aspose::Words::Drawing::RelativeHorizontalPosition enum
linktitle: RelativeHorizontalPosition
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::RelativeHorizontalPosition enum. Specifies to what the horizontal position of a shape or text frame is relative in C++.'
type: docs
weight: 33000
url: /cpp/aspose.words.drawing/relativehorizontalposition/
---
## RelativeHorizontalPosition enum


Specifies to what the horizontal position of a shape or text frame is relative.

```cpp
enum class RelativeHorizontalPosition
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Margin | 0 | Specifies that the horizontal positioning shall be relative to the page margins. |
| Page | 1 | The object is positioned relative to the left edge of the page. |
| Column | 2 | The object is positioned relative to the left side of the column. |
| Character | 3 | The object is positioned relative to the left side of the paragraph. |
| LeftMargin | 4 | Specifies that the horizontal positioning shall be relative to the left margin of the page. |
| RightMargin | 5 | Specifies that the horizontal positioning shall be relative to the right margin of the page. |
| InsideMargin | 6 | Specifies that the horizontal positioning shall be relative to the inside margin of the current page (the left margin on odd pages, right on even pages). |
| OutsideMargin | 7 | Specifies that the horizontal positioning shall be relative to the outside margin of the current page (the right margin on odd pages, left on even pages). |
| Default | n/a | Default value is [Column](./). |


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


Shows how to insert a floating image to the center of a page. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Insert a floating image that will appear behind the overlapping text and align it to the page's center.
SharedPtr<Shape> shape = builder->InsertImage(ImageDir + u"Logo.jpg");
shape->set_WrapType(WrapType::None);
shape->set_BehindText(true);
shape->set_RelativeHorizontalPosition(RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(RelativeVerticalPosition::Page);
shape->set_HorizontalAlignment(HorizontalAlignment::Center);
shape->set_VerticalAlignment(VerticalAlignment::Center);

doc->Save(ArtifactsDir + u"Image.CreateFloatingPageCenter.docx");
```

## See Also

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
