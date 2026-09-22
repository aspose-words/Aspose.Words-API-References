---
title: "Aspose::Words::Font::get_UnderlineColor yöntemi"
linktitle: "get_UnderlineColor"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Font::get_UnderlineColor yöntemi. C++'ta fonta uygulanan alt çizginin rengini alır veya ayarlar."
type: docs
weight: 56000
url: /tr/cpp/aspose.words/font/get_underlinecolor/
---
## Font::get_UnderlineColor method


Yazı tipine uygulanan alt çizgi rengini alır veya ayarlar.

```cpp
System::Drawing::Color Aspose::Words::Font::get_UnderlineColor()
```


## Örnekler



Bir metin alt çizgisinin stilini ve rengini nasıl yapılandıracağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Underline(Aspose::Words::Underline::Dotted);
builder->get_Font()->set_UnderlineColor(System::Drawing::Color::get_Red());

builder->Writeln(u"Underlined text.");

doc->Save(get_ArtifactsDir() + u"Font.Underlines.docx");
```

## Ayrıca Bakınız

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
