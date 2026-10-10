---
title: "Aspose::Words::Fonts::FontInfo::get_Name metodu"
linktitle: "get_Name"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fonts::FontInfo::get_Name yöntemi. C++'ta yazı tipinin adını alır."
type: docs
weight: 6000
url: /tr/cpp/aspose.words.fonts/fontinfo/get_name/
---
## FontInfo::get_Name method


Yazı tipinin adını alır.

```cpp
System::String Aspose::Words::Fonts::FontInfo::get_Name() const
```

## Açıklamalar


**null** olamaz. Boş bir dize olabilir.

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
