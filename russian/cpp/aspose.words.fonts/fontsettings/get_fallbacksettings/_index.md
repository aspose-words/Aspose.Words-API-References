---
title: "Aspose::Words::Fonts::FontSettings::get_FallbackSettings метод"
linktitle: "get_FallbackSettings"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fonts::FontSettings::get_FallbackSettings метод. Параметры, связанные с механизмом резервного шрифта в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.fonts/fontsettings/get_fallbacksettings/
---
## FontSettings::get_FallbackSettings method


[Settings](../../../aspose.words.settings/) related to font fallback mechanism.

```cpp
System::SharedPtr<Aspose::Words::Fonts::FontFallbackSettings> Aspose::Words::Fonts::FontSettings::get_FallbackSettings() const
```


## Примеры



Показывает, как распределять резервные шрифты по диапазонам кодов символов Unicode.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
doc->set_FontSettings(fontSettings);
System::SharedPtr<Aspose::Words::Fonts::FontFallbackSettings> fontFallbackSettings = fontSettings->get_FallbackSettings();

// Настройте наши параметры шрифтов, чтобы получать шрифты только из папки "MyFonts".
auto folderFontSource = System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), false);
fontSettings->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({folderFontSource}));

// Вызов метода "BuildAutomatic" сгенерирует схему резервного шрифта, которая
// распределит доступные шрифты по максимально возможному количеству кодов символов Unicode.
// В нашем случае он имеет доступ только к небольшому набору шрифтов в папке "MyFonts".
fontFallbackSettings->BuildAutomatic();
fontFallbackSettings->Save(get_ArtifactsDir() + u"FontSettings.FallbackSettingsCustom.BuildAutomatic.xml");

// Мы также можем загрузить пользовательскую схему подстановки из файла, как показано.
// Эта схема применяет шрифт "AllegroOpen" к блокам Unicode "0000-00ff", шрифт "AllegroOpen" к диапазону "0100-024f",
// и шрифт "M+ 2m" во всех остальных диапазонах, которые не покрыты другими шрифтами схемы.
fontFallbackSettings->Load(get_MyDir() + u"Custom font fallback settings.xml");

// Создайте объект DocumentBuilder и установите его шрифт на тот, которого нет ни в одном из наших источников.
// Наши настройки шрифтов вызовут схему резервного шрифта для символов, набранных шрифтом, который недоступен.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->get_Font()->set_Name(u"Missing Font");

// Используйте builder для вывода каждого символа Unicode от 0x0021 до 0x052F,
// с описательными строками, разделяющими блоки Unicode, определённые в нашей пользовательской схеме резервного шрифта.
for (int32_t i = 0x0021; i < 0x0530; i++)
{
    switch (i)
    {
        case 0x0021:
            builder->Writeln(u"\n\n0x0021 - 0x00FF: \nBasic Latin/Latin-1 Supplement Unicode blocks in \"AllegroOpen\" font:");
            break;

        case 0x0100:
            builder->Writeln(u"\n\n0x0100 - 0x024F: \nLatin Extended A/B blocks, mostly in \"AllegroOpen\" font:");
            break;

        case 0x0250:
            builder->Writeln(u"\n\n0x0250 - 0x052F: \nIPA/Greek/Cyrillic blocks in \"M+ 2m\" font:");
            break;

    }

    builder->Write(System::String::Format(u"{0}", System::Convert::ToChar(i)));
}

doc->Save(get_ArtifactsDir() + u"FontSettings.FallbackSettingsCustom.pdf");
```

## См. также

* Class [FontFallbackSettings](../../fontfallbacksettings/)
* Class [FontSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
