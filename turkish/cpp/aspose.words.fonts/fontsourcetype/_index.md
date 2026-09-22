---
title: "Aspose::Words::Fonts::FontSourceType enum"
linktitle: "FontSourceType"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fonts::FontSourceType enum. C++'de font kaynağının türünü belirtir."
type: docs
weight: 23000
url: /tr/cpp/aspose.words.fonts/fontsourcetype/
---
## FontSourceType enum


Yazı tipi kaynağının türünü belirtir.

```cpp
enum class FontSourceType
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| FontFile | 0 | Tek bir font dosyasını temsil eden bir [FileFontSource](../filefontsource/) nesnesi. |
| FontsFolder | 1 | Font dosyalarını içeren bir klasörü temsil eden bir [FolderFontSource](../folderfontsource/) nesnesi. |
| MemoryFont | 2 | Bellekteki tek bir fontu temsil eden bir [MemoryFontSource](../memoryfontsource/) nesnesi. |
| SystemFonts | 3 | Sisteme yüklü tüm fontları temsil eden bir [SystemFontSource](../systemfontsource/) nesnesi. |
| FontStream | 4 | Font verileri içeren bir akışı temsil eden bir [StreamFontSource](../streamfontsource/) nesnesi. |


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

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
