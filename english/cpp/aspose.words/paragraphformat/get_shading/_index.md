---
title: Aspose::Words::ParagraphFormat::get_Shading method
linktitle: get_Shading
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::ParagraphFormat::get_Shading method. Returns a Shading object that refers to the shading formatting for the paragraph in C++.'
type: docs
weight: 29000
url: /cpp/aspose.words/paragraphformat/get_shading/
---
## ParagraphFormat::get_Shading method


Returns a [Shading](../../shading/) object that refers to the shading formatting for the paragraph.

```cpp
System::SharedPtr<Aspose::Words::Shading> Aspose::Words::ParagraphFormat::get_Shading()
```


## Examples



Shows how to decorate text with borders and shading. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::BorderCollection> borders = builder->get_ParagraphFormat()->get_Borders();
borders->set_DistanceFromText(20);
borders->idx_get(Aspose::Words::BorderType::Left)->set_LineStyle(Aspose::Words::LineStyle::Double);
borders->idx_get(Aspose::Words::BorderType::Right)->set_LineStyle(Aspose::Words::LineStyle::Double);
borders->idx_get(Aspose::Words::BorderType::Top)->set_LineStyle(Aspose::Words::LineStyle::Double);
borders->idx_get(Aspose::Words::BorderType::Bottom)->set_LineStyle(Aspose::Words::LineStyle::Double);

System::SharedPtr<Aspose::Words::Shading> shading = builder->get_ParagraphFormat()->get_Shading();
shading->set_Texture(Aspose::Words::TextureIndex::TextureDiagonalCross);
shading->set_BackgroundPatternColor(System::Drawing::Color::get_LightCoral());
shading->set_ForegroundPatternColor(System::Drawing::Color::get_LightSalmon());

builder->Write(u"This paragraph is formatted with a double border and shading.");
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.ApplyBordersAndShading.docx");
```

## See Also

* Class [Shading](../../shading/)
* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
