---
title: "Aspose::Words::Font::get_LocaleId metodu"
linktitle: "get_LocaleId"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Font::get_LocaleId metodu. C++'da biçimlendirilmiş karakterlerin yerel ayar tanımlayıcısını (dili) alır veya ayarlar."
type: docs
weight: 22000
url: /tr/cpp/aspose.words/font/get_localeid/
---
## Font::get_LocaleId method


Biçimlendirilmiş karakterlerin yerel kimliğini (dil) alır veya ayarlar.

```cpp
int32_t Aspose::Words::Font::get_LocaleId()
```


## Örnekler



Bir belge oluşturucu ile eklediğimiz metnin yerel ayarını nasıl ayarlayacağımızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Yazı tipinin yerel ayarını İngilizce olarak ayarlayıp bazı Rusça metin eklersek,
// İngilizce yerel ayar denetleyicisi metni tanımaz ve bir yazım hatası olarak algılar.
builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"en-US", false)->get_LCID());
builder->Writeln(u"Привет!");

// Uygun denetleyiciyi uygulamak için ekleyeceğimiz metne eşleşen bir yerel ayar ayarlayın.
builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"ru-RU", false)->get_LCID());
builder->Writeln(u"Привет!");

doc->Save(get_ArtifactsDir() + u"Font.LocaleId.docx");
```

## Ayrıca Bakınız

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
