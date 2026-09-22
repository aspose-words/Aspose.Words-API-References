---
title: "Aspose::Words::Fonts::FontFallbackSettings::Load yöntemi"
linktitle: "Load"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fonts::FontFallbackSettings::Load yöntemi. C++'ta XML akışından geri dönüş ayarlarını yükler."
type: docs
weight: 5000
url: /tr/cpp/aspose.words.fonts/fontfallbacksettings/load/
---
## FontFallbackSettings::Load(const System::SharedPtr\<System::IO::Stream\>\&) method


XML akışından geri dönüş ayarlarını yükler.

```cpp
void Aspose::Words::Fonts::FontFallbackSettings::Load(const System::SharedPtr<System::IO::Stream> &stream)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| akış | const System::SharedPtr\<System::IO::Stream\>\& | Girdi akışı. |

## Örnekler



Bir akıştan font geri dönüş ayarlarını nasıl yükleyip kaydedileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Font geri dönüş ayarları kümesini tanımlayan bir XML belgesi yükleyin.
{
    auto fontFallbackStream = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Font fallback rules.xml", System::IO::FileMode::Open);
    auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
    fontSettings->get_FallbackSettings()->Load(fontFallbackStream);

    doc->set_FontSettings(fontSettings);
}

doc->Save(get_ArtifactsDir() + u"FontSettings.LoadFontFallbackSettingsFromStream.pdf");

// Belgemizin mevcut font geri dönüş ayarlarını bir XML belgesi olarak kaydetmek için bir akış kullanın.
{
    auto fontFallbackStream = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"FallbackSettings.xml", System::IO::FileMode::Create);
    doc->get_FontSettings()->get_FallbackSettings()->Save(fontFallbackStream);
}
```

## Ayrıca Bakınız

* Class [FontFallbackSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
## FontFallbackSettings::Load(const System::String\&) method


XML dosyasından yazı tipi geri dönüş ayarlarını yükler.

```cpp
void Aspose::Words::Fonts::FontFallbackSettings::Load(const System::String &fileName)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fileName | const System::String\& | Girdi dosya adı. |

## Örnekler



Yerel dosya sisteminde bir XML belgesinden font geri dönüş ayarlarını nasıl yükleyip kaydedileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Font geri dönüş ayarları kümesini tanımlayan bir XML belgesi yükleyin.
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
fontSettings->get_FallbackSettings()->Load(get_MyDir() + u"Font fallback rules.xml");

doc->set_FontSettings(fontSettings);
doc->Save(get_ArtifactsDir() + u"FontSettings.LoadFontFallbackSettingsFromFile.pdf");

// Belgemizin mevcut font geri dönüş ayarlarını bir XML belgesi olarak kaydedin.
doc->get_FontSettings()->get_FallbackSettings()->Save(get_ArtifactsDir() + u"FallbackSettings.xml");
```

## Ayrıca Bakınız

* Class [FontFallbackSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
## FontFallbackSettings::Load(std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> void Aspose::Words::Fonts::FontFallbackSettings::Load(std::basic_istream<CharType, Traits> &stream)
```

## Ayrıca Bakınız

* Class [FontFallbackSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
