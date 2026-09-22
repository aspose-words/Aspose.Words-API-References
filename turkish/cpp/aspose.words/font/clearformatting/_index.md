---
title: "Aspose::Words::Font::ClearFormatting metodu"
linktitle: "ClearFormatting"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Font::ClearFormatting metodu. C++'da varsayılan yazı tipi biçimlendirmesine sıfırlar."
type: docs
weight: 2000
url: /tr/cpp/aspose.words/font/clearformatting/
---
## Font::ClearFormatting method


Varsayılan yazı tipi biçimlendirmesini sıfırlar.

```cpp
void Aspose::Words::Font::ClearFormatting()
```

## Açıklamalar


Alındığı nesneden [Font](../) elde edilen nesne üzerinde açıkça belirtilen tüm yazı tipi biçimlendirmelerini kaldırır, böylece yazı tipi biçimlendirmesi uygun üst nesneden devralınır.

## Örnekler



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

## Ayrıca Bakınız

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
