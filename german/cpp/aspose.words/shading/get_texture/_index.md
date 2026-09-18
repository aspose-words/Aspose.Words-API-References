---
title: "Aspose::Words::Shading::get_Texture Methode"
linktitle: "get_Texture"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Shading::get_Texture Methode. Ruft die Schattierungstextur ab oder legt sie fest in C++."
type: docs
weight: 10000
url: /de/cpp/aspose.words/shading/get_texture/
---
## Shading::get_Texture method


Liest oder legt fest die Schattierungs-Textur.

```cpp
Aspose::Words::TextureIndex Aspose::Words::Shading::get_Texture()
```


## Beispiele



Zeigt, wie man Text mit Rahmen und Schattierung dekoriert.
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

## Siehe auch

* Enum [TextureIndex](../../textureindex/)
* Class [Shading](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
