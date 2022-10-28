---
title: get_IsInline
second_title: Aspose.Words for C++ API Reference
description: A quick way to determine if this shape is positioned inline with text.
type: docs
weight: 365
url: /cpp/aspose.words.drawing/shapebase/get_isinline/
---
## ShapeBase.get_IsInline method


A quick way to determine if this shape is positioned inline with text.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsInline()
```


Has effect only for top level shapes.

## Examples




Shows how to determine whether a shape is inline or floating. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Below are two wrapping types that shapes may have.
// 1 -  Inline:
builder->Write(u"Hello world! ");
SharedPtr<Shape> shape = builder->InsertShape(ShapeType::Rectangle, 100, 100);
shape->set_FillColor(System::Drawing::Color::get_LightBlue());
builder->Write(u" Hello again.");

// An inline shape sits inside a paragraph among other paragraph elements, such as runs of text.
// In Microsoft Word, we may click and drag the shape to any paragraph as if it is a character.
// If the shape is large, it will affect vertical paragraph spacing.
// We cannot move this shape to a place with no paragraph.
ASSERT_EQ(WrapType::Inline, shape->get_WrapType());
ASSERT_TRUE(shape->get_IsInline());

// 2 -  Floating:
shape = builder->InsertShape(ShapeType::Rectangle, RelativeHorizontalPosition::LeftMargin, 200, RelativeVerticalPosition::TopMargin, 200, 100, 100,
                             WrapType::None);
shape->set_FillColor(System::Drawing::Color::get_Orange());

// A floating shape belongs to the paragraph that we insert it into,
// which we can determine by an anchor symbol that appears when we click the shape.
// If the shape does not have a visible anchor symbol to its left,
// we will need to enable visible anchors via "Options" -> "Display" -> "Object Anchors".
// In Microsoft Word, we may left click and drag this shape freely to any location.
ASSERT_EQ(WrapType::None, shape->get_WrapType());
ASSERT_FALSE(shape->get_IsInline());

doc->Save(ArtifactsDir + u"Shape.IsInline.docx");
```

