---
title: Aspose::Words::Drawing::ShapeBase::set_Target method
linktitle: set_Target
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::ShapeBase::set_Target method. Sets the target frame for the shape hyperlink in C++.'
type: docs
weight: 86000
url: /cpp/aspose.words.drawing/shapebase/set_target/
---
## ShapeBase::set_Target method


Sets the target frame for the shape hyperlink.

```cpp
void Aspose::Words::Drawing::ShapeBase::set_Target(const System::String & value)
```

## Remarks


The default value is an empty string.
## Examples


Shows how to insert a shape which contains an image, and is also a hyperlink.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_HRef(u"https://forum.aspose.com/");
shape->set_Target(u"New Window");
shape->set_ScreenTip(u"Aspose.Words Support Forums");

// Ctrl + left-clicking the shape in Microsoft Word will open a new web browser window
// and take us to the hyperlink in the "HRef" property.
doc->Save(get_ArtifactsDir() + u"Image.InsertImageWithHyperlink.docx");
```
## See Also

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
