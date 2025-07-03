---
title: Aspose::Words::Drawing::TextBox::get_NoTextRotation method
linktitle: get_NoTextRotation
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::TextBox::get_NoTextRotation method. Gets or sets a boolean value indicating either text of the TextBox should not rotate when the shape is rotated in C++.'
type: docs
weight: 10000
url: /cpp/aspose.words.drawing/textbox/get_notextrotation/
---
## TextBox::get_NoTextRotation method


Gets or sets a boolean value indicating either text of the [TextBox](../) should not rotate when the shape is rotated.

```cpp
bool Aspose::Words::Drawing::TextBox::get_NoTextRotation()
```

## Remarks


The default value is **false**

## Examples



Shows how to disable text rotation when the shape is rotate. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Ellipse, 20, 20);
shape->get_TextBox()->set_NoTextRotation(true);

doc->Save(get_ArtifactsDir() + u"Shape.NoTextRotation.docx");
```

## See Also

* Class [TextBox](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
