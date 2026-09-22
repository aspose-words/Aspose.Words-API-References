---
title: "Aspose::Words::Font::get_NameFarEast metodu"
linktitle: "get_NameFarEast"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Font::get_NameFarEast metodu. C++'ta Doğu Asya bir yazı tipi adını döndürür veya ayarlar."
type: docs
weight: 28000
url: /tr/cpp/aspose.words/font/get_namefareast/
---
## Font::get_NameFarEast method


Doğu Asya yazı tipi adını alır veya ayarlar.

```cpp
System::String Aspose::Words::Font::get_NameFarEast()
```


## Örnekler



Uzak Doğu dilinde metin ekleme ve biçimlendirme nasıl yapılır gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Belge oluşturucunun eklediği herhangi bir metne uygulayacağı yazı tipi ayarlarını belirtin.
builder->get_Font()->set_Name(u"Courier New");
builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"en-US", false)->get_LCID());

// Yazı tipimiz ve yerel ayarımız için "FarEast" eşdeğerlerini adlandırın.
// Eğer oluşturucu bu Yazı tipi yapılandırmasıyla Asya karakterleri eklerse, bu karakterleri içeren her run
// bu karakterler, varsayılan yerine "FarEast" yazı tipi/yerel ayarı kullanarak görüntülenecek.
// Bu, batı yazı tipinin Asya karakterleri için ideal temsiller sunmadığı durumlarda faydalı olabilir.
builder->get_Font()->set_NameFarEast(u"SimSun");
builder->get_Font()->set_LocaleIdFarEast(System::MakeObject<System::Globalization::CultureInfo>(u"zh-CN", false)->get_LCID());

// Bu metin varsayılan yazı tipi/yerel ayarda görüntülenecek.
builder->Writeln(u"Hello world!");

// Bunlar Asya karakterleri olduğu için, bu run bizim "FarEast" yazı tipi/yerel ayar eşdeğerlerimizi uygulayacak.
builder->Writeln(u"你好世界");

doc->Save(get_ArtifactsDir() + u"Font.FarEast.docx");
```

## Ayrıca Bakınız

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
