---
title: "Aspose::Words::Fonts::FontSettings::get_DefaultInstance metodu"
linktitle: "get_DefaultInstance"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::FontSettings::get_DefaultInstance metodu. C++'ta statik varsayılan yazı tipi ayarları."
type: docs
weight: 1000
url: /tr/cpp/aspose.words.fonts/fontsettings/get_defaultinstance/
---
## FontSettings::get_DefaultInstance method


Statik varsayılan yazı tipi ayarları.

```cpp
static System::SharedPtr<Aspose::Words::Fonts::FontSettings> Aspose::Words::Fonts::FontSettings::get_DefaultInstance()
```


## Örnekler



Varsayılan yazı tipi ayarları örneğinin nasıl yapılandırılacağını gösterir.
```cpp
// Varsayılan yazı tipi ayarları örneğini "Courier New" yazı tipini kullanacak şekilde yapılandırın
// bilinmeyen bir yazı tipi kullanmaya çalıştığımızda yedek bir ikame olarak.
Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_DefaultFontName(u"Courier New");

ASSERT_TRUE(Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->get_SubstitutionSettings()->get_DefaultFontSubstitution()->get_Enabled());

auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Non-existent font");
builder->Write(u"Hello world!");

// Bu belgenin FontSettings yapılandırması yok. Belgeyi işlediğimizde,
// varsayılan FontSettings örneği eksik yazı tipini çözecektir.
// Aspose.Words, bilinmeyen yazı tipini kullanan metni işlemek için "Courier New" kullanacaktır.
ASSERT_TRUE(System::TestTools::IsNull(doc->get_FontSettings()));

doc->Save(get_ArtifactsDir() + u"FontSettings.DefaultFontInstance.pdf");
```

## Ayrıca Bakınız

* Class [FontSettings](../)
* Class [FontSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
