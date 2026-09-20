---
title: "Aspose::Words::Fonts::FontConfigSubstitutionRule класс"
linktitle: "FontConfigSubstitutionRule"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fonts::FontConfigSubstitutionRule класс. Правило замены конфигурации шрифтов. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.fonts/fontconfigsubstitutionrule/
---
## FontConfigSubstitutionRule class


[Font](../../aspose.words/font/) config substitution rule. To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/) documentation article.

```cpp
class FontConfigSubstitutionRule : public Aspose::Words::Fonts::FontSubstitutionRule
```

## Методы

| Метод | Описание |
| --- | --- |
| virtual [get_Enabled](../fontsubstitutionrule/get_enabled/)() | Указывает, включено правило или нет. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsFontConfigAvailable](./isfontconfigavailable/)() | Проверьте, доступна ли утилита fontconfig или нет. |
| [ResetCache](./resetcache/)() | Сбрасывает кэш результатов вызова fontconfig. |
| [set_Enabled](./set_enabled/)(bool) override | Указывает, включено правило или нет. |
| static [Type](./type/)() |  |
## Примечания


Это правило использует утилиту fontconfig на платформах Linux (и других Unix-подобных), чтобы получить замену, если оригинальный шрифт недоступен.

Если утилита fontconfig недоступна, то это правило будет проигнорировано.

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

* Class [FontSubstitutionRule](../fontsubstitutionrule/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
