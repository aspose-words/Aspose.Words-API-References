---
title: "Aspose::Words::ParagraphFormat::get_Shading method"
linktitle: "get_Shading"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::ParagraphFormat::get_Shading 方法。返回一个 Shading 对象，该对象引用段落的着色格式（在 C++ 中）。"
type: docs
weight: 29000
url: /zh/cpp/aspose.words/paragraphformat/get_shading/
---
## ParagraphFormat::get_Shading method


返回一个 [Shading](../../shading/) 对象，该对象引用段落的着色格式。

```cpp
System::SharedPtr<Aspose::Words::Shading> Aspose::Words::ParagraphFormat::get_Shading()
```


## 示例



展示如何使用边框和阴影装饰文本。
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

## 另见

* Class [Shading](../../shading/)
* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
