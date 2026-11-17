---
title: Aspose::Words::Drawing::ShapeBase::set_Hidden method
linktitle: set_Hidden
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::ShapeBase::set_Hidden method. Sets a boolean value indicating whether the shape is visible in C++.'
type: docs
weight: 77600
url: /cpp/aspose.words.drawing/shapebase/set_hidden/
---
## ShapeBase::set_Hidden method


Sets a boolean value indicating whether the shape is visible.

```cpp
void Aspose::Words::Drawing::ShapeBase::set_Hidden(bool value)
```

## Remarks

 The default value is **false**. 
## Examples


Shows how to hide the shape.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Shadow color.docx"));

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(NodeType::Shape, 0, true));
if (!shape->get_Hidden())
{
    shape->set_Hidden(true);
}

doc->Save(get_ArtifactsDir() + u"Shape.Hidden.docx");
```
## See Also

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
