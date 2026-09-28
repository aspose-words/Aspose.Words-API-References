---
title: "Aspose::Words::Fonts::FontFallbackSettings::LoadMsOfficeFallbackSettings метод"
linktitle: "LoadMsOfficeFallbackSettings"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fonts::FontFallbackSettings::LoadMsOfficeFallbackSettings метод. Загружает предопределённые настройки резервных шрифтов, имитирующие резервные шрифты Microsoft Word, и использует шрифты Microsoft Office в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words.fonts/fontfallbacksettings/loadmsofficefallbacksettings/
---
## FontFallbackSettings::LoadMsOfficeFallbackSettings method


Загружает предопределённые настройки резервного шрифта, которые имитируют резервный шрифт Microsoft Word и используют шрифты Microsoft Office.

```cpp
void Aspose::Words::Fonts::FontFallbackSettings::LoadMsOfficeFallbackSettings()
```


## Примеры



Показывает, как загрузить предопределённые настройки резервных шрифтов.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
doc->set_FontSettings(fontSettings);
System::SharedPtr<Aspose::Words::Fonts::FontFallbackSettings> fontFallbackSettings = fontSettings->get_FallbackSettings();

// Сохраните схему резервных шрифтов по умолчанию в XML-документ.
// Например, один из элементов имеет значение "0C00-0C7F" для Range и соответствующее значение "Vani" для FallbackFonts.
// Это означает, что если шрифт, используемый в некотором тексте, не содержит символов для диапазона Unicode 0x0C00-0x0C7F,
// резервная схема будет использовать символы из заменяющего шрифта "Vani".
fontFallbackSettings->Save(get_ArtifactsDir() + u"FontSettings.FallbackSettings.Default.xml");

// Ниже представлены две предопределённые схемы резервных шрифтов, из которых мы можем выбрать.
// 1 -  Использовать схему Microsoft Office по умолчанию, которая совпадает с текущей схемой по умолчанию:
fontFallbackSettings->LoadMsOfficeFallbackSettings();
fontFallbackSettings->Save(get_ArtifactsDir() + u"FontSettings.FallbackSettings.LoadMsOfficeFallbackSettings.xml");

// 2 -  Использовать схему, построенную на шрифтах Google Noto:
fontFallbackSettings->LoadNotoFallbackSettings();
fontFallbackSettings->Save(get_ArtifactsDir() + u"FontSettings.FallbackSettings.LoadNotoFallbackSettings.xml");
```

## См. также

* Class [FontFallbackSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
