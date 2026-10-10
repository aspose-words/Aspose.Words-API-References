---
title: "Aspose::Words::Font::get_Name yöntemi"
linktitle: "get_Name"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Font::get_Name yöntemi. C++'ta yazı tipinin adını alır veya ayarlar."
type: docs
weight: 25000
url: /tr/cpp/aspose.words/font/get_name/
---
## Font::get_Name method


Yazı tipinin adını alır veya ayarlar.

```cpp
System::String Aspose::Words::Font::get_Name()
```

## Açıklamalar


Alırken, [NameAscii](../get_nameascii/) döndürür.

Ayarlarken, belirtilen değere [NameAscii](../get_nameascii/), [NameBi](../get_namebi/), [NameFarEast](../get_namefareast/) ve [NameOther](../get_nameother/) ayarlar.

## Örnekler



Biçimlendirilmiş metni [DocumentBuilder](../../documentbuilder/) kullanarak nasıl ekleyeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Yazı tipi biçimlendirmesini belirtin, ardından metin ekleyin.
System::SharedPtr<Aspose::Words::Font> font = builder->get_Font();
font->set_Size(16);
font->set_Bold(true);
font->set_Color(System::Drawing::Color::get_Blue());
font->set_Name(u"Courier New");
font->set_Underline(Aspose::Words::Underline::Dash);

builder->Write(u"Hello world!");
```


Bir metin run'ını font özelliğini kullanarak nasıl biçimlendireceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");

System::SharedPtr<Aspose::Words::Font> font = run->get_Font();
font->set_Name(u"Courier New");
font->set_Size(36);
font->set_HighlightColor(System::Drawing::Color::get_Yellow());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);
doc->Save(get_ArtifactsDir() + u"Font.CreateFormattedRun.docx");
```

## Ayrıca Bakınız

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
