---
title: get_IsDecorative
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the flag that specifies whether the shape is decorative in the document.
type: docs
weight: 313
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
auto doc = MakeObject<Document>(MyDir + u"Decorative shapes.docx");

auto shape = System::DynamicCast<Shape>(doc->GetChildNodes(NodeType::Shape, true)->idx_get(0));
ASSERT_TRUE(shape->get_IsDecorative());

// If "AlternativeText" is not empty, the shape cannot be decorative.
// That's why our value has changed to 'false'.
shape->set_AlternativeText(u"Alternative text.");
ASSERT_FALSE(shape->get_IsDecorative());

auto builder = MakeObject<DocumentBuilder>(doc);

builder->MoveToDocumentEnd();
// Create a new shape as decorative.
shape = builder->InsertShape(ShapeType::Rectangle, 100, 100);
shape->set_IsDecorative(true);

doc->Save(ArtifactsDir + u"Shape.IsDecorative.docx");
```

## See Also

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words](../../../)
