---
title: "Aspose::Words::Fonts::FontSubstitutionRule класс"
linktitle: "FontSubstitutionRule"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fonts::FontSubstitutionRule класс. Это абстрактный базовый класс для правила замены шрифтов. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 12000
url: /ru/cpp/aspose.words.fonts/fontsubstitutionrule/
---
## FontSubstitutionRule class


Это абстрактный базовый класс для правила подстановки шрифтов. Чтобы узнать больше, посетите статью документации [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class FontSubstitutionRule : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| virtual [get_Enabled](./get_enabled/)() | Указывает, включено правило или нет. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [set_Enabled](./set_enabled/)(bool) | Сеттер для [Aspose::Words::Fonts::FontSubstitutionRule::get_Enabled](./get_enabled/). |
| static [Type](./type/)() |  |

## Примеры



Показывает зависимую от операционной системы замену конфигурации шрифтов.
```cpp
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
System::SharedPtr<Aspose::Words::Fonts::FontConfigSubstitutionRule> fontConfigSubstitution = fontSettings->get_SubstitutionSettings()->get_FontConfigSubstitution();

bool isWindows = System::MakeArray<System::PlatformID>({System::PlatformID::Win32NT, System::PlatformID::Win32S, System::PlatformID::Win32Windows, System::PlatformID::WinCE})->LINQ_Any(static_cast<System::Func<System::PlatformID, bool>>(static_cast<std::function<bool(System::PlatformID p)>>([](System::PlatformID p) -> bool
{
    return System::Environment::get_OSVersion().get_Platform() == p;
})));

// Объект FontConfigSubstitutionRule работает по‑разному на платформах Windows и не‑Windows.
// На Windows он недоступен.
if (isWindows)
{
    ASSERT_FALSE(fontConfigSubstitution->get_Enabled());
    ASSERT_FALSE(fontConfigSubstitution->IsFontConfigAvailable());
}

bool isLinuxOrMac = System::MakeArray<System::PlatformID>({System::PlatformID::Unix, System::PlatformID::MacOSX})->LINQ_Any(static_cast<System::Func<System::PlatformID, bool>>(static_cast<std::function<bool(System::PlatformID p)>>([](System::PlatformID p) -> bool
{
    return System::Environment::get_OSVersion().get_Platform() == p;
})));

// На Linux/Mac мы будем иметь к нему доступ и сможем выполнять операции.
if (isLinuxOrMac)
{
    ASSERT_TRUE(fontConfigSubstitution->get_Enabled());
    ASSERT_TRUE(fontConfigSubstitution->IsFontConfigAvailable());

    fontConfigSubstitution->ResetCache();
}
```

## См. также

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
