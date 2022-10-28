---
title: get_TextureAlignment
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the alignment for tile texture fill.
type: docs
weight: 183
url: /cpp/aspose.words.drawing/fill/get_texturealignment/
---
## Fill.get_TextureAlignment method


Gets or sets the alignment for tile texture fill.

```cpp
Aspose::Words::Drawing::TextureAlignment Aspose::Words::Drawing::Fill::get_TextureAlignment()
```


## Examples




Shows how to fill and tiling the texture inside the shape. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<Shape> shape = builder->InsertShape(ShapeType::Rectangle, 80, 80);

// Apply texture alignment to the shape fill.
shape->get_Fill()->PresetTextured(PresetTexture::Canvas);
shape->get_Fill()->set_TextureAlignment(TextureAlignment::TopRight);

// Use the compliance option to define the shape using DML if you want to get "TextureAlignment"
// property after the document saves.
auto saveOptions = MakeObject<OoxmlSaveOptions>();
saveOptions->set_Compliance(OoxmlCompliance::Iso29500_2008_Strict);

doc->Save(ArtifactsDir + u"Shape.TextureFill.docx", saveOptions);
```

