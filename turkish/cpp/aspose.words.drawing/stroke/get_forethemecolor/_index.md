---
title: "Aspose::Words::Drawing::Stroke::get_ForeThemeColor metodu"
linktitle: "get_ForeThemeColor"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Stroke::get_ForeThemeColor metodu. C++'ta çizgi ön plan rengini temsil eden bir ThemeColor nesnesini alır veya ayarlar."
type: docs
weight: 10334
url: /tr/cpp/aspose.words.drawing/stroke/get_forethemecolor/
---
## Stroke::get_ForeThemeColor method


Çizgi ön plan rengini temsil eden bir ThemeColor nesnesini alır veya ayarlar.

```cpp
Aspose::Words::Themes::ThemeColor Aspose::Words::Drawing::Stroke::get_ForeThemeColor()
```


## Örnekler



Ön tema rengini ve tonlama ile gölgelendirmeyi nasıl ayarlayacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 100, 40);
System::SharedPtr<Aspose::Words::Drawing::Stroke> stroke = shape->get_Stroke();
stroke->set_ForeThemeColor(Aspose::Words::Themes::ThemeColor::Dark1);
stroke->set_ForeTintAndShade(0.5);

doc->Save(get_ArtifactsDir() + u"Shape.StrokeForeThemeColors.docx");
```

## Ayrıca Bakınız

* Enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* Class [Stroke](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
