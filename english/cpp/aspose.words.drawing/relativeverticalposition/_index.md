---
title: Aspose::Words::Drawing::RelativeVerticalPosition enum
linktitle: RelativeVerticalPosition
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::RelativeVerticalPosition enum. Specifies to what the vertical position of a shape or text frame is relative in C++.'
type: docs
weight: 34000
url: /cpp/aspose.words.drawing/relativeverticalposition/
---
## RelativeVerticalPosition enum


Specifies to what the vertical position of a shape or text frame is relative.

```cpp
enum class RelativeVerticalPosition
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Margin | 0 | Specifies that the vertical positioning shall be relative to the page margins. |
| Page | 1 | The object is positioned relative to the top edge of the page. |
| Paragraph | 2 | The object is positioned relative to the top of the paragraph that contains the anchor. |
| Line | 3 | Undocumented. |
| TopMargin | 4 | Specifies that the vertical positioning shall be relative to the top margin of the current page. |
| BottomMargin | 5 | Specifies that the vertical positioning shall be relative to the bottom margin of the current page. |
| InsideMargin | 6 | Specifies that the vertical positioning shall be relative to the inside margin of the current page. |
| OutsideMargin | 7 | Specifies that the vertical positioning shall be relative to the outside margin of the current page. |
| TableDefault | n/a | Default value is [Margin](./). |
| TextFrameDefault | n/a | Default value is [Paragraph](./). |


## Examples



Shows how to insert an image, and use it as a watermark. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insert the image into the header so that it will be visible on every page.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Transparent background logo.png");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
shape->set_BehindText(true);

// Place the image at the center of the page.
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_Left((builder->get_PageSetup()->get_PageWidth() - shape->get_Width()) / 2);
shape->set_Top((builder->get_PageSetup()->get_PageHeight() - shape->get_Height()) / 2);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertWatermark.docx");
```


Shows how to insert a floating image to the center of a page. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insert a floating image that will appear behind the overlapping text and align it to the page's center.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
shape->set_BehindText(true);
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_HorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Center);
shape->set_VerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Center);

doc->Save(get_ArtifactsDir() + u"Image.CreateFloatingPageCenter.docx");
```

## See Also

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
