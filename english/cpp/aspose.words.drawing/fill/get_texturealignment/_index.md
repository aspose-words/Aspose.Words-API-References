---
title: Aspose::Words::Drawing::Fill::get_TextureAlignment method
linktitle: get_TextureAlignment
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Fill::get_TextureAlignment method. Gets or sets the alignment for tile texture fill in C++.'
type: docs
weight: 20000
url: /cpp/aspose.words.drawing/fill/get_texturealignment/
---
## Fill::get_TextureAlignment method


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

## See Also

* Enum [TextureAlignment](../../texturealignment/)
* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
