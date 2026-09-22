---
title: "Aspose::Words::Shading::get_BackgroundTintAndShade metodu"
linktitle: "get_BackgroundTintAndShade"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Shading::get_BackgroundTintAndShade metodu. C++'ta bir arka plan tema rengini aydınlatan veya karartan çift bir değer alır veya ayarlar."
type: docs
weight: 6000
url: /tr/cpp/aspose.words/shading/get_backgroundtintandshade/
---
## Shading::get_BackgroundTintAndShade method


Arka plan tema rengini aydınlatan veya karartan bir double değerini alır veya ayarlar.

```cpp
double Aspose::Words::Shading::get_BackgroundTintAndShade()
```

## Açıklamalar


Bu özellik için izin verilen değerler -1 (en karanlık) ile 1 (en açık) arasındadır.

Sıfır (0) nötrdür.

## Örnekler



Shading dokusu için ön plan ve arka plan renklerinin nasıl ayarlanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Shading> shading = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Shading();
shading->set_Texture(Aspose::Words::TextureIndex::Texture12Pt5Percent);
shading->set_ForegroundPatternThemeColor(Aspose::Words::Themes::ThemeColor::Dark1);
shading->set_BackgroundPatternThemeColor(Aspose::Words::Themes::ThemeColor::Dark2);

shading->set_ForegroundTintAndShade(0.5);
shading->set_BackgroundTintAndShade(-0.2);

builder->get_Font()->get_Border()->set_Color(System::Drawing::Color::get_Green());
builder->get_Font()->get_Border()->set_LineWidth(2.5);
builder->get_Font()->get_Border()->set_LineStyle(Aspose::Words::LineStyle::DashDotStroker);

builder->Writeln(u"Foreground and background pattern colors for shading texture.");

doc->Save(get_ArtifactsDir() + u"Font.ForegroundAndBackground.docx");
```

## Ayrıca Bakınız

* Class [Shading](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
