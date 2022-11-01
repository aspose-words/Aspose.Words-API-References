---
title: WrapType
second_title: Aspose.Words for C++ API Reference
description: Specifies how text is wrapped around a shape or picture.
type: docs
weight: 573
url: /cpp/aspose.words.drawing/wraptype/
---
## WrapType enum


Specifies how text is wrapped around a shape or picture.

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | 3 | No text wrapping around the shape. The shape is placed behind or in front of text. |
| Inline | 0 | The shape remains on the same layer as text and treated as a character. |
| TopBottom | 1 | The text stops at the top of the shape and restarts on the line below the shape. |
| Square | 2 | Wraps text around all sides of the square bounding box of the shape. |
| Tight | 4 | Wraps tightly around the edges of the shape, instead of wrapping around the bounding box. |
| Through | 5 | Same as Tight, but wraps inside any parts of the shape that are open. |


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

