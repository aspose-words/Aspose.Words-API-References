---
title: Aspose::Words::Drawing::TextBox::set_NoTextRotation method
linktitle: set_NoTextRotation
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::TextBox::set_NoTextRotation method. Sets a boolean value indicating either text of the TextBox should not rotate when the shape is rotated in C++.'
type: docs
weight: 25000
url: /cpp/aspose.words.drawing/textbox/set_notextrotation/
---
## TextBox::set_NoTextRotation method


Sets a boolean value indicating either text of the TextBox should not rotate when the shape is rotated.

```cpp
void Aspose::Words::Drawing::TextBox::set_NoTextRotation(bool value)
```

## Remarks


The default value is **false**
## Examples


Shows how to disable text rotation when the shape is rotate.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(ShapeType::Ellipse, static_cast<double>(20), static_cast<double>(20));
shape->get_TextBox()->set_NoTextRotation(true);

doc->Save(get_ArtifactsDir() + u"Shape.NoTextRotation.docx");
```
## See Also

* Class [TextBox](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
