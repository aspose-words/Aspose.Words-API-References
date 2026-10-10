---
title: "Aspose::Words::Drawing::Fill::get_BackTintAndShade metodu"
linktitle: "get_BackTintAndShade"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Fill::get_BackTintAndShade metodu. C++'ta arka plan rengini aydınlatan veya karartan bir double değer alır veya ayarlar."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.drawing/fill/get_backtintandshade/
---
## Fill::get_BackTintAndShade method


Arka plan rengini açan veya karartan bir double değerini alır veya ayarlar.

```cpp
double Aspose::Words::Drawing::Fill::get_BackTintAndShade()
```

## Açıklamalar


Bu özellik için izin verilen değerler -1 (en karanlık) ile 1 (en açık) arasındadır.

Sıfır (0) nötrdür.

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

* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
