---
title: Aspose::Words::Drawing::ShapeBase::get_IsDecorative method
linktitle: get_IsDecorative
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::ShapeBase::get_IsDecorative method. Gets or sets the flag that specifies whether the shape is decorative in the document in C++.'
type: docs
weight: 25000
url: /cpp/aspose.words.drawing/shapebase/get_isdecorative/
---
## ShapeBase::get_IsDecorative method


Gets or sets the flag that specifies whether the shape is decorative in the document.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsDecorative()
```


## Examples



Shows how to set that the shape is decorative. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Decorative shapes.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->idx_get(0));
ASSERT_TRUE(shape->get_IsDecorative());

// If "AlternativeText" is not empty, the shape cannot be decorative.
// That's why our value has changed to 'false'.
shape->set_AlternativeText(u"Alternative text.");
ASSERT_FALSE(shape->get_IsDecorative());

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->MoveToDocumentEnd();
// Create a new shape as decorative.
shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 100, 100);
shape->set_IsDecorative(true);

doc->Save(get_ArtifactsDir() + u"Shape.IsDecorative.docx");
```

## See Also

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
