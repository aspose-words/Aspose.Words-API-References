---
title: Aspose::Words::Drawing::TextureAlignment enum
linktitle: TextureAlignment
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::TextureAlignment enum. Specifies the alignment for the tiling of the texture fill in C++.'
type: docs
weight: 42000
url: /cpp/aspose.words.drawing/texturealignment/
---
## TextureAlignment enum


Specifies the alignment for the tiling of the texture fill.

```cpp
enum class TextureAlignment
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| TopLeft | 0 | Top left texture alignment. |
| Top | 1 | Top texture alignment. |
| TopRight | 2 | Top right texture alignment. |
| Left | 3 | Left texture alignment. |
| Center | 4 | Center texture alignment. |
| Right | 5 | Right texture alignment. |
| BottomLeft | 6 | Bottom left texture alignment. |
| Bottom | 7 | Bottom texture alignment. |
| BottomRight | 8 | Bottom right texture alignment. |
| None | 9 | None texture alignment. |


## Examples



Shows how to fill and tiling the texture inside the shape. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 80, 80);

// Apply texture alignment to the shape fill.
shape->get_Fill()->PresetTextured(Aspose::Words::Drawing::PresetTexture::Canvas);
shape->get_Fill()->set_TextureAlignment(Aspose::Words::Drawing::TextureAlignment::TopRight);

// Use the compliance option to define the shape using DML if you want to get "TextureAlignment"
// property after the document saves.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Strict);

doc->Save(get_ArtifactsDir() + u"Shape.TextureFill.docx", saveOptions);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Shape.TextureFill.docx");
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

ASSERT_EQ(Aspose::Words::Drawing::TextureAlignment::TopRight, shape->get_Fill()->get_TextureAlignment());
ASSERT_EQ(Aspose::Words::Drawing::PresetTexture::Canvas, shape->get_Fill()->get_PresetTexture());
```

## See Also

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
