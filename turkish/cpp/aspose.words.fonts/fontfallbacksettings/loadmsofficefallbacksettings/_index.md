---
title: "Aspose::Words::Fonts::FontFallbackSettings::LoadMsOfficeFallbackSettings method"
linktitle: "LoadMsOfficeFallbackSettings"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fonts::FontFallbackSettings::LoadMsOfficeFallbackSettings method. Microsoft Word yedeklemesini taklit eden ve C++'da Microsoft Office fontlarını kullanan önceden tanımlanmış yedek ayarları yükler."
type: docs
weight: 6000
url: /tr/cpp/aspose.words.fonts/fontfallbacksettings/loadmsofficefallbacksettings/
---
## FontFallbackSettings::LoadMsOfficeFallbackSettings method


Microsoft Word geri dönüşünü taklit eden ve Microsoft Office yazı tiplerini kullanan önceden tanımlı geri dönüş ayarlarını yükler.

```cpp
void Aspose::Words::Fonts::FontFallbackSettings::LoadMsOfficeFallbackSettings()
```


## Örnekler



Önceden tanımlı geri dönüş font ayarlarını nasıl yükleyeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
doc->set_FontSettings(fontSettings);
System::SharedPtr<Aspose::Words::Fonts::FontFallbackSettings> fontFallbackSettings = fontSettings->get_FallbackSettings();

// Varsayılan yedek font şemasını bir XML belgesine kaydedin.
// Örneğin, öğelerden biri Range için "0C00-0C7F" değerine ve FallbackFonts için karşılık gelen "Vani" değerine sahiptir.
// Bu, bir metnin kullandığı font 0x0C00-0x0C7F Unicode bloğu için sembollere sahip değilse anlamına gelir,
// yedek şema, "Vani" font ikamesindeki sembolleri kullanacaktır.
fontFallbackSettings->Save(get_ArtifactsDir() + u"FontSettings.FallbackSettings.Default.xml");

// Aşağıda seçebileceğimiz iki önceden tanımlanmış font yedekleme şeması bulunmaktadır.
// 1 -  Varsayılan Microsoft Office şemasını kullanın, bu varsayılan olanla aynıdır:
fontFallbackSettings->LoadMsOfficeFallbackSettings();
fontFallbackSettings->Save(get_ArtifactsDir() + u"FontSettings.FallbackSettings.LoadMsOfficeFallbackSettings.xml");

// 2 -  Google Noto fontlarından oluşturulan şemayı kullanın:
fontFallbackSettings->LoadNotoFallbackSettings();
fontFallbackSettings->Save(get_ArtifactsDir() + u"FontSettings.FallbackSettings.LoadNotoFallbackSettings.xml");
```

## Ayrıca Bakınız

* Class [FontFallbackSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
