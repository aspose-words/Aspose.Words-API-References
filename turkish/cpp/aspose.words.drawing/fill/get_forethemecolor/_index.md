---
title: "Aspose::Words::Drawing::Fill::get_ForeThemeColor metodu"
linktitle: "get_ForeThemeColor"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Fill::get_ForeThemeColor metodu. Doldurma için ön plan rengini temsil eden bir ThemeColor nesnesini alır veya ayarlar C++'ta."
type: docs
weight: 8000
url: /tr/cpp/aspose.words.drawing/fill/get_forethemecolor/
---
## Fill::get_ForeThemeColor method


Dolgu için ön plan rengini temsil eden bir ThemeColor nesnesini alır veya ayarlar.

```cpp
Aspose::Words::Themes::ThemeColor Aspose::Words::Drawing::Fill::get_ForeThemeColor()
```


## Örnekler



Ön plan/arka plan şekil rengi için tema renginin nasıl ayarlanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::RoundRectangle, 80, 80);

System::SharedPtr<Aspose::Words::Drawing::Fill> fill = shape->get_Fill();
fill->set_ForeThemeColor(Aspose::Words::Themes::ThemeColor::Dark1);
fill->set_BackThemeColor(Aspose::Words::Themes::ThemeColor::Background2);

// Not: Yazı tipi dolgu için "BackThemeColor" ve "BackTintAndShade" kullanmayın.
if (fill->get_BackTintAndShade() == 0)
{
    fill->set_BackTintAndShade(0.2);
}

doc->Save(get_ArtifactsDir() + u"Shape.FillThemeColor.docx");
```

## Ayrıca Bakınız

* Enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
