---
title: "Aspose::Words::Font::get_Underline yöntemi"
linktitle: "get_Underline"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Font::get_Underline yöntemi. C++'ta yazı tipine uygulanan alt çizgi türünü alır veya ayarlar."
type: docs
weight: 55000
url: /tr/cpp/aspose.words/font/get_underline/
---
## Font::get_Underline method


Yazı tipine uygulanan alt çizgi türünü alır veya ayarlar.

```cpp
Aspose::Words::Underline Aspose::Words::Font::get_Underline()
```


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


Bir hiperlink alanının nasıl ekleneceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"For more information, please visit the ");

// Bir hiperlink ekleyin ve özel biçimlendirme ile vurgulayın.
// Hiperlink, URL'de belirtilen konuma götürecek tıklanabilir bir metin parçası olacaktır.
builder->get_Font()->set_Color(System::Drawing::Color::get_Blue());
builder->get_Font()->set_Underline(Aspose::Words::Underline::Single);
builder->InsertHyperlink(u"Google website", u"https://www.google.com", false);
builder->get_Font()->ClearFormatting();
builder->Writeln(u".");

// Microsoft Word'de metindeki bağlantıya Ctrl + sol tıklama, yeni bir web tarayıcı penceresi aracılığıyla URL'ye götürür.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertHyperlink.docx");
```


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

* Enum [Underline](../../underline/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
