---
title: "Aspose::Words::Fonts::FontFallbackSettings::LoadNotoFallbackSettings yöntemi"
linktitle: "LoadNotoFallbackSettings"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fonts::FontFallbackSettings::LoadNotoFallbackSettings yöntemi. C++'ta Google Noto fontlarını kullanan önceden tanımlı geri dönüş ayarlarını yükler."
type: docs
weight: 7000
url: /tr/cpp/aspose.words.fonts/fontfallbacksettings/loadnotofallbacksettings/
---
## FontFallbackSettings::LoadNotoFallbackSettings method


Google Noto yazı tiplerini kullanan önceden tanımlı geri dönüş ayarlarını yükler.

```cpp
void Aspose::Words::Fonts::FontFallbackSettings::LoadNotoFallbackSettings()
```


## Örnekler



Google Noto fontları için önceden tanımlı font geri dönüş ayarlarını nasıl ekleyeceğinizi gösterir.
```cpp
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();

// Bunlar SIL Açık Font Lisansı altında lisanslanan ücretsiz fontlardır.
// Fontları buradan indirebiliriz:
// https://www.google.com/get/noto/#sans-lgc
fontSettings->SetFontsFolder(get_FontsDir() + u"Noto", false);

// Önceden tanımlı ayarların yalnızca normal ağırlıkta Sans stilinde Noto fontlarını kullandığını unutmayın.
// Noto fontlarının bazıları gelişmiş tipografi özelliklerini kullanır.
// Gelişmiş tipografi içeren fontlar, Aspose.Words şu anda bunları desteklemediği için doğru şekilde işlenemeyebilir.
fontSettings->get_FallbackSettings()->LoadNotoFallbackSettings();
fontSettings->get_SubstitutionSettings()->get_FontInfoSubstitution()->set_Enabled(false);
fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_DefaultFontName(u"Noto Sans");

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(fontSettings);
```


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
