---
title: Aspose::Words::Drawing::ShapeBase::get_Hidden method
linktitle: get_Hidden
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::ShapeBase::get_Hidden method. Gets or sets a boolean value indicating whether the shape is visible in C++.'
type: docs
weight: 22750
url: /cpp/aspose.words.drawing/shapebase/get_hidden/
---
## ShapeBase::get_Hidden method


Gets or sets a boolean value indicating whether the shape is visible.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_Hidden()
```


## Examples



Shows how to hide the shape. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shadow color.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
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
