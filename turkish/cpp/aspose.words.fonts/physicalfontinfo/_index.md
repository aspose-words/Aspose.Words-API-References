---
title: "Aspose::Words::Fonts::PhysicalFontInfo class"
linktitle: "PhysicalFontInfo"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fonts::PhysicalFontInfo class. Aspose.Words yazı tipi motoru için mevcut fiziksel yazı tipi hakkında bilgi belirtir. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 15000
url: /tr/cpp/aspose.words.fonts/physicalfontinfo/
---
## PhysicalFontInfo class


Aspose.Words yazı tipi motoru için mevcut fiziksel yazı tipleri hakkında bilgi belirtir. Daha fazla bilgi için, [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/) dokümantasyon makalesini ziyaret edin.

```cpp
class PhysicalFontInfo : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_EmbeddingLicensingRights](./get_embeddinglicensingrights/)() const | Yazı tipi için gömme lisans hakları. |
| [get_FilePath](./get_filepath/)() const | Varsa yazı tipi dosyasının yolu. |
| [get_FontFamilyName](./get_fontfamilyname/)() const | Yazı tipinin aile adı. |
| [get_FullFontName](./get_fullfontname/)() const | Yazı tipinin tam adı. |
| [get_Version](./get_version/)() const | Yazı tipinin sürüm dizesi. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## Örnekler



Kullanılabilir yazı tiplerini listeleme yöntemini gösterir.
```cpp
// Aspose.Words'ü özel bir klasörden yazı tipleri alacak şekilde yapılandırın ve ardından her kullanılabilir yazı tipini yazdırın.
System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> folderFontSource = System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), true)});

for (auto&& fontInfo : System::IterateOver(folderFontSource[0]->GetAvailableFonts()))
{
    std::cout << "FontFamilyName : " << fontInfo->get_FontFamilyName() << std::endl;
    std::cout << "FullFontName  : " << fontInfo->get_FullFontName() << std::endl;
    std::cout << "Version  : " << fontInfo->get_Version() << std::endl;
    std::cout << "FilePath : " << fontInfo->get_FilePath() << "\n" << std::endl;
}
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
