---
title: "Aspose::Words::Shading::get_ForegroundPatternColor método"
linktitle: "get_ForegroundPatternColor"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Shading::get_ForegroundPatternColor método. Obtiene o establece el color que se aplica al primer plano del objeto Shading en C++."
type: docs
weight: 7000
url: /es/cpp/aspose.words/shading/get_foregroundpatterncolor/
---
## Shading::get_ForegroundPatternColor method


Obtiene o establece el color que se aplica al primer plano del objeto [Shading](../).

```cpp
System::Drawing::Color Aspose::Words::Shading::get_ForegroundPatternColor()
```


## Ejemplos



Muestra cómo decorar el texto con bordes y sombreado.
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

## Ver también

* Class [Shading](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
