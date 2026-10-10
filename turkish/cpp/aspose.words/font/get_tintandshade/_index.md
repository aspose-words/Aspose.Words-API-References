---
title: "Aspose::Words::Font::get_TintAndShade yöntemi"
linktitle: "get_TintAndShade"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Font::get_TintAndShade yöntemi. C++'ta bir rengi aydınlatan veya karartan çift değer alır veya ayarlar."
type: docs
weight: 54000
url: /tr/cpp/aspose.words/font/get_tintandshade/
---
## Font::get_TintAndShade method


Bir rengi açan veya karartan çift bir değeri alır veya ayarlar.

```cpp
double Aspose::Words::Font::get_TintAndShade()
```

## Açıklamalar


Bu özellik için izin verilen değerler -1 (en koyu) ile 1 (en açık) arasında değişir.

Sıfır (0) nötrdür.

## Örnekler



Temalı stili oluşturma ve kullanma yöntemini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln();

// Tema yazı tipi özellikleriyle bazı stiller oluşturun.
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"ThemedStyle");
style->get_Font()->set_ThemeFont(Aspose::Words::Themes::ThemeFont::Major);
style->get_Font()->set_ThemeColor(Aspose::Words::Themes::ThemeColor::Accent5);
style->get_Font()->set_TintAndShade(0.3);

builder->get_ParagraphFormat()->set_StyleName(u"ThemedStyle");
builder->Writeln(u"Text with themed style");
```

## Ayrıca Bakınız

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
