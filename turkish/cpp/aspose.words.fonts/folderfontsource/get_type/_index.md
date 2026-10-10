---
title: "Aspose::Words::Fonts::FolderFontSource::get_Type yöntemi"
linktitle: "get_Type"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fonts::FolderFontSource::get_Type yöntemi. C++'ta font kaynağının tipini döndürür."
type: docs
weight: 5000
url: /tr/cpp/aspose.words.fonts/folderfontsource/get_type/
---
## FolderFontSource::get_Type method


Yazı tipi kaynağının türünü döndürür.

```cpp
Aspose::Words::Fonts::FontSourceType Aspose::Words::Fonts::FolderFontSource::get_Type() override
```


## Örnekler



Yazı tipi kaynağı olarak yazı tiplerini içeren yerel bir sistem klasörünün nasıl kullanılacağını gösterir.
```cpp
// Yazı tipi dosyalarını içeren bir klasörden yazı tipi kaynağı oluştur.
auto folderFontSource = System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), false, 1);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({folderFontSource}));

ASSERT_EQ(get_FontsDir(), folderFontSource->get_FolderPath());
ASPOSE_ASSERT_EQ(false, folderFontSource->get_ScanSubfolders());
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::FontsFolder, folderFontSource->get_Type());
ASSERT_EQ(1, folderFontSource->get_Priority());
```

## Ayrıca Bakınız

* Enum [FontSourceType](../../fontsourcetype/)
* Class [FolderFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
