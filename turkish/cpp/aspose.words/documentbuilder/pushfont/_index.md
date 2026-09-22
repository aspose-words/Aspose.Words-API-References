---
title: "Aspose::Words::DocumentBuilder::PushFont method"
linktitle: "PushFont"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentBuilder::PushFont yöntemi. Mevcut karakter biçimlendirmesini C++'da yığına kaydeder."
type: docs
weight: 63000
url: /tr/cpp/aspose.words/documentbuilder/pushfont/
---
## DocumentBuilder::PushFont method


Geçerli karakter biçimlendirmesini yığına kaydeder.

```cpp
void Aspose::Words::DocumentBuilder::PushFont()
```


## Örnekler



Bir belge oluşturucusunun biçimlendirme yığını nasıl kullanılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Yazı tipi biçimlendirmesini ayarlayın, ardından köprüden önce gelen metni yazın.
builder->get_Font()->set_Name(u"Arial");
builder->get_Font()->set_Size(24);
builder->Write(u"To visit Google, hold Ctrl and click ");

// Mevcut biçimlendirme yapılandırmamızı yığında koruyun.
builder->PushFont();

// Yeni bir stil uygulayarak oluşturucunun mevcut biçimlendirmesini değiştirin.
builder->get_Font()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Hyperlink);
builder->InsertHyperlink(u"here", u"http://www.google.com", false);

ASSERT_EQ(System::Drawing::Color::get_Blue().ToArgb(), builder->get_Font()->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::Underline::Single, builder->get_Font()->get_Underline());

// Daha önce kaydettiğimiz yazı tipi biçimlendirmesini geri yükleyin ve öğeyi yığından kaldırın.
builder->PopFont();

ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), builder->get_Font()->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::Underline::None, builder->get_Font()->get_Underline());

builder->Write(u". We hope you enjoyed the example.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.PushPopFont.docx");
```

## Ayrıca Bakınız

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
