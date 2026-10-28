---
title: Aspose::Words::Drawing::Fill::set_TextureAlignment method
linktitle: set_TextureAlignment
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Fill::set_TextureAlignment method. Sets the alignment for tile texture fill in C++.'
type: docs
weight: 77000
url: /cpp/aspose.words.drawing/fill/set_texturealignment/
---
## Fill::set_TextureAlignment method


Sets the alignment for tile texture fill.

```cpp
void Aspose::Words::Drawing::Fill::set_TextureAlignment(Aspose::Words::Drawing::TextureAlignment value)
```

## Examples


Shows how to fill and tiling the texture inside the shape.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(ShapeType::Rectangle, static_cast<double>(80), static_cast<double>(80));

// Apply texture alignment to the shape fill.
shape->get_Fill()->PresetTextured(PresetTexture::Canvas);
shape->get_Fill()->set_TextureAlignment(TextureAlignment::TopRight);

// Use the compliance option to define the shape using DML if you want to get "TextureAlignment"
// property after the document saves.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Compliance(OoxmlCompliance::Iso29500_2008_Strict);

doc->Save(get_ArtifactsDir() + u"Shape.TextureFill.docx", saveOptions);

doc = System::MakeObject<Aspose::Words::Document>(System::String(get_ArtifactsDir() + u"Shape.TextureFill.docx"));
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(NodeType::Shape, 0, true));

ASSERT_EQ(TextureAlignment::TopRight, shape->get_Fill()->get_TextureAlignment());
ASSERT_EQ(PresetTexture::Canvas, shape->get_Fill()->get_PresetTexture());
```
## See Also

* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
