---
title: Aspose::Words::Drawing::ShapeBase::get_IsTopLevel method
linktitle: get_IsTopLevel
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::ShapeBase::get_IsTopLevel method. Returns true if this shape is not a child of a group shape in C++.'
type: docs
weight: 36000
url: /cpp/aspose.words.drawing/shapebase/get_istoplevel/
---
## ShapeBase::get_IsTopLevel method


Returns **true** if this shape is not a child of a group shape.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsTopLevel()
```


## Examples



Shows how to tell whether a shape is a part of a group shape. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shape->set_Width(200);
shape->set_Height(200);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);

// A shape by default is not part of any group shape, and therefore has the "IsTopLevel" property set to "true".
ASSERT_TRUE(shape->get_IsTopLevel());

auto group = System::MakeObject<Aspose::Words::Drawing::GroupShape>(doc);
group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

// Once we assimilate a shape into a group shape, the "IsTopLevel" property changes to "false".
ASSERT_FALSE(shape->get_IsTopLevel());
```

## See Also

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
