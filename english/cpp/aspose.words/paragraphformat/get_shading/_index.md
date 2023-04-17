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

* Class [Shading](../../shading/)
* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
