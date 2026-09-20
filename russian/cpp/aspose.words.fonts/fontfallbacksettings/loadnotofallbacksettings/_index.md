---
title: "Метод Aspose::Words::Fonts::FontFallbackSettings::LoadNotoFallbackSettings"
linktitle: "LoadNotoFallbackSettings"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Fonts::FontFallbackSettings::LoadNotoFallbackSettings. Загружает предопределённые настройки резервных шрифтов, использующие шрифты Google Noto, в C++."
type: docs
weight: 7000
url: /ru/cpp/aspose.words.fonts/fontfallbacksettings/loadnotofallbacksettings/
---
## FontFallbackSettings::LoadNotoFallbackSettings method


Загружает предопределённые настройки резервного шрифта, которые используют шрифты Google Noto.

```cpp
void Aspose::Words::Fonts::FontFallbackSettings::LoadNotoFallbackSettings()
```


## Примеры



Показывает, как добавить предопределённые настройки резервных шрифтов для шрифтов Google Noto.
```cpp
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();

// Это бесплатные шрифты, лицензированные по SIL Open Font License.
// Мы можем скачать шрифты здесь:
// https://www.google.com/get/noto/#sans-lgc
fontSettings->SetFontsFolder(get_FontsDir() + u"Noto", false);

// Обратите внимание, что предопределённые настройки используют только шрифты Noto в стиле Sans с обычным начертанием.
// Некоторые шрифты Noto используют расширенные типографические функции.
// Шрифты с расширенной типографикой могут отображаться некорректно, так как Aspose.Words в настоящее время их не поддерживает.
fontSettings->get_FallbackSettings()->LoadNotoFallbackSettings();
fontSettings->get_SubstitutionSettings()->get_FontInfoSubstitution()->set_Enabled(false);
fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_DefaultFontName(u"Noto Sans");

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(fontSettings);
```


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
