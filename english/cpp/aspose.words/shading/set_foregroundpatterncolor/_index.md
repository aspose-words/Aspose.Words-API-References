---
title: Aspose::Words::Shading::set_ForegroundPatternColor method
linktitle: set_ForegroundPatternColor
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Shading::set_ForegroundPatternColor method. Sets the color that''s applied to the foreground of the Shading object in C++.'
type: docs
weight: 17000
url: /cpp/aspose.words/shading/set_foregroundpatterncolor/
---
## Shading::set_ForegroundPatternColor method


Sets the color that's applied to the foreground of the [Shading](../) object.

```cpp
void Aspose::Words::Shading::set_ForegroundPatternColor(System::Drawing::Color value)
```

## Examples


Shows how to decorate text with borders and shading.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::BorderCollection> borders = builder->get_ParagraphFormat()->get_Borders();
borders->set_DistanceFromText(20);
borders->idx_get(BorderType::Left)->set_LineStyle(LineStyle::Double);
borders->idx_get(BorderType::Right)->set_LineStyle(LineStyle::Double);
borders->idx_get(BorderType::Top)->set_LineStyle(LineStyle::Double);
borders->idx_get(BorderType::Bottom)->set_LineStyle(LineStyle::Double);

System::SharedPtr<Aspose::Words::Shading> shading = builder->get_ParagraphFormat()->get_Shading();
shading->set_Texture(TextureIndex::TextureDiagonalCross);
shading->set_BackgroundPatternColor(System::Drawing::Color::get_LightCoral());
shading->set_ForegroundPatternColor(System::Drawing::Color::get_LightSalmon());

builder->Write(u"This paragraph is formatted with a double border and shading.");
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.ApplyBordersAndShading.docx");
```
## See Also

* Class [Shading](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
