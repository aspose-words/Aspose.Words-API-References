---
title: "Aspose::Words::Fonts::FileFontSource::get_Type metodu"
linktitle: "get_Type"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fonts::FileFontSource::get_Type metodu. C++'ta font kaynağının tipini döndürür."
type: docs
weight: 5000
url: /tr/cpp/aspose.words.fonts/filefontsource/get_type/
---
## FileFontSource::get_Type method


Yazı tipi kaynağının türünü döndürür.

```cpp
Aspose::Words::Fonts::FontSourceType Aspose::Words::Fonts::FileFontSource::get_Type() override
```


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

* Enum [FontSourceType](../../fontsourcetype/)
* Class [FileFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
