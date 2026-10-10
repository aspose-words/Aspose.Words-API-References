---
title: "Aspose::Words::Fonts::FontSourceBase::get_Priority method"
linktitle: "get_Priority"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fonts::FontSourceBase::get_Priority method. C++'ta yazı tipi kaynağı önceliğini döndürür."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.fonts/fontsourcebase/get_priority/
---
## FontSourceBase::get_Priority method


Yazı tipi kaynağı önceliğini döndürür.

```cpp
int32_t Aspose::Words::Fonts::FontSourceBase::get_Priority() const
```

## Açıklamalar


Bu değer, farklı yazı tipi kaynaklarında aynı aile adı ve stile sahip yazı tipleri olduğunda kullanılır. Bu durumda Aspose.Words, daha yüksek öncelik değerine sahip kaynaktan yazı tipini seçer.

Varsayılan değer 0'dır.

## Örnekler



Yerel dosya sistemindeki bir yazı tipi dosyasını yazı tipi kaynağı olarak nasıl kullanılacağını gösterir.
```cpp
auto fileFontSource = System::MakeObject<Aspose::Words::Fonts::FileFontSource>(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf", 0);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({fileFontSource}));

ASSERT_EQ(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf", fileFontSource->get_FilePath());
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::FontFile, fileFontSource->get_Type());
ASSERT_EQ(0, fileFontSource->get_Priority());
```

## Ayrıca Bakınız

* Class [FontSourceBase](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
