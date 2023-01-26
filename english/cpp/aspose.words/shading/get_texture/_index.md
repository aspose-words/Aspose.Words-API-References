---
title: get_Texture
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the shading texture.
type: docs
weight: 118
url: /cpp/aspose.words/shading/get_texture/
---
## Shading::get_Texture method


Gets or sets the shading texture.

```cpp
Aspose::Words::TextureIndex Aspose::Words::Shading::get_Texture()
```


## Examples



Shows how to decorate text with borders and shading. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<BorderCollection> borders = builder->get_ParagraphFormat()->get_Borders();
borders->set_DistanceFromText(20);
borders->idx_get(BorderType::Left)->set_LineStyle(LineStyle::Double);
borders->idx_get(BorderType::Right)->set_LineStyle(LineStyle::Double);
borders->idx_get(BorderType::Top)->set_LineStyle(LineStyle::Double);
borders->idx_get(BorderType::Bottom)->set_LineStyle(LineStyle::Double);

SharedPtr<Shading> shading = builder->get_ParagraphFormat()->get_Shading();
shading->set_Texture(TextureIndex::TextureDiagonalCross);
shading->set_BackgroundPatternColor(System::Drawing::Color::get_LightCoral());
shading->set_ForegroundPatternColor(System::Drawing::Color::get_LightSalmon());

builder->Write(u"This paragraph is formatted with a double border and shading.");
doc->Save(ArtifactsDir + u"DocumentBuilder.ApplyBordersAndShading.docx");
```

## See Also

* Enum [TextureIndex](../../textureindex/)
* Class [Shading](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
