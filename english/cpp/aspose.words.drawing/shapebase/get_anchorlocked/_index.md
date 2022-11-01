---
title: get_AnchorLocked
second_title: Aspose.Words for C++ API Reference
description: Specifies whether the shape's anchor is locked.
type: docs
weight: 40
url: /cpp/aspose.words.drawing/shapebase/get_anchorlocked/
---
## ShapeBase.get_AnchorLocked method


Specifies whether the shape's anchor is locked.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_AnchorLocked()
```


The default value is **false**.

Has effect only for top level shapes.

This property affects behavior of the shape's anchor in Microsoft Word. When the anchor is not locked, moving the shape in Microsoft Word can move the shape's anchor too.

## Examples




Shows how to lock or unlock a shape's paragraph anchor. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");

builder->Write(u"Our shape will have an anchor attached to this paragraph.");
SharedPtr<Shape> shape = builder->InsertShape(ShapeType::Rectangle, 200, 160);
shape->set_WrapType(WrapType::None);
builder->InsertBreak(BreakType::ParagraphBreak);

builder->Writeln(u"Hello again!");

// Set the "AnchorLocked" property to "true" to prevent the shape's anchor
// from moving when moving the shape in Microsoft Word.
// Set the "AnchorLocked" property to "false" to allow any movement of the shape
// to also move its anchor to any other paragraph that the shape ends up close to.
shape->set_AnchorLocked(anchorLocked);

// If the shape does not have a visible anchor symbol to its left,
// we will need to enable visible anchors via "Options" -> "Display" -> "Object Anchors".
doc->Save(ArtifactsDir + u"Shape.AnchorLocked.docx");
```

