---
title: "Aspose::Words::Shading::get_BackgroundPatternColor méthode"
linktitle: "get_BackgroundPatternColor"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Shading::get_BackgroundPatternColor méthode. Obtient ou définit la couleur qui''est appliquée à l'arrière-plan de l'objet Shading en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words/shading/get_backgroundpatterncolor/
---
## Shading::get_BackgroundPatternColor method


Obtient ou définit la couleur qui est appliquée à l'arrière-plan de l'objet [Shading](../).

```cpp
System::Drawing::Color Aspose::Words::Shading::get_BackgroundPatternColor()
```


## Exemples



Montre comment décorer le texte avec des bordures et de l’ombrage.
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

## Voir aussi

* Class [Shading](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
