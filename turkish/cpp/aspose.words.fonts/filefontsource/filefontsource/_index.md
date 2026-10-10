---
title: "Aspose::Words::Fonts::FileFontSource::FileFontSource yapıcı"
linktitle: "FileFontSource"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fonts::FileFontSource::FileFontSource yapıcı. C++'ta ctor."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.fonts/filefontsource/filefontsource/
---
## FileFontSource::FileFontSource(const System::String\&) constructor


Yapıcı.

```cpp
Aspose::Words::Fonts::FileFontSource::FileFontSource(const System::String &filePath)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| filePath | const System::String\& | Font dosyasının yolu. |

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

* Class [FileFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
## FileFontSource::FileFontSource(const System::String\&, int32_t) constructor


Yapıcı.

```cpp
Aspose::Words::Fonts::FileFontSource::FileFontSource(const System::String &filePath, int32_t priority)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| filePath | const System::String\& | Font dosyasının yolu. |
| priority | int32_t | [Font](../../../aspose.words/font/) kaynağı önceliği. Daha fazla bilgi için [Priority](../../fontsourcebase/get_priority/) özelliği açıklamasına bakın. |

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

* Class [FileFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
## FileFontSource::FileFontSource(const System::String\&, int32_t, const System::String\&) constructor


Yapıcı.

```cpp
Aspose::Words::Fonts::FileFontSource::FileFontSource(const System::String &filePath, int32_t priority, const System::String &cacheKey)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| filePath | const System::String\& | Font dosyasının yolu. |
| priority | int32_t | [Font](../../../aspose.words/font/) kaynağı önceliği. Daha fazla bilgi için [Priority](../../fontsourcebase/get_priority/) özelliği açıklamasına bakın. |
| cacheKey | const System::String\& | Bu kaynağın önbellekteki anahtarı. Daha fazla bilgi için [CacheKey](../get_cachekey/) özelliği açıklamasına bakın. |

## Ayrıca Bakınız

* Class [FileFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
