---
title: "Aspose::Words::Fonts::FontInfo::get_IsTrueType metodu"
linktitle: "get_IsTrueType"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fonts::FontInfo::get_IsTrueType metodu. Bu yazı tipinin raster ya da vektör yazı tipi yerine TrueType veya OpenType yazı tipi olduğunu gösterir. Varsayılan değer C++'da doğrudur."
type: docs
weight: 5000
url: /tr/cpp/aspose.words.fonts/fontinfo/get_istruetype/
---
## FontInfo::get_IsTrueType method


Bu yazı tipinin raster veya vektör yazı tipi yerine TrueType veya OpenType yazı tipi olduğunu gösterir. Varsayılan **true**.

```cpp
bool Aspose::Words::Fonts::FontInfo::get_IsTrueType() const
```


## Örnekler



Bir belgede mevcut olan yazı tiplerinin ayrıntılarını nasıl yazdıracağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font.docx");

System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> allFonts = doc->get_FontInfos();

// Belgedeki kullanılan ve kullanılmayan tüm yazı tiplerini yazdırın.
for (int32_t i = 0; i < allFonts->get_Count(); i++)
{
    std::cout << System::String::Format(u"Font index #{0}", i) << std::endl;
    std::cout << System::String::Format(u"\tName: {0}", allFonts->idx_get(i)->get_Name()) << std::endl;
    std::cout << System::String::Format(u"\tIs {0}a trueType font", (allFonts->idx_get(i)->get_IsTrueType() ? System::String(u"") : System::String(u"not "))) << std::endl;
}
```

## Ayrıca Bakınız

* Class [FontInfo](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
