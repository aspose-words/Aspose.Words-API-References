---
title: get_IsTopLevel
second_title: Aspose.Words for C++ API Reference
description: Returns true if this shape is not a child of a group shape.
type: docs
weight: 443
url: /cpp/aspose.words.drawing/shapebase/get_istoplevel/
---
## ShapeBase.get_IsTopLevel method


Returns true if this shape is not a child of a group shape.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsTopLevel()
```


## Examples




Shows how to tell whether a shape is a part of a group shape. 
```cpp
auto doc = MakeObject<Document>();

auto shape = MakeObject<Shape>(doc, ShapeType::Rectangle);
shape->set_Width(200);
shape->set_Height(200);
shape->set_WrapType(WrapType::None);

// A shape by default is not part of any group shape, and therefore has the "IsTopLevel" property set to "true".
ASSERT_TRUE(shape->get_IsTopLevel());

auto group = MakeObject<GroupShape>(doc);
group->AppendChild(shape);

// Once we assimilate a shape into a group shape, the "IsTopLevel" property changes to "false".
ASSERT_FALSE(shape->get_IsTopLevel());
```

