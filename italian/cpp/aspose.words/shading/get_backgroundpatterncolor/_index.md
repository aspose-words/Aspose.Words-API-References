---
title: "Aspose::Words::Shading::get_BackgroundPatternColor metodo"
linktitle: "get_BackgroundPatternColor"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Shading::get_BackgroundPatternColor metodo. Ottiene o imposta il colore che viene applicato allo sfondo dell'oggetto Shading in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words/shading/get_backgroundpatterncolor/
---
## Shading::get_BackgroundPatternColor method


Ottiene o imposta il colore che viene applicato allo sfondo dell'oggetto [Shading](../).

```cpp
System::Drawing::Color Aspose::Words::Shading::get_BackgroundPatternColor()
```


## Esempi



Mostra come decorare il testo con bordi e ombreggiatura.
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

## Vedi anche

* Class [Shading](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
