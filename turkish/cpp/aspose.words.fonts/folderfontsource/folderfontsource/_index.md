---
title: "Aspose::Words::Fonts::FolderFontSource::FolderFontSource yapıcı"
linktitle: "FolderFontSource"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fonts::FolderFontSource::FolderFontSource yapıcı. C++'daki ctor."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.fonts/folderfontsource/folderfontsource/
---
## FolderFontSource::FolderFontSource(const System::String\&, bool) constructor


Yapıcı.

```cpp
Aspose::Words::Fonts::FolderFontSource::FolderFontSource(const System::String &folderPath, bool scanSubfolders)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| folderPath | const System::String\& | Klasöre yol. |
| scanSubfolders | bool | Alt klasörleri tarayıp taramayacağını belirler. |

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

* Class [FolderFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
## FolderFontSource::FolderFontSource(const System::String\&, bool, int32_t) constructor


Yapıcı.

```cpp
Aspose::Words::Fonts::FolderFontSource::FolderFontSource(const System::String &folderPath, bool scanSubfolders, int32_t priority)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| folderPath | const System::String\& | Klasöre yol. |
| scanSubfolders | bool | Alt klasörleri tarayıp taramayacağını belirler. |
| priority | int32_t | [Font](../../../aspose.words/font/) kaynağı önceliği. Daha fazla bilgi için [Priority](../../fontsourcebase/get_priority/) özelliği açıklamasına bakın. |

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

* Class [FolderFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
